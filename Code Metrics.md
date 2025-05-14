# 📊 Code Metrics: List, Explanation, and Examples

This guide explains common code metrics used to evaluate code quality and maintainability, especially in C/C++ and embedded systems.

---
## 1. Cyclomatic Complexity

**What it measures:** Number of independent paths through code.

**Why it matters:** High complexity makes code harder to test and maintain.

**Example:**
```c
int calculate(int x) {
    if (x > 0) {
        if (x % 2 == 0) {
            return x / 2;
        } else {
            return x * 2;
        }
    } else {
        return 0;
    }
}
```
Cyclomatic complexity: 3

2. Lines of Code (LOC)
What it measures: Total lines in code.

Why it matters: Large functions or files often indicate poor structure.

Example:

```c
void longFunction() {
    // hundreds of lines...
}
```
3. Code Duplication
What it measures: Repeated blocks of code.

Why it matters: Makes maintenance and debugging harder.

Example:

```
void updateSensor1() { readADC(); filterData(); computeAverage(); }
void updateSensor2() { readADC(); filterData(); computeAverage(); }
```

4. Halstead Metrics
What it measures: Uses operators and operands to estimate complexity and effort.

Why it matters: Quantifies understandability and maintainability.

5. Maintainability Index
What it measures: Composite score from complexity, LOC, and Halstead metrics.

Why it matters: Indicates overall maintainability. Lower = worse.

6. Code Coverage
What it measures: % of code executed during tests.

Why it matters: Uncovered code = untested, risky paths.

Tools: gcov, Unity, CppUTest

7. Comment Density
What it measures: Ratio of comments to code.

Why it matters: Aids maintainability.

Example:
```
// Retry counter for failed attempts
int retryCount = 1;
```
8. Function/Module Coupling
What it measures: How interconnected modules are.

Why it matters: High coupling = fragile code.

Example:
```
void appFunction() {
    sensorDriverInit();
}
```
9. Fan-In / Fan-Out
What it measures:

Fan-In: How many modules call this one?

Fan-Out: How many modules it calls?

Example:
```
void controlLoop() {
    readSensors();
    filterData();
    controlMotor();
    logTelemetry();
}
```
📌 Summary Table
| Metric                | Measures                       | Why it Matters                       | Good Tools               |
| --------------------- | ------------------------------ | ------------------------------------ | ------------------------ |
| Cyclomatic Complexity | Logic branches in code         | Simpler code = fewer bugs            | SonarQube, Understand    |
| LOC                   | Code volume                    | Indicates potential complexity       | cloc, CLOC++, VSCode     |
| Duplication           | Repeated logic                 | Increases bugs and size              | SonarQube, CppCheck      |
| Halstead Metrics      | Cognitive load                 | Measures maintainability             | Understand               |
| Maintainability Index | Overall maintainability        | Composite health score               | Visual Studio, SonarQube |
| Code Coverage         | Test effectiveness             | Higher = better test assurance       | gcov, Unity, Bullseye    |
| Comment Density       | Documentation sufficiency      | Clarifies intent and maintainability | CLOC, VSCode             |
| Coupling              | Module interdependence         | Loosely coupled = more flexible      | Understand, Lizard       |
| Fan-In / Fan-Out      | Function/module responsibility | Too high = fragile or bloated design | Understand, Lizard       |

"""			
