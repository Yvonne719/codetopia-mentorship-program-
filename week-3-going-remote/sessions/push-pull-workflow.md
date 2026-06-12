**git remote add origin**

Purpose: Links your local repo to a remote repository under the name "origin", so you can push/pull without typing the full URL each time.

Syntax: `git remote add <name> <url>`

Example: `git remote add origin git@github.com:Edwardasar/capstone-1.git`

Expected outcome: No output on success. Running `git remote -v` afterward shows `origin` pointing to that URL for both fetch and push.

**git push -u origin main**

Purpose: Uploads your local `main` branch commits to the `origin` remote, and sets up tracking so future `git push`/`git pull` on this branch don't need the remote/branch specified.

Syntax: `git push -u <remote> <branch>` (`-u` = `--set-upstream`)

Example: `git push -u origin main`

Expected outcome: Git uploads commits and creates `main` on the remote if it doesn't exist. Output shows branches being set up to track `origin/main`. After this, plain `git push` and `git pull` work without arguments.

**git pull origin main**

Purpose: Fetches commits from the `main` branch on `origin` and merges them into your current local branch, updating it with changes others have pushed.

Syntax: `git pull <remote> <branch>`

Example: `git pull origin main`

Expected outcome: Git downloads new commits from the remote `main` and merges them into your local branch. If there are no conflicts, you'll see a summary of changed files; if your local branch has diverging changes, Git may create a merge commit or report conflicts to resolve.