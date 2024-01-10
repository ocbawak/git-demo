#Demo Git Repository

#To set your global username/email configuration:
#Open the command line.
#Set your username:
git config --global user.name "FIRST_NAME LAST_NAME"
#Set your email address:
git config --global user.email "MY_NAME@example.com"

#Verify your configuration by displaying your configuration file:
cat .git/config

#verify your git configuratio
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git config --global --list
user.name=Cornilus Bawak
user.email=ocbawak@gmail.com


Web Hosting Comparison Chart 2024 - initializr.com.webarchive
(base) iphoneiphone@Iphones-MacBook-Pro website % cd ..
#Create a git demo directory
(base) iphoneiphone@Iphones-MacBook-Pro projects % mkdir git-demo
#initialise your your git working directory
(base) iphoneiphone@Iphones-MacBook-Pro projects % git init git-demo
Initialized empty Git repository in /Users/iphoneiphone/Projects/git-demo/.git/
#Change directory to make sure you are in your working directory
(base) iphoneiphone@Iphones-MacBook-Pro projects % cd git-demo
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % ls

#verify your working directory
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % pwd
/Users/iphoneiphone/projects/git-demo

#invoke a textmate file called readme.md
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % mate README.md
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % ls
README.md

#check status of the newly created file
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % ls
README.md
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git add readme.md
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)
#Add file to the staging area before commit
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git add README.md
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   README.md
#Commit the file
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git commit -m "Initial Commit"
[main (root-commit) 32cafaf] Initial Commit
 1 file changed, 3 insertions(+)
 create mode 100644 README.md
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % ls
README.md
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % open README.md
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % open readme.md
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % 

#Removing git files
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git rm debug.log
rm 'debug.log'
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % ls
README.md
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % 


#Moving files in git
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % ls
README.md	index.html	website
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git mv index.html website
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % ls
README.md	website
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % cd website
(base) iphoneiphone@Iphones-MacBook-Pro website % ls
index.html
(base) iphoneiphone@Iphones-MacBook-Pro website % 
(base) iphoneiphone@Iphones-MacBook-Pro website % git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	renamed:    ../index.html -> index.html

(base) iphoneiphone@Iphones-MacBook-Pro website % 
(base) iphoneiphone@Iphones-MacBook-Pro website % git commit -m "Move file to new destination"
[main 6bba9d3] Move file to new destination
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename index.html => website/index.html (100%)
(base) iphoneiphone@Iphones-MacBook-Pro website % git log
commit 6bba9d3ec0bd29817e3d3c17a7e94e3bfecc361f (HEAD -> main)
Author: Cornilus Bawak <ocbawak@gmail.com>
Date:   Mon Jan 8 08:44:07 2024 -0600

    Move file to new destination

commit c6862664baac393d9de7bd2065f9ce65c99480d8
Author: Cornilus Bawak <ocbawak@gmail.com>
Date:   Sun Jan 7 13:27:49 2024 -0600

    Initial Commit

commit faa9c54d0f37961f661ecf8e5c4b4e9c9e66b797
Author: Cornilus Bawak <ocbawak@gmail.com>
Date:   Sun Jan 7 12:58:29 2024 -0600

    Saving new changes
#Ignoring file in git. Use the dot before the file name to ignore
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % mate .gitignore
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % ls
README.md	application.log	website
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % ls -a
.		.git		README.md	website
..		.gitignore	application.log
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.gitignore
	application.log

no changes added to commit (use "git add" and/or "git commit -a")
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git add application.log
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git commit -m "Initial Commit"
[main 263c4c8] Initial Commit
 1 file changed, 3 insertions(+)
 create mode 100644 application.log
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.gitignore

no changes added to commit (use "git add" and/or "git commit -a")
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % 

#Git History / File Management Commands
 

##Lecture Command Listing -- History
git log
git help log
git log --oneline --graph --decorate --color
 

##Lecture Command Listing -- Removing Files
pwd
git status
mate debug.log
ls
git status
git add .
git status
git commit -m "adding log file that really does not belong here"
clear
git status
git rm debug.log
ls
git status
git commit -m "removing log file"
clear
mate info.log
ls
git add info.log
git commit -m "adding info log"
git status
clear
ls
rm info.log
ls
git status
git add .
git add -u
clear
git status
git commit -m "Removing info.log"
 

