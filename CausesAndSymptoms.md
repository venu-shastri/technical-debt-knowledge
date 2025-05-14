## Causes and Symptoms
- **Common Causes:**
  - Time constraints and deadlines.
  - Evolving product requirements.
  - Lack of domain knowledge.
  - Inadequate tools or team skills.

- **Symptoms and Indicators:**
  - Frequent bugs and regressions.
  - High onboarding time for new developers.
  - Low test coverage.
  - Poor performance and scalability issues.

 ### Realistic Scenarios 
 Causes of Technical Debt
These are the reasons technical debt happens—some intentional, some accidental.

1. Time Constraints
Developers cut corners to meet a deadline.

Scenario:
A startup rushes to release a minimum viable product (MVP). To ship fast, the team skips writing tests and hardcodes several values. While it helps hit the release date, it builds debt.

🧠 "We'll clean it up later."

2. Lack of Knowledge
Teams make poor decisions because they don’t fully understand the system or tools.

Scenario:
A junior developer writes inefficient SQL queries without indexing because they aren’t aware of query optimization. The system slows down under load later.

🧠 "We didn’t know better at the time."

3. Evolving Requirements
The business changes direction, making previous code obsolete or incompatible.

Scenario:
An e-commerce app initially uses a flat pricing model, but the business later introduces tiered and promotional pricing. The original code doesn’t support this, causing code hacks and workarounds.

🧠 "We designed it for yesterday’s rules."

4. Inadequate Processes or Standards
No proper code review, testing, or documentation standards in place.

Scenario:
Developers push code directly to production without reviews or automated tests. Over time, the system becomes fragile and hard to maintain.

🧠 "Nobody's watching the gate."

5. Poor Communication
Teams aren’t aligned on architecture, design patterns, or best practices.

Scenario:
Frontend and backend teams build APIs without consulting each other. Integration becomes difficult, and they patch things last minute.

🧠 "We weren’t on the same page."

6. Lack of Refactoring
Teams focus only on adding features, not cleaning up.

Scenario:
Old functions are reused without updating them, resulting in bloated, unreadable code.

🧠 "If it works, don’t touch it."

🧩 Symptoms of Technical Debt
These are the signs that technical debt exists in your project.

1. Frequent Bugs and Breakages
Small code changes cause unrelated parts of the system to fail.

Scenario:
A fix to the login flow accidentally breaks the user profile update. Developers lack confidence in the code.

🚨 Symptom of tightly coupled or fragile code.

2. Slow Onboarding of New Developers
New team members struggle to understand the system.

Scenario:
It takes a new developer weeks to contribute because there's no documentation and the code is hard to read.

🚨 Symptom of undocumented, complex codebase.

3. Low Test Coverage
There are few or no automated tests in place.

Scenario:
The team fears deploying changes on Friday because the testing is mostly manual or non-existent.

🚨 Symptom of testing debt.

4. Repeated Fixes in the Same Area
Same bugs or crashes happen in the same module repeatedly.

Scenario:
The payment gateway module breaks every other sprint, and developers keep “patching” instead of fixing the root cause.

🚨 Symptom of neglected refactoring or design debt.

5. Slow Development Velocity
Features take longer and longer to implement.

Scenario:
Adding a small feature like "add coupon code" takes weeks due to complex interdependencies.

🚨 Symptom of poor architecture or spaghetti code.

6. Hard-to-Understand Code
Code lacks naming conventions, comments, or structure.

Scenario:
A function named doItAll() spans 300 lines and touches multiple subsystems.

🚨 Symptom of code and documentation debt.

✅ Summary Table

| Cause                 | Description                                     | Real-world Scenario                                    |
| --------------------- | ----------------------------------------------- | ------------------------------------------------------ |
| Time Constraints      | Rushing to deliver features                     | Skipping tests to meet a launch deadline               |
| Lack of Knowledge     | Inexperience or unfamiliarity                   | Inefficient database queries                           |
| Evolving Requirements | System no longer matches business needs         | Rewriting pricing logic due to policy changes          |
| Inadequate Processes  | No reviews, testing, or documentation standards | Bugs in production from untested features              |
| Poor Communication    | Teams working in silos                          | API integration problems due to lack of coordination   |
| Lack of Refactoring   | Continuous feature development without cleanup  | Accumulation of legacy code that no one wants to touch |

