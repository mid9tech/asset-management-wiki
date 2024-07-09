## Commit Conventions

**Format:** `<type>(<scope>): <subject>`

### Type:
- **feat:** A new feature.
- **docs:** Documentation only changes.
- **style:** Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc).
- **refactor:** A code change that neither fixes a bug nor adds a feature.
- **perf:** A code change that improves performance.
- **test:** Adding missing or correcting existing tests.
- **build:** Changes that affect the build system or external dependencies (example scopes: pip, docker, npm).
- **ci:** Changes to CI configuration files and scripts (example scopes: GitLabCI).

### Scope:
Field should be a noun that represents the part of the codebase affected by the commit.

### Subject:
Brief description of the commit.

### Example: feat(user-profile): add avatar upload functionality

---
## Branch Naming Convention

### Feature Branches:
Use the prefix `feature/` followed by a brief, descriptive name of the feature or user story (e.g., `feature/user-authentication`).

### Bugfix Branches:
Use the prefix `bugfix/` followed by a brief, descriptive name of the bug or issue being fixed (e.g., `bugfix/login-error-handling`).

### Hotfix Branches:
Use the prefix `hotfix/` followed by a brief, descriptive name of the urgent issue or hotfix (e.g., `hotfix/security-patch`).

### Release Branches:
Use the prefix `release/` followed by the version number or release name (e.g., `release/v1.0.0`, `release/summer-update`).

### Example:
- **Feature Branch:**
  - `feature/user-authentication`
  
- **Bugfix Branch:**
  - `bugfix/login-error-handling`
  
- **Hotfix Branch:**
  - `hotfix/security-patch`
  
- **Release Branch:**
  - `release/v1.0.0`

