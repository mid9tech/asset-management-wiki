## Pull Request (PR) Description Convention

### Title:
- Begin with a clear and concise title that summarizes the purpose of the pull request. Use imperative mood (e.g., "Add feature X", "Fix issue Y").

### Description:
- Provide a detailed description of what changes were made and why. Include relevant context, such as related issues or user stories.
- Describe any technical decisions or considerations made during implementation.
- Mention if there are any breaking changes or dependencies that reviewers should be aware of.

### Checklist:
- **Testing:** Outline the testing strategy used to verify the changes (e.g., unit tests, integration tests).
- **Documentation:** Describe any updates made to documentation (e.g., README files, API documentation).
- **Reviewers:** Tag specific team members or reviewers who should review the code changes.
- **Deployment Notes:** Provide instructions or notes related to deployment, if applicable.
- **Additional Notes:** Include any additional information or context that might be helpful for reviewers or stakeholders.

### Review Guidelines:
- Specify specific areas of focus for reviewers (e.g., performance, security, UX).
- Provide guidance on how to test and validate the changes locally or in a staging environment.
- Encourage constructive feedback and collaboration among team members.

### Completion Criteria:
- Define the criteria that need to be met before the pull request can be merged (e.g., all tests passing, approval from at least two reviewers).

### Closing Issues:
- If this PR resolves or relates to any GitHub issues, mention them using keywords like "Closes #123" or "Fixes #456".

### Example:
- **Title:**
  - Add user authentication feature

- **Description:**
  - Implemented user authentication using JWT tokens for secure access.
  - Integrated with existing user management system.
  - Updated login and registration screens to accommodate new authentication flow.
  - Resolves #123, #124.

- **Checklist:**
  - **Testing:** Unit tests added for authentication service.
  - **Documentation:** Updated README with new authentication setup instructions.
  - **Reviewers:** @developer1, @developer2
  - **Deployment Notes:** Requires database migration script.
  - **Additional Notes:** Ensure backward compatibility with existing user sessions.

- **Review Guidelines:**
  - Focus on security aspects of JWT implementation.
  - Test login and registration flows with different user roles.
  - Deploy to staging environment for end-to-end testing.

- **Completion Criteria:**
  - All tests passing on CI/CD pipeline.
  - Approval from both reviewers (@developer1, @developer2).
