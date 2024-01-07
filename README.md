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