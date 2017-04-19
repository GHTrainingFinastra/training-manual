### Reset Mixed

Next we will try the default mode of reset, `reset --mixed`:

1. Once again, we will start by viewing the history of our project: `git log --oneline`
- Go back one commit in history: `git reset HEAD~`
- See where the tip of the branch is pointing: `git log --oneline --decorate`
- The changes we made in the last commit have been moved back to the working directory: `git status`
- Move the files to the staging area before we can commit them: `git add file5.md file6.md`
- Re-commit the files: `git commit -m "re-add file 5 and 6"`


> **Note:** Notice that although we have essentially made the exact same commit (adding file 5 and 6 together with the same HEAD and commit message) we still get a new commit ID. This can help us see why the reset command should never be used on commits that have been pushed to the remote.