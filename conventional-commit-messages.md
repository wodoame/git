Conventional Commit messages are a standardized format for writing commit messages in software development. They make commit logs more readable and consistent, which is especially helpful in projects with many contributors or automated tools like changelogs or CI/CD pipelines.

Here's a detailed tutorial:

---

### **What Are Conventional Commits?**
Conventional Commits are a lightweight standard for commit message formatting. They provide a consistent structure that makes it easier to:
- Understand the purpose of a commit.
- Automate the generation of changelogs.
- Trigger semantic versioning (e.g., major, minor, or patch releases).
- Communicate changes effectively.

The format consists of:
1. **Type**: Describes the kind of change.
2. **Optional Scope**: Context of the change (e.g., a specific module or component).
3. **Subject**: A brief description of the change.
4. **Optional Body**: Additional details about the change.
5. **Optional Footer**: Notes like breaking changes or issue references.

---

### **The Basic Syntax**
```
<type>[optional scope]: <subject>
[optional body]

[optional footer]
```

#### **Example Commit Messages**
1. Adding a new feature:
   ```
   feat(auth): add support for two-factor authentication
   ```
2. Fixing a bug:
   ```
   fix(ui): resolve button alignment issue on mobile
   ```
3. Updating documentation:
   ```
   docs: update README with setup instructions
   ```

---

### **Commit Types**
Here are the most common types:

1. **feat**: A new feature.
   - Example: `feat: add user authentication module`

2. **fix**: A bug fix.
   - Example: `fix: correct typo in validation logic`

3. **docs**: Changes to documentation.
   - Example: `docs: add API usage examples to README`

4. **style**: Changes that don’t affect code logic, like formatting or linting.
   - Example: `style: fix indentation in main.js`

5. **refactor**: Code changes that neither fix a bug nor add a feature (e.g., improving code structure).
   - Example: `refactor: simplify user role validation logic`

6. **test**: Adding or updating tests.
   - Example: `test: add unit tests for auth middleware`

7. **chore**: Other changes that don’t modify `src` or `test` files, such as updating dependencies or build scripts.
   - Example: `chore: update dependency eslint to v7.32.0`

8. **perf**: Changes that improve performance.
   - Example: `perf: optimize image loading with lazy loading`

9. **build**: Changes that affect the build system or external dependencies.
   - Example: `build: configure webpack for production builds`

10. **ci**: Changes to CI configuration.
    - Example: `ci: add GitHub Actions workflow for testing`

---

### **Scopes**
The scope is optional but useful to clarify the area affected by the change. For instance, if your project has multiple modules, you can specify which part is affected.

#### Examples:
- `feat(ui): add dark mode toggle`
- `fix(auth): handle token expiration gracefully`

If the scope isn’t relevant, you can omit it:
- `docs: update CONTRIBUTING.md`

---

### **Subjects**
The subject should:
1. Be concise (50 characters or less).
2. Start with a lowercase letter (unless proper noun).
3. Avoid ending with a period.
4. Use an imperative tone, e.g., "add" instead of "added" or "adds".

#### Example:
- ✅ `feat: add search functionality`
- ❌ `feat: Added search functionality.`

---

### **Optional Body**
The body adds context or reasoning behind the change. Use it when the subject alone doesn’t tell the full story.

#### Example:
```
fix(auth): handle expired tokens

Previously, the system would crash when encountering an expired token. 
This fix ensures a proper error message is shown to the user instead.
```

---

### **Optional Footer**
The footer is used for:
1. Breaking changes.
2. Issue references.

#### Breaking Change Example:
```
feat(api): remove deprecated v1 endpoints

BREAKING CHANGE: The v1 endpoints are no longer supported. Clients must migrate to v2.
```

#### Issue Reference Example:
```
fix(ui): resolve dropdown alignment issue

Closes #1234
```

---

### **Advantages of Using Conventional Commits**
1. **Readability**: Commit logs are clear and consistent.
2. **Automation**:
   - Generate changelogs automatically.
   - Trigger version bumps in Semantic Versioning (e.g., `feat` for minor, `fix` for patch).
   - Enforce commit rules with linting tools like `commitlint`.
3. **Team Communication**: Makes it easier for team members to understand the purpose of each commit.

---

### **Tools for Conventional Commits**
- **Commitlint**: Enforce the format in your project.
- **Husky**: Automate commit message checks via Git hooks.
- **Standard Version**: Automate changelogs and versioning.

---
