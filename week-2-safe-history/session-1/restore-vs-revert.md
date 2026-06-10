| Command | Change History | Safe For Shared Repo | Typical Use Case |
| :--- | :--- | :--- | :--- |
| `git restore` | No | Yes | Discarding local, uncommitted experimental changes in a file. |
| `git restore --staged` | No | Yes | Accidentally running `git add` on a file you aren't ready to commit yet. |
| `git revert` | Yes | Yes | Undoing a bug introduced in a previous commit that has already been pushed. |
| `git reset --soft` | Yes | No | Undoing a commit to fix the commit message or combine it with more changes. |