Stashing in Git is like putting your current, incomplete work on hold temporarily so you can work on something else without losing your progress. Here's how it works:

### What is Git Stash?
When you're working on a feature or fixing a bug, you might not be ready to commit your changes yet, but you need to switch to another branch or pull in changes from a remote repository. Stashing saves your current changes (modified and staged files) in a stack-like structure, allowing you to restore them later.

### Common Git Stash Commands
1. **Save changes to stash**:
   ```bash
   git stash
   ```
   This saves your changes and restores your working directory to the state of the last commit.

   - Optionally, you can include a message:
     ```bash
     git stash push -m "Work in progress on feature X"
     ```

2. **View stash list**:
   ```bash
   git stash list
   ```
   This displays all the stashed changes as a list. Each stash is identified by an index like `stash@{0}`, along with your message (if provided).

3. **Apply stashed changes**:
   ```bash
   git stash apply
   ```
   This restores the latest stashed changes without removing them from the stash.

   - If you want to apply a specific stash, use:
     ```bash
     git stash apply stash@{n}
     ```

4. **Remove stashed changes after applying**:
   ```bash
   git stash pop
   ```
   This restores the latest stashed changes and removes them from the stash.

5. **Delete a stash**:
   ```bash
   git stash drop stash@{n}
   ```
   Deletes a specific stash.

   - To clear all stashes:
     ```bash
     git stash clear
     ```

### Key Points
- **Staging vs. Working Directory**: Git stashes both staged (files added with `git add`) and unstaged changes, but it does not stash untracked files by default.
- **Include Untracked Files**: To stash untracked files as well:
  ```bash
  git stash -u
  ```
- **Conflict Handling**: Applying or popping a stash might result in merge conflicts. Resolve them as you would during a merge.

### When to Use Git Stash
- Switching branches while keeping incomplete work.
- Testing something in a clean working directory.
- Pulling the latest changes from the remote before resuming your current work.
