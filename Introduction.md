## 1. INTRODUCTION TO TECHNICAL DEBT

### Definition and Concept

- **What is Technical Debt?**

  - A metaphor introduced by Ward Cunningham to describe the trade-off between short-term gains and long-term code quality.
  - Accumulated consequences of quick-and-dirty solutions.

- **Types of Technical Debt:**

  - **Code Debt** – Poor code structure, duplicated code.
  - **Design Debt** – Poor architectural decisions, anti-patterns.
  - **Documentation Debt** – Lack of or outdated documentation.
  - **Testing Debt** – Inadequate or missing tests.
  - **Build Debt** – Fragile build systems, outdated dependencies.

  ##### Examples of Technical Debt Types

  | Type of Technical Debt    | Example                                                      | Impact                                                       |
  | ------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
  | **Code Debt**             | Duplicated code blocks instead of reusable functions         | Increases maintenance effort, higher risk of inconsistent bug fixes |
  | **Design Debt**           | Using monolithic architecture when microservices are more appropriate | Hinders scalability and flexibility                          |
  | **Documentation Debt**    | Missing or outdated API documentation                        | Slows onboarding, increases misuse of code                   |
  | **Testing Debt**          | Lack of unit tests for critical business logic               | Makes refactoring risky, increases bug occurrence            |
  | **Build/Dependency Debt** | Relying on outdated or deprecated third-party libraries      | Introduces security risks, blocks upgrades                   |
  | **Infrastructure Debt**   | Manual deployment instead of automated CI/CD pipelines       | Error-prone processes, slow release cycles                   |
  | **UX/UI Debt**            | Interfaces not accessible for screen readers or keyboard navigation | Excludes users with disabilities, violates accessibility standards |
  | **Security Debt**         | Storing user passwords in plaintext                          | High risk of data breach, legal and compliance issues        |

  """
