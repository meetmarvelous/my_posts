1. `git push`:
   - This command is used to upload local branch commits to a remote repository.
   - If you have previously set up a tracking branch for the current local branch, the `git push` command will push your commits to that tracking branch on the remote repository.
   - If you haven't set up a tracking branch, you need to specify the remote repository and the branch to push to.

2. `git push -u`:
   - The `-u` option stands for "upstream."
   - This command sets up a tracking relationship between the local branch and the specified remote branch.
   - It is typically used for the initial push of a local branch to a remote repository.
   - After using `git push -u`, subsequent invocations of `git push` without any additional arguments will push to the same remote branch.

3. `git push origin main`:
   - This command pushes the local branch named `main` to the remote repository called `origin`.
   - `origin` is the default name often given to the remote repository that your local repository was cloned from.
   - `main` refers to the branch name you want to push to the remote repository.

To summarize, `git push` is used to push commits to a remote repository, `git push -u` is used to set up a tracking relationship for the current branch, and `git push origin main` is used to push the local branch named `main` to the remote repository called `origin`.
