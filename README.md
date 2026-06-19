# Git-Advanced-Exercises
Getting started
Part 1: Refining Git History (10 Challenges)
Missing File Fix

```bash
Nettie King@Nettie-Win MINGW64 ~
$ git clone https://github.com/FaridaKINGUELEOUA/Git-Advanced-Exercises.git
Cloning into 'Git-Advanced-Exercises'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (3/3), done.

Nettie King@Nettie-Win MINGW64 ~
$ cd Git-Advanced-Exercises

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ touch test{1..4}.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git add test1.md && git commit -m "chore: Create initial file"
[main 496b9f0] chore: Create initial file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git add test2.md && git commit -m "chore: Create another file"
[main 0a85d1c] chore: Create another file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git add test3.md && git commit -m "chore: Create third and fourth files"
[main 3a1a281] chore: Create third and fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git log
commit 3a1a2814790de817592d17d5b8b8afb5d6e568b0 (HEAD -> ma
commit 3a1a2814790de817592d17d5b8b8afb5d6e568b0 (HEAD -> main)
Author: Nettie Farida <fanekingue@gmail.com>
Date:   Fri Jun 19 15:00:03 2026 +0200

    chore: Create third and fourth files

commit 0a85d1c99873edb70c2105dffcbb81c51480dbb0
Author: Nettie Farida <fanekingue@gmail.com>
Date:   Fri Jun 19 14:59:53 2026 +0200

    chore: Create another file

commit 496b9f04ef188cd4f66448ca9053250d94d48436
Author: Nettie Farida <fanekingue@gmail.com>
Date:   Fri Jun 19 14:59:43 2026 +0200

    chore: Create initial file

commit 07725c610de1c1568ce2363bf49405d70a099bce (origin/mai
n, origin/HEAD)
Author: FaridaKINGUELEOUA <fanekingue@gmail.com>
Date:   Fri Jun 19 14:52:27 2026 +0200

    Initial commit
(END)
Date:   Fri Jun 19 14:59:43 2026 +0200

    chore: Create initial file

commit 07725c610de1c1568ce2363bf49405d70a099bce (origin/main, origin/HEAD)
Author: FaridaKINGUELEOUA <fanekingue@gmail.com>
Date:   Fri Jun 19 14:52:27 2026 +0200
```

    Initial commit
~
(END)
