Feature branch naming in Git should be consistent, descriptive, and follow a standard naming convention to ensure clarity and collaboration among team members. Here are some common best practices for naming feature branches:

### General Format
1. **Prefix**: Indicate the branch type (e.g., `feature`, `fix`, `chore`, etc.).
2. **Brief Description**: Describe the feature or task in a concise, kebab-case format (lowercase, hyphen-separated words).
3. **Optional Issue Identifier**: Include the issue or ticket number from your project management tool (e.g., Jira, GitHub Issues).

### Example Formats
- **With Prefix Only**:
  ```
  feature/add-login-page
  fix/correct-footer-links
  chore/update-readme
  ```
- **With Issue Identifier**:
  ```
  feature/123-add-login-page
  fix/456-correct-footer-links
  chore/789-update-readme
  ```

### Naming Guidelines
1. **Use Lowercase and Hyphens**:
   - Avoid spaces or underscores.
   - Example: `feature/add-api-endpoint`.

2. **Be Descriptive**:
   - Clearly describe the purpose of the branch.
   - Bad: `feature/branch1`.
   - Good: `feature/user-authentication`.

3. **Keep it Short but Meaningful**:
   - Focus on the core purpose of the branch.

4. **Use a Prefix System**:
   - `feature/` for new features.
   - `fix/` for bug fixes.
   - `hotfix/` for urgent production issues.
   - `chore/` for tasks like documentation or refactoring.
   - `test/` for testing or experimentation.

5. **Sync with Your Workflow**:
   - Align branch names with your project management system's workflow (e.g., linking with ticket numbers).

### Real-World Examples
- Adding a new feature:
  ```
  feature/123-create-user-dashboard
  ```
- Fixing a bug:
  ```
  fix/456-resolve-navbar-overlap
  ```
- Refactoring code:
  ```
  chore/refactor-authentication-module
  ```
