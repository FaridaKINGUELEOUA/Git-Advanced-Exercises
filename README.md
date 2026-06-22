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

5. Advanced Squashing
Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git rebase -i HEAD~2
[detached HEAD eae3eed] Create third and fourth files
 Date: Fri Jun 19 15:38:06 2026 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md
Successfully rebased and updated refs/heads/main.

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git log --oneline
eae3eed (HEAD -> main) Create third and fourth files
bd3e666 chore: Create initial and second files
07725c6 (origin/main, origin/HEAD) Initial commit

6. Dropping commits
Nettie King@Nettie-Win MINGW64 ~
$ cd Git-Advanced-Exercises

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ touch unwanted.txt

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ echo "Some content" > unwanted.txt

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git add unwanted.txt
warning: in the working copy of 'unwanted.txt', LF will be replaced by CRLF the next time Git touches it

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git commit -m "Unwanted commit"
[main ef6a0a7] Unwanted commit
 1 file changed, 1 insertion(+)
 create mode 100644 unwanted.txt

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git log --oneline
ef6a0a7 (HEAD -> main) Unwanted commit
eae3eed Create third and fourth files
bd3e666 chore: Create initial and second files
07725c6 (origin/main, origin/HEAD) Initial commit

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git rebase -i HEAD~1
Successfully rebased and updated refs/heads/main.

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git log --oneline
eae3eed (HEAD -> main) Create third and fourth files
bd3e666 chore: Create initial and second files
07725c6 (origin/main, origin/HEAD) Initial commit

7. Reordering commits history
Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git rebase -i HEAD~2
Successfully rebased and updated refs/heads/main.

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git log
commit 1a6cdf5540e71b155fc8c1da683fd20332d00389 (HEAD -> main)
Author: Nettie Farida <fanekingue@gmail.com>
Date:   Fri Jun 19 14:59:43 2026 +0200

    chore: Create initial and second files

commit 1e55bc41c74edbd562576543d6beb5bb253f35ba
Author: Nettie Farida <fanekingue@gmail.com>
Date:   Fri Jun 19 15:38:06 2026 +0200

8. Cherry-picking commits
Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git switch -c ft/branch
Switched to a new branch 'ft/branch'

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (ft/branch)
$ echo "Implemented test 5" >test5.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (ft/branch)
$ git switch main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git log --oneline ft/branch
1a6cdf5 (HEAD -> main, ft/branch) chore: Create initial and second files
1e55bc4 Create third and fourth files
07725c6 (origin/main, origin/HEAD) Initial commit

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git switch ft/branch
Switched to branch 'ft/branch'

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (ft/branch)
$ git log --oneline
1a6cdf5 (HEAD -> ft/branch, main) chore: Create initial and second files
1e55bc4 Create third and fourth files
07725c6 (origin/main, origin/HEAD) Initial commit

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (ft/branch)
$ git add test5.md
warning: in the working copy of 'test5.md', LF will be replaced by CRLF the next time Git touches it

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (ft/branch)
$ git commit -m "Implemented test 5"
[ft/branch 9d33e94] Implemented test 5
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (ft/branch)
$ git log --oneline
9d33e94 (HEAD -> ft/branch) Implemented test 5
1a6cdf5 (main) chore: Create initial and second files
1e55bc4 Create third and fourth files
07725c6 (origin/main, origin/HEAD) Initial commit

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (ft/branch)
$ git switch main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Nettie King@Nettie-Win MINGW64 ~/Git-Advanced-Exercises (main)
$ git cherry-pick 9d33e94 
[main 8cf54d9] Implemented test 5
 Date: Mon Jun 22 13:52:28 2026 +0200
 1 file changed, 1 insertion(+)
 create mode 100644 test5.md
```
