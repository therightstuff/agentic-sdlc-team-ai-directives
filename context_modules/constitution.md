# Team Constitution

1. **Human Oversight Is Mandatory**
   Every autonomous contribution must receive human review before merge. Agents operate within guardrails; engineers are accountable for final outcomes.

2. **Build for Observability and Reproducibility**
   All features must include logging, metrics, and deterministic workflows so issues can be traced quickly.

3. **Security by Default**
   Follow least privilege for credentials, validate all inputs, and prefer managed secrets. Never ship hard-coded tokens.

4. **Tests Drive Confidence**
   Write automated tests before or alongside new logic. Refuse to ship when critical coverage is missing.

5. **Documentation Matters**
   Capture assumptions, API contracts, and hand-off notes in the repo. Agents and humans rely on clear context to move fast safely.

6. **Stateless Services**
   All services should be designed to be stateless, meaning they do not maintain any internal state between requests. This ensures scalability, reliability, and ease of deployment in cloud environments. State should be externalized to databases or caches as needed.

7. **Zero Trust Security Model**
    Adopt a zero trust approach where no entity is trusted by default, even if it's inside the network perimeter. Always verify and authenticate every request, implement least privilege access, and continuously monitor for threats.

8. **Think Before Coding**
    Don't assume. Don't hide confusion. Surface tradeoffs. State assumptions explicitly—if uncertain, ask rather than guess. Present multiple interpretations when ambiguity exists. Push back when warranted if a simpler approach is available. Stop when confused and name what's unclear.

9. **Simplicity First**
    Minimum code that solves the problem. Nothing speculative. No features beyond what was asked, no abstractions for single-use code, no "flexibility" that wasn't requested, no error handling for impossible scenarios. If 200 lines could be 50, rewrite it. Every senior engineer should agree the solution is not overcomplicated.

10. **Surgical Changes**
    Touch only what you must. Clean up only your own mess. When editing existing code, don't "improve" adjacent code, comments, or formatting. Don't refactor things that aren't broken. Match existing style, even if you'd do it differently. Remove imports/variables/functions that YOUR changes made unused, but don't remove pre-existing dead code unless asked.

11. **Goal-Driven Execution**
    Define success criteria. Loop until verified. Transform imperative tasks into verifiable goals with clear success metrics. For multi-step tasks, state a brief plan with what each step accomplishes and how to verify it. Strong success criteria enable autonomous looping; weak criteria require constant clarification.

## AI Context

1. To verify changes locally, run `npm run synth`.
2. Never deploy autonomously; always ask for human deployment after verification.

## Priorities

1. Ensure code is human readable and maintainable. Simplicity is king.
2. Ensure code is well-documented, with clear comments explaining non-obvious logic.
3. Ensure performance is acceptable, but do not prematurely optimize.
4. Use the smallest number of dependencies necessary to accomplish the task.
5. Separate concerns appropriately, following best practices for modularity and single responsibility.
6. Ensure proper error handling and logging are in place.
7. Be consistent with existing code style and conventions used in the codebase. Pay attention to linter warnings and problems identified by SonarQube.
8. Use meaningful variable and function names that accurately describe their purpose.

## Security

1. Ensure all user inputs are properly validated and sanitized to prevent vulnerabilities such as SQL injection, XSS, and other common attacks.
2. Ensure security best practices are followed, especially regarding user data and authentication.
3. Ensure accessibility standards are met to provide a good experience for all users.
4. Avoid introducing SonarQube issues, especially critical and high severity findings.

## Constraints

1. Do not introduce breaking changes to existing functionality.
2. Do not touch anything outside the scope of the requested changes.
