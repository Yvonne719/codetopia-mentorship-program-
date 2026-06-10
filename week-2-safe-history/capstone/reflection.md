1. When should you use git restore?
Use git restore when you have made changes to a file in your working directory that you haven't committed yet and you want to discard them.

Scenario: You accidentally deleted a function or added "bad content" to first.md and want the file to return to its state as of the last commit.

Effect: It overwrites your current local changes with the "clean" version from the repository.

2. When should you use git restore --staged?
Use this when you have already run git add on a file, but you’ve changed your mind about including it in the next commit.

Scenario: You ran git add . but realized one of those files isn't ready to be saved yet.

Effect: it moves the file out of the Staging Area and back into your Working Directory. Your code doesn't change, but it's no longer "green" in git status.

3. Why is git revert safer than rewriting history?
git revert is safer because it does not change the past. Instead of deleting a bad commit from the timeline, it adds a new commit that undoes the changes.

Collaboration: If you are working on a team, rewriting history (like using reset) can break your teammates' local copies. Revert is a "safe" move because it moves the project forward linearly.

4. What is the difference between revert and reset?
git revert	Creates a new "undo" commit. The history grows longer, and nothing is deleted. Use this for pushed code whilst git reset moves branch pointer backward, effectively deleting commits from the timeline. Use this only for local, unpushed mistakes.

5. What mistake did you make and how did you recover?
In my practice session, I added "bad content" to my recipes.md file.

The Recovery: Since I hadn't committed the mistake yet, I used git restore first.md. This instantly wiped out the bad text and brought back the original version of my file. Later, when I accidentally made a "bad commit," I used git revert HEAD to create a fresh commit that canceled out the error without messing up my Git log.

6. Undo Tactics: Learning that there is a specific "undo" button for every stage of the Git process.