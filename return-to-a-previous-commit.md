To go back to a previous commit in Git, you can use either the `git reset` or `git revert` command, depending on your needs. Here’s a quick overview of both methods:

### Using `git reset`
This command moves the current branch to the specified commit. It can be used in three modes: `--soft`, `--mixed`, and `--hard`.

1. **Find the commit hash**:
   ```bash
   git log --oneline
   ```
   This will list all commits with their hashes.

2. **Reset to the desired commit**:
   ```bash
   git reset --hard <commit-hash>
   ```
   Replace `<commit-hash>` with the hash of the commit you want to go back to. The `--hard` option will reset your working directory and staging area to match the specified commit.

   **Note**: Be cautious with `--hard` as it will discard all changes after the specified commit.

### Using `git revert`
This command creates a new commit that undoes the changes from a previous commit.

1. **Find the commit hash**:
   ```bash
   git log --oneline
   ```

2. **Revert the commit**:
   ```bash
   git revert <commit-hash>
   ```
   Replace `<commit-hash>` with the hash of the commit you want to revert. This will create a new commit that reverses the changes made by the specified commit.

### Example
If you want to reset to a commit with hash `abc123`:
```bash
git reset --hard abc123
```

Or if you want to revert the changes made by commit `abc123`:
```bash
git revert abc123
```
