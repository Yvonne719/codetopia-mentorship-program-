Why do remote repositories matter?
They give you a backup off your machine, let multiple people collaborate on the same codebase, and serve as the single source of truth everyone syncs with. Without one, your work exists only on one computer and no one else can access or contribute to it.

What does the -u flag do?
It sets up "upstream tracking" — linking your local branch (e.g. main) to a specific branch on the remote (origin/main). Once set, you can run git push and git pull without specifying the remote/branch names, since Git remembers the link.

How do local and remote repositories stay synchronized?
Through push (send local commits to remote) and pull (fetch remote commits and merge into local). They don't sync automatically — sync only happens when you explicitly run these commands. This means it's normal for local and remote to be temporarily out of sync until someone pushes or pulls.

What challenges I faced?
Forgetting -u and having to specify remote/branch every time i made a push.

What I leart this week?
How git remote works.