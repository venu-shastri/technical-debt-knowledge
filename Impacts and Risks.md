📉 Impacts of Technical Debt

| **Time Horizon** | **Category**          | **Impact Description**                                           | **Example (Embedded)**                                |
| ---------------- | --------------------- | ---------------------------------------------------------------- | ----------------------------------------------------- |
| Short-term       | Development Velocity  | Faster initial development at the cost of cutting corners        | Skipping tests or hardcoding delays to meet deadlines |
| Short-term       | Product Delivery      | Quicker time-to-market with less stability                       | Releasing without full validation                     |
| Short-term       | Cost                  | Reduced short-term cost                                          | Avoiding refactoring or skipping code reviews         |
| Long-term        | Maintenance Burden    | Increasing effort needed to fix or modify code                   | Developers need hours to understand legacy modules    |
| Long-term        | Defect Rate           | More bugs due to fragile or complex code                         | ISR timing bugs surface during system integration     |
| Long-term        | Team Morale           | Developer frustration with messy, hard-to-understand code        | High turnover or burnout in firmware team             |
| Long-term        | Project Cost          | Accumulated debt increases cost of changes, testing, and updates | A minor feature takes weeks to integrate              |
| Long-term        | System Stability      | Potential crashes, misbehavior, or missed real-time deadlines    | Timer overflows due to hardcoded assumptions          |
| Long-term        | Safety and Compliance | Inability to pass audits or meet regulatory standards            | ISO 26262 failure due to poor documentation           |

⚠️ Risks of Ignoring Technical Debt

| **Risk**                       | **Description**                                                   | **Severity** | **Example**                                      |
| ------------------------------ | ----------------------------------------------------------------- | ------------ | ------------------------------------------------ |
| **System Failure**             | Critical bugs can cause hardware damage or safety hazards         | High         | Faulty motor control due to unvalidated inputs   |
| **Increased Development Time** | Every new feature requires workarounds or extra effort            | High         | New protocol requires rewriting existing stack   |
| **Test Coverage Gaps**         | Inadequate tests cause undetected regressions                     | High         | Bugs reintroduced due to missing tests    |
| **Loss of Knowledge**          | Tribal knowledge with no documentation                            | Medium       | Original authors left, code is undocumented      |
| **Customer Escalations**       | Bugs that escape to production impact customer trust              | High         | Devices freeze after 10 days due to watchdog bug |
| **Inability to Reuse**         | Code is too coupled or hardware-specific to reuse                 | Medium       | Sensor driver hardcoded to specific MCU pins     |
| **Blocked Certification**      | Product fails compliance due to bad traceability or missing tests | Critical     | Failure to meet DO-178C or IEC 61508 guidelines  |

# Technical Debt Risk Register

| Risk                    | Description                                                | Severity | Examples                                         | Mitigation Strategy                                |
|-------------------------|------------------------------------------------------------|----------|-------------------------------------------------|---------------------------------------------------|
| System Failure          | Critical bugs can cause hardware damage or safety hazards  | High     | Faulty motor control due to unvalidated inputs   | Refactor regularly and add validation              |
| Increased Development Time | Every new feature requires workarounds or extra effort  | High     | New protocol requires rewriting existing stack   | Allocate time for debt reduction                     |
| Test Coverage Gaps      | Inadequate tests cause undetected regressions              | High     | Memory leak reintroduced due to missing tests    | Increase automated tests and code reviews           |
| Loss of Knowledge       | Tribal knowledge with no documentation                      | Medium   | Original authors left, code is undocumented      | Document thoroughly and onboard new developers      |
| Customer Escalations    | Bugs that escape to production impact customer trust       | High     | Devices freeze after 10 days due to watchdog bug | Improve testing and monitoring                        |
| Inability to Reuse      | Code is too coupled or hardware-specific to reuse          | Medium   | Sensor driver hardcoded to specific MCU pins     | Modularize and decouple code                          |
| Blocked Certification   | Product fails compliance due to bad traceability or missing tests | Critical | Failure to meet DO-178C or IEC 61508 guidelines  | Maintain traceability and perform compliance audits |

