# git exercises
# Bundle 1
# exercise 1
PS C:\Users\user\Documents\git_exercises> git init
Initialized empty Git repository in C:/Users/user/Documents/Git_Exercises/.git/
PS C:\Users\user\Documents\git_exercises> git status        
On branch master

No commits yet
nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\user\Documents\git_exercises> git branch -M main
PS C:\Users\user\Documents\git_exercises> git status
On branch main

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\user\Documents\git_exercises> git add readme.md
PS C:\Users\user\Documents\git_exercises> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Gihozo-Christelle.jpg
        new file:   index.html

[main (root-commit) 49dae7a] initial commit
 create mode 100644 Gihozo-Christelle.jpg
PS C:\Users\user\Documents\git_exercises> git remote add origin https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
On branch main
nothing to commit, working tree clean
Enumerating objects: 5, done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
PS C:\Users\user\Documents\git_exercises> git checkout -b dev
Switched to a new branch 'dev'
PS C:\Users\user\Documents\git_exercises> git checkout -b test
PS C:\Users\user\Documents\git_exercises> git checkout -d test
HEAD is now at 49dae7a initial commit
PS C:\Users\user\Documents\git_exercises> git checkout dev    
PS C:\Users\user\Documents\git_exercises> git checkout main
Switched to branch 'main'
PS C:\Users\user\Documents\git_exercises> git checkout dev 
Switched to branch 'dev'
PS C:\Users\user\Documents\git_exercises> git status
On branch dev
nothing to commit, working tree clean
PS C:\Users\user\Documents\git_exercises> git push origin dev
remote: Create a pull request for 'dev' on GitHub by visiting:
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
On branch dev
PS C:\Users\user\Documents\git_exercises> git branch -D test
Deleted branch test (was 49dae7a).


# Exercises 2
PS C:\Users\user\Documents\git_exercises> git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html
nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\user\Documents\git_exercises> git add home.html
PS C:\Users\user\Documents\git_exercises> git stash save "saving changes for home.html"
PS C:\Users\user\Documents\git_exercises> git add about.html
PS C:\Users\user\Documents\git_exercises> git stash save "saving changes for about.html"
Saved working directory and index state On dev: saving changes for about.html
PS C:\Users\user\Documents\git_exercises> git add team.html
PS C:\Users\user\Documents\git_exercises> git stash save "saving changes for team.html" 
Saved working directory and index state On dev: saving changes for team.html
stash@{0}: On dev: saving changes for team.html
stash@{1}: On dev: saving changes for about.html
stash@{2}: On dev: saving changes for home.html
user@FEI5CG80215XW MINGW64 ~/Documents/git_exercises (dev)
$ git stash list
stash@{0}: On dev: saving changes for team.html
stash@{1}: On dev: saving changes for about.html
stash@{2}: On dev: saving changes for home.html

user@FEI5CG80215XW MINGW64 ~/Documents/git_exercises (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (33fde1af66c503db8f36215c4e6d251ca35e7e85)

user@FEI5CG80215XW MINGW64 ~/Documents/git_exercises (dev)
$ git stash list
stash@{0}: On dev: saving changes for team.html
stash@{1}: On dev: saving changes for home.html

user@FEI5CG80215XW MINGW64 ~/Documents/git_exercises (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (51d791c8be11deb853e9aa5c4825718e71a3f36f)

user@FEI5CG80215XW MINGW64 ~/Documents/git_exercises (dev)
$ git add .

user@FEI5CG80215XW MINGW64 ~/Documents/git_exercises (dev)
$ git commit -m "Committing current changes for the html pages"
[dev 84818c1] Committing current changes for the html pages
 2 files changed, 24 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

user@FEI5CG80215XW MINGW64 ~/Documents/git_exercises (dev)
$ git push origin dev
fatal: unable to access 'https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git/': Could not resolve host: github.com

user@FEI5CG80215XW MINGW64 ~/Documents/git_exercises (dev)
$ git push origin dev
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 753 bytes | 753.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
   bcc74b4..84818c1  dev -> dev

user@FEI5CG80215XW MINGW64 ~/Documents/git_exercises (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (99b40518100380781d222d44511e64099a095c83)
PS C:\Users\user\Documents\git_exercises> ls


    Directory: C:\Users\user\Documents\git_exercises


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         5/17/2023  11:57 PM            274 about.html
-a----         5/16/2023   7:16 PM        1993179 Gihozo-Christelle.jpg
-a----         5/17/2023  11:57 PM            330 home.html
-a----         5/17/2023  10:59 PM            877 index.html
-a----         5/17/2023  10:57 PM             43 readme.md
-a----         5/18/2023  12:01 AM            274 team.html