##Lecture Command Listing -- Moving Files
ls
mkdir web
ls
git mv index.html web
cd web/
ll
pwd
cd ..
ls
git status
git commit -m "Moving index.html file to web folder"
clear
 

##Lecture Command Listing -- Ignoring Files
mate application.log
ls
git status
mate .iitignore
git status
ls -a
git add .gitignore
clear
git status
git commit -m "adding ignore file"
 


##Seeing Repository History

git log
git log --oneline --graph --decorate --color
Git's log command displays the repository's history in reverse chronological order. The no-params version displays the standard view.

Git log options from above: --oneline Compacts log data on to one line, abbreviating the SHA1 hash --graph Adds asterisk marks and pipes next to each commit to show the branching graph lines --decorate Adds the markers for branch names and tags next to corresponding commits --color Adds some color to the output -- nice to have, depending on the operating system
Removing a file using Git

git rm file-name
##Removing a file using Terminal

rm file-name
##This removes the file outside Git's knowledge

Updating Git's Index (staging area)

git add -u
##The -u parameter will recursively update Git's staging area regarding deleted/moved files outside of Git.

mkdir folder-name
##The mkdir command is a nearly universal command for creating a directory/folder.

Making a directory (folder)

git mv source destination
##The git mv command will move the source (file or folder) to the destination with Git.

#Pushing files to github
(base) iphoneiphone@Iphones-MacBook-Pro projects % ls
SQL		demo-one	git-demo	website
(base) iphoneiphone@Iphones-MacBook-Pro projects % git demo
git: 'demo' is not a git command. See 'git --help'.

The most similar command is
	daemon
(base) iphoneiphone@Iphones-MacBook-Pro projects % cd git demo
cd: string not in pwd: git
(base) iphoneiphone@Iphones-MacBook-Pro projects % cd git-demo
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.gitignore

no changes added to commit (use "git add" and/or "git commit -a")
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % open readme.md
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git remote add origin git@github.com:ocbawak/git-demo.git
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git remote -v
origin	git@github.com:ocbawak/git-demo.git (fetch)
origin	git@github.com:ocbawak/git-demo.git (push)
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git push -u origin master
error: src refspec master does not match any
error: failed to push some refs to 'github.com:ocbawak/git-demo.git'
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git push -u origin base
error: src refspec base does not match any
error: failed to push some refs to 'github.com:ocbawak/git-demo.git'
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % 
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git remote add origin git@github.com:ocbawak/git-demo.git
git branch -M master
git push -u origin master
error: remote origin already exists.
Enumerating objects: 24, done.
Counting objects: 100% (24/24), done.
Delta compression using up to 10 threads
Compressing objects: 100% (19/19), done.
Writing objects: 100% (24/24), 3.57 KiB | 3.57 MiB/s, done.
Total 24 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), done.
To github.com:ocbawak/git-demo.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % git push origin master
Everything up-to-date
(base) iphoneiphone@Iphones-MacBook-Pro git-demo % 

Git Remote Commands
Git Remote Commands
 

Lecture Command Listing
git status
git remote add origin git@github.com:scm-ninja/git-demo.git
git remote -v
git push -u origin master
git push origin master
ls
cd web/
mate index.html
clear
git commit -am "Updating index page for GH"
git status
git pull origin master
git push origin master
 

Command Reference
Creating a remote repository reference

git remote add remote-name remote-repository-location
Using git remote add command allows us to associate a remote repository. Normally, you want to paste in the full URL for the remote repository given to you by your Git host (GitHub). By convention, the first or primary remote repository is named origin.

List Git's Remotes

git remote -v
The git remote command lists the names of all the remote repositories and the -v parameter (verbose) will display the full URL of the remote repository for each remote name listed

Send Changes to Remote

git push -u remote-name branch-name
git push remote-name branch-name
The git push sends all your local changes (commits) on branch branch-name to the remote named remote-name. The -u parameter is needed the first time you push a branch to the remote.

Receive Changes from Remote

git pull remote-name branch-name
The git pull receives all your remote changes (commits) from the remote named remote-name and on branch branch-name.