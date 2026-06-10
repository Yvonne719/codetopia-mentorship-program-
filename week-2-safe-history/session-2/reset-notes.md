Soft Reset
A Soft Reset is the least destructive way to undo a commit. It moves the HEAD pointer back to a specific commit in history, but it leaves your files exactly as they are.

Differences between soft reset, mixed reset and hard reset

| Command      | Description |
| ----------- | ----------- |
| git reset --soft      | Moves HEAD back to the specified commit. Keeps both your Staging Area and Working Directory intact. Changes remain green in git status.       |
| git reset --mixed   | The default setting. Moves HEAD back and clears the Staging Area, but leaves your Working Directory untouched. Changes remain in your files but turn red in git status.        |
| git reset --hard | The destructive option. Moves HEAD back, clears the Staging Area, and completely overwrites your Working Directory. Any uncommitted code is permanently deleted. |