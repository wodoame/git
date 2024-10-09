You can retrieve a deleted branch in Git using the `git reflog` command. Here’s how you can do it:

1. **Find the commit hash of the deleted branch**:
   ```bash
   git reflog
   ```
   This command shows a log of all changes to the repository, including the deleted branch. Look for the commit hash associated with the branch you deleted.

2. **Create a new branch from that commit**:
   ```bash
   git checkout -b <new-branch-name> <commit-hash>
   ```
   Replace `<new-branch-name>` with the name you want to give to the restored branch and `<commit-hash>` with the hash you found in the previous step.

### Example
If the commit hash of the deleted branch is `abc123`, you can restore it like this:
```bash
git checkout -b restored-branch abc123
```

This will create a new branch named `restored-branch` starting from the commit `abc123`.
