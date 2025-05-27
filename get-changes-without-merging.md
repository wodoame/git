It is possible to get someone’s changes in Git without merging them. You can do this by **fetching** their branch and then **checking it out** or **cherry-picking** specific commits.

**Options:**

1. **Fetch and checkout their branch (no merge to your branch):**
   ```sh
   git fetch origin their-branch
   git checkout their-branch
   ```
   This puts you on their branch, but does not merge it into yours.

2. **Cherry-pick specific commits:**
   ```sh
   git fetch origin their-branch
   git cherry-pick <commit-hash>
   ```
   This applies only the selected commit(s) to your branch.

3. **View their changes without merging:**
   ```sh
   git fetch origin their-branch
   git diff origin/their-branch
   ```
   This shows the differences without applying them.

You only merge if you use `git merge`. Fetching, checking out, or cherry-picking does not merge by default.


This **does apply to forks**, but with a small difference:  
You need to add the fork as a remote first.

**Example:**

1. **Add the fork as a remote:**
   ```sh
   git remote add theirfork https://github.com/theirusername/theirrepo.git
   ```

2. **Fetch their branch:**
   ```sh
   git fetch theirfork their-branch
   ```

3. **View, checkout, or cherry-pick as before:**
   - View changes:
     ```sh
     git diff theirfork/their-branch
     ```
   - Checkout:
     ```sh
     git checkout theirfork/their-branch
     ```
   - Cherry-pick:
     ```sh
     git cherry-pick <commit-hash>
     ```

So, you can get changes from a fork without merging, just like with branches in the same repo.
