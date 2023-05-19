# Bundle 2

PS C:\Users\user\Documents\git_exercises> git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
Untracked files:
  (use "git add <file>..." to include in what will be 
committed)
        services.html
nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\user\Documents\git_exercises> git status  
On branch ft/bundle-2
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)   
        new file:   services.html

PS C:\Users\user\Documents\git_exercises> git commit -m "new page from the ft/bundle-2 branch"
[ft/bundle-2 f22e137] new page from the ft/bundle-2 branch
 1 file changed, 12 insertions(+)
 create mode 100644 services.html
PS C:\Users\user\Documents\git_exercises> git push --set-upstream origin ft/bundle-2 
fatal: unable to access 'https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git/': Could not resolve host: github.com
PS C:\Users\user\Documents\git_exercises> git push --sremote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Gihozo23/Gym-Git-Exercise-Solution/pull
remote:
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
PS C:\Users\user\Documents\git_exercises>  git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\user\Documents\git_exercises>

remote: Counting objects: 100% (2/2), done.
remote: Compressing objects: 100% (2/2), done.
Unpacking objects: 100% (2/2), 1.21 KiB | 155.00 KiB/s, done.
From https://github.com/Gihozo23/Gym-Git-Exercise-Solution
 * branch            main       -> FETCH_HEAD
   49dae7a..bb18626  main       -> origin/main
Updating 49dae7a..bb18626
Fast-forward
 about.html    |  12 +++++
 home.html     |  12 +++++
 readme.md     | 154 ++++++++++++++++++++++++++++++++++++++++++++++++++
 services.html |  12 +++++
 4 files changed, 190 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS C:\Users\user\Documents\git_exercises> git checkout -b ft/service-re
Switched to a new branch 'ft/service-redesign'
PS C:\Users\user\Documents\git_exercises> git commit -m "Add new change
PS C:\Users\user\Documents\git_exercises> git push origin ft/service-re
Enumerating objects: 5, done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 383 bytes | 383.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by vi
remote:      https://github.com/Gihozo23/Gym-Git-Exercise-Solution/pull
remote:
 * [new branch]      ft/service-redesign -> ft/service-redesign
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\user\Documents\git_exercises> git add services.html
PS C:\Users\user\Documents\git_exercises> git commit -m "Add new change
[main 3b251d3] Add new changes to service.html on main branch
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\user\Documents\git_exercises> git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
   bb18626..3b251d3  main -> main
PS C:\Users\user\Documents\git_exercises> git checkout ft/service-redes
Switched to branch 'ft/service-redesign'
PS C:\Users\user\Documents\git_exercises> git diff main
diff --git a/services.html b/services.html
index 1795184..01f95e2 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,6 @@
     <title>Service center</title>
 </head>
 <body>
-    <h1> second part and it is done in the main branchgit </h1>
+    <h1> first part and it is done from the ft/service-redesign.</h1>
 </body>
 </html>
\ No newline at end of file
PS C:\Users\user\Documents\git_exercises> git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Merge branch 'main' into ft/service-redesign
PS C:\Users\user\Documents\git_exercises> git add services.html
PS C:\Users\user\Documents\git_exercises> git commit
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\user\Documents\git_exercises> git push --set-upstream origin ft/service-redesign
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 405 bytes | 405.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.  
To https://github.com/Gihozo23/Gym-Git-Exercise-Solution.git
   2682865..087baf2  ft/service-redesign -> ft/service-redesign        
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.