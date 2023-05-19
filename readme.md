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

# git exercises
# Bundle 3
# Exercise 1

PS C:\Users\user\Documents\git_exercises> git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
PS C:\Users\user\Documents\git_exercises> git add team.html
PS C:\Users\user\Documents\git_exercises> git commit -m "changes about the new html page"     
[ft/team-page e9c3c4a] changes about the new html page
 1 file changed, 12 insertions(+)
ush origin --set-upstream ft/team-page
fatal: unable to access 'https://github.com/Gihush origin --set-upstreaozo23/Gym-Git-Exercise-Solution.git/': Recv faiozo23/Gym-Git-Exercise-Slure: Connection was reset                     ush origin ft/team-page
PS C:\Users\user\Documents\git_exercises> git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 506 bytes | 506.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Gihozo23/Gym-Git-Exercise-Solution/pull
remote:
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
 * [new branch]      ft/team-page -> ft/team-page
PS C:\Users\user\Documents\git_exercises> git checkout main
error: Your local changes to the following files would be overwritten b
        readme.md
Please commit your changes or stash them before you switch branches.
Aborting
PS C:\Users\user\Documents\git_exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\user\Documents\git_exercises> git checkout -b ft/contact-pa
Switched to a new branch 'ft/contact-page'
PS C:\Users\user\Documents\git_exercises> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\user\Documents\git_exercises> git log
commit 993dd55e9e2e04b1167fec76beb159e08b86794b (HEAD -> ft/team-page)
Author: GIHOZO23 <christellegihozo23@gmail.com>
Date:   Fri May 19 23:12:30 2023 +0300

    Readme file updated

commit e9c3c4a7d60d25441c8d7da62c3419882b95b081 (origin/ft/team-page)
Author: GIHOZO23 <christellegihozo23@gmail.com>
Date:   Fri May 19 22:59:19 2023 +0300

    changes about the new html page

