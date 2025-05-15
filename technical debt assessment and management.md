📝 Technical Debt Assessment Template

📄 Template 1: Debt Identification Worksheet

| **Component/Module** | **Type of Debt** | **Symptoms**                          | **Impact**                  | **Evidence**                    | **Owner** | **Date Identified** |
| -------------------- | ---------------- | ------------------------------------- | --------------------------- | ------------------------------- | --------- | ------------------- |
| UART Driver          | Code Complexity  | Nested conditionals, poor testability | High (delays updates)       | Code review, 15% coverage       | A. Kumar  | 2025-05-10          |
| Bootloader           | Update/Process   | No rollback, unclear update steps     | Critical (risk of bricking) | Bug reports, no version control | S. Mehta  | 2025-04-27          |

#### Debt Types:
- Code Complexity
- Documentation
- Build System
- Process/Release
- Testing
- Architecture

📊 Technical Debt Scoring Template

📄 Template 2: Technical Debt Scorecard

| **Metric**                | **Threshold** | **Actual** | **Risk Level** | **Notes**              |
| ------------------------- | ------------- | ---------- | -------------- | ---------------------- |
| Cyclomatic Complexity     | ≤ 10          | 17         | High           | Refactor needed        |
| Code Coverage             | ≥ 80%         | 48%        | Medium         | Increase unit tests    |
| Static Analysis Warnings  | ≤ 20          | 113        | High           | Use MISRA guidelines   |
| Time to Understand Module | ≤ 1 hr        | 3 hrs      | Medium         | Code readability issue |
| Bug Reopen Rate           | ≤ 5%          | 12%        | High           | Incomplete fixes       |

🛠️ Technical Debt Remediation Plan Template

📄 Template 3: Remediation Tracker

| **Debt Item**       | **Fix Plan**                             | **Priority** | **ETA**    | **Owner** | **Status**  |
| ------------------- | ---------------------------------------- | ------------ | ---------- | --------- | ----------- |
| Nested Logic in ISR | Move logic outside ISR, use event queue  | High         | 2025-06-01 | A. Kumar  | In Progress |
| Legacy Bootloader   | Add rollback, write update protocol spec | Critical     | 2025-06-15 | S. Mehta  | Planned     |
| Missing Tests       | Add unit tests for drivers               | Medium       | 2025-06-10 | R. Das    | Not Started |


