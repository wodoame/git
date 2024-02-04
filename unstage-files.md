In Git, to unstage files that you have previously staged for a commit, you can use the `git reset` command. Here are the steps:

1. Open a terminal or command prompt.

2. Navigate to the root directory of your Git repository using the `cd` command.

3. Use the following command to unstage files:

   ```bash
   git reset <file(s)>
   ```

   Replace `<file(s)>` with the name of the file or files you want to unstage. If you want to unstage all files, you can use:

   ```bash
   git reset
   ```

   This command will unstage the specified file(s), and the changes will be moved back to the working directory.

4. Optionally, you can use `git status` to check the status of your working directory. The files should now be listed as "unstaged changes."

If you also want to discard the changes in the working directory and revert to the last committed state, you can use `git checkout`:

```bash
git checkout -- <file(s)>
```

Again, replace `<file(s)>` with the name of the file or files you want to revert. Be cautious when using `git checkout` as it discards the changes in your working directory.

Remember to use these commands carefully, especially when dealing with unstaging or discarding changes, as it could result in data loss.