commit dc9680c11a5b91ee638c9c3021d5ea4a979c3c09 (origin/ft/service-rede
Author: GIHOZO23 <christellegihozo23@gmail.com>
Date:   Fri May 19 20:54:55 2023 +0300

    new changes done

commit aaa33db0bc81005c3fffa3e4f27a5969327aaad9
Author: GIHOZO23 <christellegihozo23@gmail.com>
Date:   Fri May 19 20:48:38 2023 +0300

    new changes to the readme file

commit 087baf269a75d6de50e7e6a919402e51cce05aa4
Merge: 2682865 3b251d3
Author: GIHOZO23 <christellegihozo23@gmail.com>
Date:   Fri May 19 20:43:49 2023 +0300

    Merge branch 'main' into ft/service-redesign

commit 3b251d302b2facd8e46d6bfd6e9928ff21f63c27 (origin/main, main, ft/
Author: GIHOZO23 <christellegihozo23@gmail.com>
Date:   Fri May 19 19:55:16 2023 +0300

    Add new changes to service.html on main branch

commit bb18626c8e642347211d68f9445dcdd05778d95e
Merge: f728481 f22e137
Author: Furaha123 <96550169+Furaha123@users.noreply.github.com>
Date:   Fri May 19 20:34:02 2023 +0300

    Merge pull request #2 from Gihozo23/ft/bundle-2

    new page from the ft/bundle-2 branch

commit 26828659b651a6fa5597a941dbc5fe0544b25397
Author: GIHOZO23 <christellegihozo23@gmail.com>
Date:   Fri May 19 19:47:00 2023 +0300

    Add new changes to service.html

commit f22e1377681474c9ed0e852e381e8a045d49a3aa (origin/ft/bundle-2, ft
Author: GIHOZO23 <christellegihozo23@gmail.com>
Date:   Fri May 19 17:27:02 2023 +0300

    new page from the ft/bundle-2 branch

commit f72848191cf01cd19eef0642488590d46f8d4f3b
Merge: 49dae7a f955d78
Author: Gihozo23 <109101706+Gihozo23@users.noreply.github.com>
Date:   Thu May 18 01:11:20 2023 +0300

    Merge pull request #1 from Gihozo23/dev

    Dev

commit f955d789572147e3e04f795b061e07d378a8852e (origin/dev, dev)
Author: GIHOZO23 <christellegihozo23@gmail.com>
Date:   Thu May 18 00:09:12 2023 +0300
Date:   Thu May 18 00:09:12 2023 +0300
    Merge pull request #2 from Gihozo23/ft/bundle-2

    new page from the ft/bundle-2 branch
commit 26828659b651a6fa5597a941dbc5fe0544b25397
Author: GIHOZO23 <christellegihozo23@gmail.com>
Date:   Fri May 19 19:47:00 2023 +0300

/bundle-2)
Author: GIHOZO23 <christellegihozo23@gmail.com>
Date:   Fri May 19 17:27:02 2023 +0300
    new page from the ft/bundle-2 branch

commit f72848191cf01cd19eef0642488590d46f8d4f3b
Merge: 49dae7a f955d78
Author: Gihozo23 <109101706+Gihozo23@users.noreply.github.com>
Date:   Thu May 18 01:11:20 2023 +0300

    Merge pull request #1 from Gihozo23/dev


commit f955d789572147e3e04f795b061e07d378a8852e (origin/dev, dev)      
Author: GIHOZO23 <christellegihozo23@gmail.com>
PS C:\Users\user\Documents\git_exercises> git checkout ft/contact-page 
Switched to branch 'ft/contact-page'
PS C:\Users\user\Documents\git_exercises> git cherry-pick e9c3c4a7d60d25441c8d7da62c3419882b95b081
[ft/contact-page ea616cd] changes about the new html page
 Date: Fri May 19 22:59:19 2023 +0300
 1 file changed, 12 insertions(+)
 create mode 100644 team.html
PS C:\Users\user\Documents\git_exercises> git add team.html
PS C:\Users\user\Documents\git_exercises> git commit -m "changes where 
done because of the usage of the git cheery-pick command"
[ft/contact-page 08c43f0] changes where done because of the usage of the git cheery-pick command
PS C:\Users\user\Documents\git_exercises> git push
Counting objects: 100% (7/7), done.            o upstream branch.      
Delta compression using up to 4 threads        s upstream, use
Compressing objects: 100% (6/6), done.
Total 6 (delta 3), reused 0 (delta 0), pack-reuagesed 0
remote: Resolving deltas: 100% (3/3), completedwithout a tracking       with 1 local object.                          lp config'.
remote:
remote: Create a pull request for 'ft/contact-push --set-upstream origiage' on GitHub by visiting:
remote:      https://github.com/Gihozo23/Gym-Git-Exercise-Solution/pull/new/ft/contact-page   
remote:
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git                                   KiB/s, done.
 * [new branch]      ft/contact-page -> ft/contsed 0act-page                                        with 1 local object.   
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.                            age' on GitHub by visiti
PS C:\Users\user\Documents\git_exercises> git checkout -b ft/faq-page                         t-Exercise-Solution/pull
Switched to a new branch 'ft/faq-page'
PS C:\Users\user\Documents\git_exercises> git aPS C:\Users\user\Documents\git_exercises> git c-Solution.git 1 file changed, 12 insertions(+)              act-page
 create mode 100644 faq.html                   n/ft/contact-page'.     
PS C:\Users\user\Documents\git_exercises> git pheckout -b ft/faq-page  ush origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Compressing objects: 100% (3/3), done.
Revert "changes about the new html page"       
Writing objects: 100% (3/3), 458 bytes | 458.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Gihozo23/Gym-Git-Exercise-Solution/pull/new/ft/faq-page       
remote:
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
 * [new branch]      ft/faq-page -> ft/faq-pagePS C:\Users\user\Documents\git_exercises> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\user\Documents\git_exercises> git reverte 9c3c4a7d60d25441c8d7da62c3419882b95b081 
git: 'reverte' is not a git command. See 'git -

PS C:\Users\user\Documents\git_exercises> git revert e9c3c4a7d60d25441c8d7da62c3419882b95b081 
e new html page"
 1 file changed, 12 deletions(-)
 delete mode 100644 team.html
PS C:\Users\user\Documents\git_exercises> git push origin ft/team-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads        
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 540 bytes | 540.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
   e9c3c4a..087631f  ft/team-page -> ft/team-page

# exercise 2

PS C:\Users\user\Documents\git_exercises> git checkout ft/faq-page
Switched to branch 'ft/faq-page'
PS C:\Users\user\Documents\git_exercises> git checkout -b ft/home-page-redesign
PS C:\Users\user\Documents\git_exercises> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\user\Documents\git_exercises> git add readme.md
PS C:\Users\user\Documents\git_exercises> git commit -m "added the Bundle 3 commands to this file"
[main 785959a] added the Bundle 3 commands to this file
PS C:\Users\user\Documents\git_exercises> git push origin main
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changhint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS C:\Users\user\Documents\git_exercises> git fetch
remote: Enumerating objects: 15, done.
remote: Counting objects: 100% (15/15), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 8 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (8/8), 3.75 KiB | 69.00 KiB/s, done.
From https://github.com/Gihozo23/Gym-Git-Exercise-Solution
   3b251d3..2ccb5ef  main       -> origin/main
PS C:\Users\user\Documents\git_exercises> git push origin main
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/Gihozo23/Gym-Git
hint: Updates were rejected because the tip of your current branch is b
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for detai
PS C:\Users\user\Documents\git_exercises> git pull origin main
From https://github.com/Gihozo23/Gym-Git-Exercise-Solution
 * branch            main       -> FETCH_HEAD
Auto-merging readme.md
CONFLICT (content): Merge conflict in readme.md
Automatic merge failed; fix conflicts and then commit the result.      
le 3 commands to this file"
PS C:\Users\user\Documents\git_exercises> git push origin main
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
PS C:\Users\user\Documents\git_exercises> git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'     B/s, done.
PS C:\Users\user\Documents\git_exercises> git rsed 0ebase main                                      with 2 local objects.  
Successfully rebased and updated refs/heads/ft/-Solution.githome-page-redesign.
PS C:\Users\user\Documents\git_exercises> git add home.html                                   heckout ft/home-page-red
PS C:\Users\user\Documents\git_exercises> git commit -m "new changes"
[ft/home-page-redesign bfa401f] new changes    ebase main
 1 file changed, 1 insertion(+)                home-page-redesign.     
PS C:\Users\user\Documents\git_exercises> git push origin ft/home-page-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads        
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 333 bytes | 333.00 KiB/s, done.
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by 
visiting:
remote:      https://github.com/Gihozo23/Gym-Git-Exercise-Solution/pull/new/ft/home-page-redesign
remote:
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign