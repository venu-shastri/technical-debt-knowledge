### 📊 Technical Debt Tracking Metrics

| **Category**           | **Metric**                         | **Description**                                                                 | **Tools / Sources**                  |
|------------------------|------------------------------------|---------------------------------------------------------------------------------|--------------------------------------|
| **Code-Level**         | Cyclomatic Complexity              | Measures number of independent paths in the code.                              | SonarQube, ReSharper                 |
|                        | Cognitive Complexity               | Quantifies how difficult code is to understand.                                | SonarQube                            |
|                        | Code Churn                         | Frequency of changes to the same files.                                        | Git, CodeScene                       |
|                        | Technical Debt Ratio               | Debt as a percentage of total dev effort. (`Remediation / Dev Cost`)          | SonarQube                            |
|                        | Code Coverage                      | Percentage of code covered by automated tests.                                 | Coverlet, JaCoCo, dotCover           |
|                        | Code Duplication                   | Identifies repeated code blocks.                                               | SonarQube, ReSharper                 |
|                        | Static Code Analysis Warnings      | Number/severity of warnings (e.g., unused vars, null refs).                    | ESLint, SonarQube, FxCop             |
| **Team-Level**         | Developer Sentiment                | Subjective feedback via surveys or retros.                                     | Team surveys, anonymous forms        |
|                        | Lead Time for Changes              | Time from commit to production.                                                | JIRA, GitLab, GitHub Actions         |
|                        | Bug Reopen Rate                    | % of bugs that were fixed but reopened.                                        | JIRA, Azure DevOps                   |
|                        | Onboarding Time                    | Avg. time for new devs to become productive.                                   | Internal HR/PM records               |
|                        | Time Spent Troubleshooting         | Ratio of bug fixing/debugging vs feature work.                                 | Time-tracking, developer feedback    |
| **Strategic**          | Rework Percentage                  | Portion of work that is redone or discarded.                                   | JIRA, Git history                    |
|                        | Dependency Volatility              | Frequency and impact of dependency changes.                                    | Git logs, Dependency Trackers        |
|                        | Hotspot Analysis                   | Files with high complexity + frequent edits.                                   | CodeScene, Git data                  |


### 📊 Technical Debt Tracking Metrics (C / C++ Focus)

| **Category**           | **Metric**                         | **Description**                                                                 | **Tools / Sources (C/C++ Compatible)**           |
|------------------------|------------------------------------|---------------------------------------------------------------------------------|--------------------------------------------------|
| **Code-Level**         | Cyclomatic Complexity              | Measures number of independent paths in the code.                              | **CppDepend**, **Understand**, **SonarQube**     |
|                        | Cognitive Complexity               | Quantifies how difficult code is to understand.                                | **SonarQube**, **Understand**                    |
|                        | Code Churn                         | Frequency of changes to the same files.                                        | **Git**, **CodeScene**, **GitStats**             |
|                        | Technical Debt Ratio               | Debt as a percentage of total dev effort. (`Remediation / Dev Cost`)          | **SonarQube**, **CppDepend**                     |
|                        | Code Coverage                      | Percentage of code covered by automated tests.                                 | **gcov**, **lcov**, **LLVM’s Source-based Code Coverage** |
|                        | Code Duplication                   | Identifies repeated code blocks.                                               | **CPD (PMD)**, **SonarQube**                     |
|                        | Static Code Analysis Warnings      | Number/severity of warnings (e.g., null derefs, memory leaks).                | **Cppcheck**, **Clang-Tidy**, **PVS-Studio**, **Coverity** |
| **Team-Level**         | Developer Sentiment                | Subjective feedback via surveys or retros.                                     | **Custom surveys**, **Google Forms**, **Retrospective tools** |
|                        | Lead Time for Changes              | Time from commit to production.                                                | **JIRA**, **GitLab CI**, **GitHub Actions**, **Azure DevOps** |
|                        | Bug Reopen Rate                    | % of bugs that were fixed but reopened.                                        | **JIRA**, **Bugzilla**, **Redmine**              |
|                        | Onboarding Time                    | Avg. time for new devs to become productive.                                   | **Internal tracking**, **HR onboarding metrics** |
|                        | Time Spent Troubleshooting         | Ratio of bug fixing/debugging vs feature work.                                 | **Time-tracking tools**, **JIRA**, **Dev feedback** |
| **Strategic**          | Rework Percentage                  | Portion of work that is redone or discarded.                                   | **JIRA**, **Git history**, **Custom metrics**     |
|                        | Dependency Volatility              | Frequency and impact of dependency changes.                                    | **CMake**, **Conan**, **vcpkg**, **Git**         |
|                        | Hotspot Analysis                   | Files with high complexity + frequent edits.                                   | **CodeScene**, **CppDepend**, **Git**            |

