The 3 Git States
Modified (Working Directory): This is your actual local workspace on your computer. When you open a file and make changes, add new lines of code, or delete something, the file is in the modified state. Git knows you changed it, but those changes aren't officially saved in your project history yet.

Staged (Staging Area / Index): Think of this as a preparation zone or a cargo dock. When you run git add <filename>, you are telling Git, "Hey, I want these specific changes to be part of my next snapshot." It allows you to select exactly which modifications you want to save, leaving out files you aren't ready to commit yet.

Committed (Local Repository): When you run git commit, Git takes everything you put into the staging area and permanently saves that snapshot to your local database (the .git folder). The data is now safely stored in your project's history with a unique ID


