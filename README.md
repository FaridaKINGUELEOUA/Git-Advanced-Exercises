# Git-Advanced-Exercises
Getting started
Part 1: Refining Git History (10 Challenges)
1.Missing File Fix

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
    Initial commit
~
(END)
Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git add test4.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git commit --amend -m "chore:Create third and fourth files"
[main f19fa6a] chore:Create third and fourth files
 Date: Fri Jun 19 15:00:03 2026 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$
2. Editing commit history
Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git add test4.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git commit --amend -m "chore:Create third and fourth files"
[main f19fa6a] chore:Create third and fourth files
 Date: Fri Jun 19 15:00:03 2026 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

 3.Squashing Commits
Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git log --oneline
f19fa6a (HEAD -> main) chore:Create third and fourth files
0a85d1c chore: Create another file
496b9f0 chore: Create initial file
07725c6 (origin/main, origin/HEAD) Initial commit

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git rebase -i HEAD~2
[detached HEAD df08c19] chore: Create a second file
 Date: Fri Jun 19 14:59:53 2026 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git rebase -i HEAD~3
[detached HEAD bd3e666] chore: Create initial and second files
 Date: Fri Jun 19 14:59:43 2026 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git log --oneline
c61fa9c (HEAD -> main) chore:Create third and fourth files
bd3e666 chore: Create initial and second files
07725c6 (origin/main, origin/HEAD) Initial commit

4. Splitting a commit
Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git reset --soft HEAD~1

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git reset

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git add test3.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git commit -m "Create third file"
[main cf1960f] Create third file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git add test4.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git commit -m "Create fourth file"
[main d2130ff] Create fourth file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git log --oneline
d2130ff (HEAD -> main) Create fourth file
cf1960f Create third file
bd3e666 chore: Create initial and second files
07725c6 (origin/main, origin/HEAD) Initial commit
```
