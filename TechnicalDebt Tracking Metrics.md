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
