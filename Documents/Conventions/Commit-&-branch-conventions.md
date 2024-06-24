# **Commit & branch conventions**
**3.	Commit Conventions**
Format: <type>(<scope>): <subject>
-	Type:
•	feat: A new feature.
•	docs: Documentation only changes.
•	style: Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc).
•	refactor: A code change that neither fixes a bug nor adds a feature.
•	perf: A code change that improves performance.
•	test: Adding missing or correcting existing tests.
•	build: Changes that affect the build system or external dependencies (example scopes: pip, docker, npm).
•	ci: Changes to CI configuration files and scripts (example scopes: GitLabCI).
-	Scope: Field should be a noun that represents the part of the codebase affected by the commit.
-	Subject: Brief description of the commit.
Example: feat(user-profile): add avatar upload functionality
4. Branch 
- The branch in GitHub will be named according to the user story.
