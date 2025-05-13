Error:  ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/divineajaegbu4/web-development.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

solution
Note: This error means that your local main branch is behind the remote main branch — there are changes on GitHub that your local copy doesn’t have. So Git is rejecting your push to avoid overwriting remote changes.

You’ll need to resolve them manually, then commit and push.

Note: This will fetch and merge the remote changes into your local branch.
1. git pull origin main

Note: Then you can push again:
2. git push origin 

---------------------------------------------------------------------

solution:
Note: ❗ Alternative (Not recommended unless you're sure):
If you want to force your changes and overwrite remote history:

git push --force origin main

-------------------------------------------------------------------------

Error:  fatal: refusing to merge unrelated histories

Note: This error means Git thinks your local project and the remote repository have different, unrelated histories — often because:

You created a new project locally and a separate one remotely (e.g., both were initialized with separate git init).

You didn't clone the repo from GitHub but added it later with git remote add.

solution: Allow Git to merge unrelated histories

1. git pull origin main --allow-unrelated-histories
Note: Then resolve any merge conflicts if they appear.

2. git push origin main

Note: This tells Git: "Yes, I know the histories are different — merge them anyway."




