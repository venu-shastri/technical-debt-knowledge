# CNC Monitoring and Alerting

We need a solution to interpret data coming out of a _CNC-machine monitor_.
Our purpose is to alert when something needs attention.
The alert needs to include information on the area that needs attention -
the machine or the environment.
The personnel that need to be alerted are different in each case.

A basic idea of CNC machines can be seen [here](https://en.wikipedia.org/wiki/Numerical_control).
Keeping these machines safe and reliable is vital in any manufacturing unit.

## Monitored data

The _CNC-machine monitor_ gives the following data:

- Operating temperature: Temperature around the CNC machine in Celsius.
Reported every half-hour. Need to alert if it goes beyond 35 degrees.

- Part-dimension variation: In mm. A variation of more than 0.05 mm needs attention
(example: a drill-bit in the machine may need replacement)

- Duration of continuous operation: Reported in minutes.
Updated once every 15 minutes.
More than 6 hours of continuous operation requires attention.

- Self-test status-code, reported at startup

| Code | Meaning |
|---:|---|
|0xFF|All ok|
|0x00|No data (examples: no power, no connection to the data-collector)|
|0x01|Controller board in the machine is not ok|
|0x02|Configuration data in the machine is corrupted|

Assume that the above data is monitored and passed-on to your program.
You can choose to take the inputs as function calls to your program, or as events.

## Expected outputs

The program needs to indicate if there is a need for attention.

When there is a need to attend,
it needs to offer an initial diagnosis,
to help in alerting the appropriate personnel:
It needs to convey whether the machine needs attention,
or if its environment needs attention.


```C++

#include <iostream>
#include <fstream>
#include <string>
using namespace std;

class CNCMachineMonitor {
private:
    float temperature;
    float dimensionVariation;
    int continuousOperationMinutes;
    int selfTestCode;

public:
    void updateTemperature(float valueCelsius) {
        temperature = valueCelsius;
        if (temperature > 35.0) {
            cout << "ALERT: High temperature detected (Environment)" << endl;
        }
    }

    void updateDimensionVariation(float variationMM) {
        dimensionVariation = variationMM;
        if (dimensionVariation > 0.05) {
            cout << "ALERT: Part-dimension variation too high (Machine)" << endl;
        }
    }

    void updateContinuousOperation(int minutes) {
        continuousOperationMinutes = minutes;
        if (continuousOperationMinutes > 360) {
            cout << "ALERT: Continuous operation exceeded 6 hours (Machine)" << endl;
        }
    }

    void checkSelfTestCode(int code) {
        selfTestCode = code;
        switch (code) {
            case 0xFF:
                cout << "Self-test OK" << endl;
                break;
            case 0x00:
                cout << "ALERT: No data from machine (Environment)" << endl;
                break;
            case 0x01:
                cout << "ALERT: Controller board failure (Machine)" << endl;
                break;
            case 0x02:
                cout << "ALERT: Configuration data corrupted (Machine)" << endl;
                break;
            default:
                cout << "ALERT: Unknown self-test code (Machine)" << endl;
        }
    }
};

int main() {
    CNCMachineMonitor monitor;
    ifstream infile("cnc_data.txt");

    if (!infile) {
        cerr << "Error opening input file." << endl;
        return 1;
    }

    float temp, variation;
    int minutes, selfTest;

    while (infile >> temp >> variation >> minutes >> hex >> selfTest) {
        monitor.updateTemperature(temp);
        monitor.updateDimensionVariation(variation);
        monitor.updateContinuousOperation(minutes);
        monitor.checkSelfTestCode(selfTest);
        cout << "---" << endl;
    }

    infile.close();
    return 0;
}

/*
Example input file (cnc_data.txt):
38.5 0.06 400 0x01
34.0 0.03 200 0xFF
36.0 0.04 300 0x00
*/

```


```C
#include <stdio.h>
#include <stdlib.h>

void update_temperature(float temp) {
    if (temp > 35.0) {
        printf("ALERT: High temperature detected (Environment)\n");
    }
}

void update_dimension_variation(float variation) {
    if (variation > 0.05) {
        printf("ALERT: Part-dimension variation too high (Machine)\n");
    }
}

void update_continuous_operation(int minutes) {
    if (minutes > 360) {
        printf("ALERT: Continuous operation exceeded 6 hours (Machine)\n");
    }
}

void check_self_test_code(int code) {
    switch (code) {
        case 0xFF:
            printf("Self-test OK\n");
            break;
        case 0x00:
            printf("ALERT: No data from machine (Environment)\n");
            break;
        case 0x01:
            printf("ALERT: Controller board failure (Machine)\n");
            break;
        case 0x02:
            printf("ALERT: Configuration data corrupted (Machine)\n");
            break;
        default:
            printf("ALERT: Unknown self-test code (Machine)\n");
            break;
    }
}

int main() {
    FILE *file = fopen("cnc_data.txt", "r");
    if (!file) {
        printf("Error opening input file.\n");
        return 1;
    }

    float temp, variation;
    int minutes, code;

    while (fscanf(file, "%f %f %d %x", &temp, &variation, &minutes, &code) == 4) {
        update_temperature(temp);
        update_dimension_variation(variation);
        update_continuous_operation(minutes);
        check_self_test_code(code);
        printf("---\n");
    }

    fclose(file);
    return 0;
}

/*
Example input file (cnc_data.txt):
38.5 0.06 400 0x01
34.0 0.03 200 0xFF
36.0 0.04 300 0x00
*/
```