🧰 Notable Tools Breakdown for C/C++:

| Tool           | Primary Use                                   |
| -------------- | --------------------------------------------- |
| **CppDepend**  | Static analysis, complexity, debt ratio       |
| **Understand** | Code comprehension, metrics, navigation       |
| **Clang-Tidy** | Linting and automated refactoring             |
| **Cppcheck**   | Lightweight static analysis                   |
| **PVS-Studio** | Deep static code analysis                     |
| **SonarQube**  | Code quality dashboard, integrates with C/C++ |
| **CodeScene**  | Hotspot detection and cognitive mapping       |
| **gcov/lcov**  | Test coverage for GCC-based toolchains        |
| **CPD (PMD)**  | Duplicate code detection                      |
| **Coverity**   | Enterprise static analysis (comprehensive)    |

📊 Technical Debt Tracking Metrics (Embedded Systems Focus)
| **Category**           | **Metric**                         | **Description**                                                                 | **Tools / Sources (Embedded Compatible)**        |
|------------------------|------------------------------------|---------------------------------------------------------------------------------|--------------------------------------------------|
| **Code-Level**         | Cyclomatic Complexity              | Measures the number of independent paths in code.                              | **LDRA**, **Understand**, **Polyspace**, **CppDepend** |
|                        | Cognitive Complexity               | Quantifies how hard code is to understand.                                     | **Understand**, **Polyspace**, **CodeSonar**     |
|                        | Code Churn                         | Identifies unstable files due to frequent changes.                             | **Git**, **CodeScene**, **GitStats**             |
|                        | Technical Debt Ratio               | Time required to fix all issues vs. new code cost.                             | **CppDepend**, **SonarQube Embedded plugins**    |
|                        | Code Coverage                      | Measures how much code is exercised by tests.                                  | **gcov**, **BullseyeCoverage**, **LDRA**, **Tessy** |
|                        | Code Duplication                   | Repeated code blocks that increase maintenance cost.                           | **CPD**, **Understand**, **SonarQube**           |
|                        | Static Code Analysis Warnings      | Detects bugs, memory leaks, undefined behavior.                                | **MISRA tools**: **PC-lint**, **Coverity**, **Polyspace**, **PVS-Studio**, **Klocwork** |
| **Team-Level**         | Developer Sentiment                | Subjective morale and friction due to tech debt.                               | **Anonymous surveys**, **Retrospective tools**   |
|                        | Lead Time for Changes              | Time from change request to deployed/tested firmware.                          | **JIRA**, **Azure DevOps**, **internal CI/CD logs** |
|                        | Bug Reopen Rate                    | Fixes that failed and were reopened.                                           | **JIRA**, **Bugzilla**, **Redmine**              |
|                        | Onboarding Time                    | Time for new devs to be productive in embedded stack.                          | **Internal tracking**, **Knowledge base**        |
|                        | Time Spent Troubleshooting         | Time in debugging hardware/software vs. feature delivery.                      | **Debug logs**, **Dev feedback**, **JIRA**        |
| **Strategic**          | Rework Percentage                  | Redone work due to unclear code or fragile systems.                            | **JIRA**, **Postmortems**, **Code review notes** |
|                        | Dependency Volatility              | Stability of firmware libraries, RTOS or HAL layers.                           | **Git**, **Vendor release logs**, **Change logs** |
|                        | Hotspot Analysis                   | Files with high complexity and frequent changes.                               | **CodeScene**, **CppDepend**, **Understand**     |

🧰 Recommended Tools for Embedded Technical Debt Tracking

| **Tool**                        | **Purpose**                                 | **Compliance**            |
| ------------------------------- | ------------------------------------------- | ------------------------- |
| **LDRA**                        | Code quality, coverage, and rule compliance | MISRA, DO-178C, ISO 26262 |
| **Polyspace**                   | Formal static analysis, runtime errors      | ISO 26262, IEC 61508      |
| **Understand**                  | Code metrics, navigation, call graphs       | General                   |
| **PC-lint Plus**                | MISRA-C, code quality                       | MISRA, AUTOSAR            |
| **Klocwork**                    | Security, bugs, rule violations             | CWE, MISRA, CERT          |
| **Coverity**                    | Advanced static analysis, defect detection  | ISO 26262, IEC 61508      |
| **PVS-Studio**                  | MISRA + general C/C++ error detection       | MISRA, AUTOSAR            |
| **BullseyeCoverage**, **Tessy** | Coverage for safety-critical systems        | ISO 26262, DO-178C        |
| **CodeScene**                   | Hotspot and social debt analysis            | General                   |
