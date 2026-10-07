# Git - sprawdzian

Egzamin@DESKTOP-C2B5R5P MINGW64 ~ (master)
$ mkdir sprawdzian

Egzamin@DESKTOP-C2B5R5P MINGW64 ~ (master)
$ cd sprawdzian

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git init
Initialized empty Git repository in C:/Users/Egzamin/sprawdzian/.git/

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git global user.name
git: 'global' is not a git command. See 'git --help'.

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git --global user.name
unknown option: --global
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--no-lazy-fetch]
           [--no-optional-locks] [--no-advice] [--bare] [--git-dir=<path>]
           [--work-tree=<path>] [--namespace=<name>] [--config-env=<name>=<envvar>]
           <command> [<args>]

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git -global user.name "Igor"
unknown option: -global
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--no-lazy-fetch]
           [--no-optional-locks] [--no-advice] [--bare] [--git-dir=<path>]
           [--work-tree=<path>] [--namespace=<name>] [--config-env=<name>=<envvar>]
           <command> [<args>]

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git config user.name "Igor"

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git config user.email "Igor.Sarlinski@zse.krakow.pl"

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ echo "# Git - sprawdzian" > README.md

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git add .
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches i
t

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git commit -m "Initial commit"
[master (root-commit) e82d9bd] Initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git remote add origin https://github.com/sarnus1980/Sprawdzian.git

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git remote -v
origin  https://github.com/sarnus1980/Sprawdzian.git (fetch)
origin  https://github.com/sarnus1980/Sprawdzian.git (push)

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git push -u origin master
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 239 bytes | 239.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/sarnus1980/Sprawdzian.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git switch -c feature-profile
Switched to a new branch 'feature-profile'

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-profile)
$ echo

"
Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-profile)
$ echo "# Profil użytkownika" > profile.md

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-profile)
$ git add .
warning: in the working copy of 'profile.md', LF will be replaced by CRLF the next time Git touches
it

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-profile)
$ git diff

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-profile)
$ git status
On branch feature-profile
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   profile.md


Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-profile)
$ git commit -m "Add profile"
[feature-profile 7f884f3] Add profile
 1 file changed, 1 insertion(+)
 create mode 100644 profile.md

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-profile)
$ git push -u origin feature-profile
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 304 bytes | 304.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'feature-profile' on GitHub by visiting:
remote:      https://github.com/sarnus1980/Sprawdzian/pull/new/feature-profile
remote:
To https://github.com/sarnus1980/Sprawdzian.git
 * [new branch]      feature-profile -> feature-profile
branch 'feature-profile' set up to track 'origin/feature-profile'.

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-profile)
$

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-profile)
$ git switch main
fatal: invalid reference: main

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-profile)
$ git switch master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git switch -c feature-contact
Switched to a new branch 'feature-contact'

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-contact)
$ echo "# Kontakt" > contact.md

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-contact)
$ git add .
warning: in the working copy of 'contact.md', LF will be replaced by CRLF the next time Git touches
it

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-contact)
$ git commit -m "Add contact"
[feature-contact fd73417] Add contact
 1 file changed, 1 insertion(+)
 create mode 100644 contact.md

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-contact)
$ git switch master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git merge feature-contact
Updating e82d9bd..fd73417
Fast-forward
 contact.md | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 contact.md

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git branch -d feature-contact
Deleted branch feature-contact (was fd73417).

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git push -u origin master
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 290 bytes | 290.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/sarnus1980/Sprawdzian.git
   e82d9bd..fd73417  master -> master
branch 'master' set up to track 'origin/master'.

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ echo "Aplikacja" > heading.txt

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git add .
warning: in the working copy of 'heading.txt', LF will be replaced by CRLF the next time Git touches
 it

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git commit -m "Add heading"
[master b13c62f] Add heading
 1 file changed, 1 insertion(+)
 create mode 100644 heading.txt

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git switch -c feature-heading
Switched to a new branch 'feature-heading'

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-heading)
$ echo "Nowoczesna aplikacja" > heading.txt

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-heading)
$ git add .
warning: in the working copy of 'heading.txt', LF will be replaced by CRLF the next time Git touches
 it

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-heading)
$ git commit -m "Change heading on feature"
[feature-heading 8b9c2d9] Change heading on feature
 1 file changed, 1 insertion(+), 1 deletion(-)

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-heading)
$ git switch master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ echo "Aplikacja webowa" > heading.txt

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git add .
warning: in the working copy of 'heading.txt', LF will be replaced by CRLF the next time Git touches
 it

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git commit -m "Change heading on master"
[master c2acc5b] Change heading on master
 1 file changed, 1 insertion(+), 1 deletion(-)

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git merge feature-heading
Auto-merging heading.txt
CONFLICT (content): Merge conflict in heading.txt
Automatic merge failed; fix conflicts and then commit the result.

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master|MERGING)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   heading.txt

no changes added to commit (use "git add" and/or "git commit -a")

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master|MERGING)
$ git diff
diff --cc heading.txt
index 3e3cf0e,c0ece0e..0000000
--- a/heading.txt
+++ b/heading.txt
@@@ -1,1 -1,1 +1,5 @@@
++<<<<<<< HEAD
 +Aplikacja webowa
++=======
+ Nowoczesna aplikacja
++>>>>>>> feature-heading

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master|MERGING)
$ code heading.txt

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master|MERGING)
$ git add .

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master|MERGING)
$ git commit -m "Konflikt fixed"
[master f2423da] Konflikt fixed

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git push -u origin master
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 8 threads
Compressing objects: 100% (8/8), done.
Writing objects: 100% (12/12), 1002 bytes | 501.00 KiB/s, done.
Total 12 (delta 4), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (4/4), done.
To https://github.com/sarnus1980/Sprawdzian.git
   fd73417..f2423da  master -> master
branch 'master' set up to track 'origin/master'.

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git switch -c feature-footer
Switched to a new branch 'feature-footer'

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-footer)
$ echo "# Stopka" > footer.md

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-footer)
$ git add .
warning: in the working copy of 'footer.md', LF will be replaced by CRLF the next time Git touches i
t

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-footer)
$ git commit -m "Add footer"
[feature-footer b215e5e] Add footer
 1 file changed, 1 insertion(+)
 create mode 100644 footer.md

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-footer)
$ git push -u origin feature-footer
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 355 bytes | 355.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'feature-footer' on GitHub by visiting:
remote:      https://github.com/sarnus1980/Sprawdzian/pull/new/feature-footer
remote:
To https://github.com/sarnus1980/Sprawdzian.git
 * [new branch]      feature-footer -> feature-footer
branch 'feature-footer' set up to track 'origin/feature-footer'.

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-footer)
$ switch master
bash: switch: command not found

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (feature-footer)
$ git switch master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ git pull origin master
From https://github.com/sarnus1980/Sprawdzian
 * branch            master     -> FETCH_HEAD
Already up to date.

Egzamin@DESKTOP-C2B5R5P MINGW64 ~/sprawdzian (master)
$ ls
README.md  contact.md  heading.txt
