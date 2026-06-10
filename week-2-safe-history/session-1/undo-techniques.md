git restore 

Purpose
This command is used to undo uncommitted changes in your working directory. It essentially "restores" a file to the state it was in at the time of your last commit.

When to use it
Use this when you’ve been hacking away at a file, realized you’ve made a mess, and want to discard all those local changes to start over from the last saved state.

git restore --staged
Purpose
This specific flag targets the Staging Area (the Index). It "unstages" a file without altering the actual code changes within that file.

When to use it
Use this when you accidentally ran git add . or git add <file>, but you aren't actually ready to commit that specific file yet. It pulls the file back out of the "waiting room" for the next commit.

git revert
Purpose
Unlike the other commands, git revert is for committed changes. It creates a new commit that does the exact opposite of a previous commit, effectively "canceling it out."

When to use it
Use this when you have already pushed changes to a shared repository (like GitHub) and realize a previous commit was a mistake. Since it doesn't delete history, it is the safest way to undo changes in a team environment.

git reset --soft
Purpose
This command moves your HEAD (the pointer to your current branch) back to a previous commit, but it keeps your changes in the staging area.

When to use it
Use this when you want to "undo" your last few commits to combine them into one, or if you committed too early and want to add more changes to that same commit. It effectively turns back the clock while keeping your work staged and ready.