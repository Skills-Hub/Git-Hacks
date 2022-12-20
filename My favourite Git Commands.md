# Git 
We all use GIT every day. Git is an excellent tool that helps developers to collaborate. I have been using GIT for a long time, and here are some of the commands I use most days.


## git config
Git config command is super helpful. Especially when you are using Git for the first time, or you have a new Git installation. This command will set up your identity - Name and Email address. And this information will be used with every commit.

### Usage

$ git config --global user.name "Your name"  

$ git config --global user.email "Your email"



## git version
As its name implies, it's just to check which version of Git you are using.

### Usage  

$ git version



## git init
This is probably the first command you use to start a new project in Git. This command will create a blank new repository, and then you can store your source code inside this repo.

### Usage  

$ git init 

Or you can use the repository name with your git init command.

$ git init <your repository name>


## git clone
The git clone command will use an existing repository to copy. There is one main difference between the git init and git clone. 

You will use the Git clone when you need to make a copy on an existing repository. The git clone command internally uses the git init command first and then checks out all its contents.

### Usage 

git clone <your project URL>



## git add
The Git add command will add all the new code files or modified files into your repository. This command offers different options to add files and folders. 

Here is the usage of the Git add command.

### Usage

$ git add your_file_name (it will add a single file to your staging area)

$ git add * ( this option will add all the modified and new files to the staging area)



## git commit
This Git command is essential. Your project quality may drop if you will not use this command appropriately. There is another article about how to use Git commands property, and you can read that here.

In simple words, the Git commit will add your changes to your local repository.

### Usage 

$ git commit -m “your useful commit message”



## git status 
This Git command is convenient to see how many files are there which need your attention. You can run this command at any time. 

You can use it in between Git add, and Git commits to see the status.

### Usage 

## git status 



## git branch
Most of the time, you have multiple branches in your Git repository. In simple terms, the branch is an independent line of code development. 

With the Git branch command, you can manage your branches effectively. There are many different options and switches of the Git branch. 

To make it simple, here I will highlight how you can create and delete a Git branch (in case you need more depth, you can refer to - Git Branching and Merging section of this article).

### Usage 

(i) To list all branches:

$ git branch 


(ii) To create a new branch:

$ git branch <branch_name>


(iii) To delete a branch:

$ git branch -d <branch_name>


## git checkout
This Git command is used to switch between branches. This is one of the powerful git commands and can use used as a swiss knife, 

In simple words, here is the syntax to switch to another branch.

### Usage

$ git checkout <branch_name>

Also, you can create and checkout to a branch in a single like, here is the usage for that 

$ git checkout -b <your_new_branch_name>



Intermediate Level Git Commands
After the basic Git commands, it's time to share with you intermediate Git commands; these Git commands are super helpful if you need to collaborate with your team, share your code with others. Also, there are commands like Git log that will help to see the history of previous commits.

## git remote
Git remote command acts like a border, and If you need to connect with the outside world, you have to use the Git remote command. This command will connect your local repository to the remote. 

### Usage 

$ git remote add <shortname> <url>

$ git remote add origin https://github.com/Skills-Hub/Git-Hacks


## git push
Once you are connected with the remote repository (with the help of the git remote command), it's time to push your changes to that repository.

### Usage 

$ git push -u <short_name> <your_branch_name>

$ git push -u origin feature_branch 

$ git push --set-upstream <short_name> <branch_name> 

$ git push --set-upstream origin feature_branch



## git fetch 
When you need to download other team members' changes, you have to use git fetch. 

This command will download all information for commits, refs, etc., so you can review it before applying those changes in your local repository.

### Usage 

$ git fetch 


## git pull
The Git pull command downloads the content (and not the metadata) and immediately updates your local repository with the latest content. 

### Usage 

$ git pull <remote_url>



## git stash
This Git command temporarily stores your modified files. You can work in stashed with the following Git command. 

### Usage 

$ git stash 

And you can view all of your stashes with the following command 

$ git stash list 

$ git stash apply 



## git log
With the help of the Git log, you can see all the previous commits with the most recent commit appear first.

### Usage 

$ git log 

$ git log --all



## git shortlog
The shortlog command shows you a summary from the Git log command. This command is helpful if you are just interested in the short summary. 

This command is helpful to see who worked on what as it group author with their commits.

### Usage 

$ git shortlog  

Git Shortlog Results


## git show
Compared to the Git log, this command git show will show you details about a specific commit.

### Usage 

$ git show <your_commit_hash>



## git rm
Sometimes you need to delete files from your codebase, and in that case, you can use the Git rm command.

It can delete tracked files from the index and the working directory.

### Usage 

$ git rm <your_file_name>



## git merge
Git merge helps you to integrate changes from two branches into a single branch. 

### Usage 

$ git merge <branch_name>

This command will merge the <branch_name> into your current selected branch.


## git rebase 
Git rebase similar to the git merge command. It integrates two branches into a single branch with one exception. A git rebase command rewrites the commit history.

You should use the Git rebase command when you have multiple private branches to consolidate into a single branch. And it will make the commit history linear.

### Usage 

$ git rebase <base>



## git bisect 
The Git bisect command helps you to find bad commits. 

### Usage

i) To start the git bisect 

$ git bisect start


ii) let git bisect know about a good commit

$ git bisect good a123 


iii) And let git bisect know about a bad commit

$ git bisect bad z123

With Git bisect you can narrow down the broken code within a few minutes.


## git cherry-pick 
Git cherry-pick is a helpful command. It's a robust command and allows you to pick any commit from any branch and apply it to any other branch.

### Usage

$ git cherry-pick <commit-hash>

Git cherry-pick doesn’t modify the history of a repository; instead, it adds to the history.



## git archive 
Git archive command will combine multiple files into a  single file. It's like a zip utility, so it means you can extract the archive files to get individual files.

### Usage 

$ git archive --format zip HEAD > archive-HEAD.zip

It will create a zip archive of the current revision.



## git pull --rebase
Most of the time, you need to do rebase (and no merge) when you use Git pull.

In that case, you can use the option

Usage

$ git pull --rebase

It will help you to keep the history clean. Also, you can avoid multiple merges.



##  git blame 
If you need to examine the content of any file line by line,  you need to use git blame. It helps you to determine who made the changes to a file.

### Usage 

$ git blame <your_file_name>



## git tag
In Git, tags are helpful, and you can use them to manage the release. You can think of a Git tag like a branch that will not change. It is significantly more important if you are making a public release.

### Usage 

$ git tag -a v1.0.0


##  git verify-commit
The git verify-commit command will check the gpg signature. GPG or “GNU Privacy Guard” is the tool used in sign files and contains their signatures.

### Usage 

$ git verify-commit <commit>



##  git verify-tag
In the same way, you can confirm a tag.

### Usage 

$ git verify-tag <tag>


##  git diff
Most of the time, you need to compare two git files or branches before you commit or push. Here is a handy command to do that. 

### Usage

i) to compare the working directory with the local repo:

$ git diff HEAD <filename>

ii) to compare two branches:

$ git diff <source branch> <target branch>



##  git citool
Git citool is a graphics alternative of the Git commit.

### Usage

$ git citool



##  git mv
To rename a git file. It will accept two arguments, source and target file name.

### Usage

$ git mv <old-file-name> <new-file-name>



##  git clean
You can deal with untracked files by using the Git clean command. You can remove all the untracked files from your working directory by using this command. In case you want to deal with tracked files you need to use the Git reset command.

### Usage

$ git clean



##  git help
There are many commands in Git, and if you need more help with any command, you can use git help at any time from the terminal. 

### Usage

$ git help <git_command>



##  git whatchanged
This command does the same thing as git log but in a raw form. And it’s in the git because of historical reasons.

### Usage

$ git whatchanged
  
  
 
### git-add
Add file contents to the index

### git-am
Apply a series of patches from a mailbox

### git-archive
Create an archive of files from a named tree

### git-bisect
Use binary search to find the commit that introduced a bug

### git-branch
List, create, or delete branches

### git-bundle
Move objects and refs by archive

### git-checkout
Switch branches or restore working tree files

### git-cherry-pick
Apply the changes introduced by some existing commits

### git-citool
Graphical alternative to git-commit

### git-clean
Remove untracked files from the working tree

### git-clone
Clone a repository into a new directory

### git-commit
Record changes to the repository

### git-describe
Give an object a human readable name based on an available ref

### git-diff
Show changes between commits, commit and working tree, etc

### git-fetch
Download objects and refs from another repository

### git-format-patch
Prepare patches for e-mail submission

### git-gc
Cleanup unnecessary files and optimize the local repository

### git-grep
Print lines matching a pattern

### git-gui
A portable graphical interface to Git

### git-init
Create an empty Git repository or reinitialize an existing one

### git-log
Show commit logs

### git-maintenance
Run tasks to optimize Git repository data

### git-merge
Join two or more development histories together

### git-mv
Move or rename a file, a directory, or a symlink

### git-notes
Add or inspect object notes

### git-pull
Fetch from and integrate with another repository or a local branch

### git-push
Update remote refs along with associated objects

### git-range-diff
Compare two commit ranges (e.g. two versions of a branch)

### git-rebase
Reapply commits on top of another base tip

### git-reset
Reset current HEAD to the specified state

### git-restore
Restore working tree files

### git-revert
Revert some existing commits

### git-rm
Remove files from the working tree and from the index

### git-shortlog
Summarize git log output

### git-show
Show various types of objects

### git-sparse-checkout
Reduce your working tree to a subset of tracked files

### git-stash
Stash the changes in a dirty working directory away

### git-status
Show the working tree status

### git-submodule
Initialize, update or inspect submodules

### git-switch
Switch branches

### git-tag
Create, list, delete or verify a tag object signed with GPG

### git-worktree
Manage multiple working trees

### gitk
The Git repository browser

### scalar
A tool for managing large Git repositories

### Ancillary Commands
Manipulators:

### git-config
Get and set repository or global options

### git-fast-export
Git data exporter

### git-fast-import
Backend for fast Git data importers

### git-filter-branch
Rewrite branches

### git-mergetool
Run merge conflict resolution tools to resolve merge conflicts

### git-pack-refs
Pack heads and tags for efficient repository access

### git-prune
Prune all unreachable objects from the object database

### git-reflog
Manage reflog information

### git-remote
Manage set of tracked repositories

### git-repack
Pack unpacked objects in a repository

### git-replace
Create, list, delete refs to replace objects

## Interrogators:

### git-annotate
Annotate file lines with commit information

### git-blame
Show what revision and author last modified each line of a file

### git-bugreport
Collect information for user to file a bug report

### git-count-objects
Count unpacked number of objects and their disk consumption

### git-diagnose
Generate a zip archive of diagnostic information

### git-difftool
Show changes using common diff tools

### git-fsck
Verifies the connectivity and validity of the objects in the database

### git-help
Display help information about Git

### git-instaweb
Instantly browse your working repository in gitweb

### git-merge-tree
Perform merge without touching index or working tree

### git-rerere
Reuse recorded resolution of conflicted merges

### git-show-branch
Show branches and their commits

### git-verify-commit
Check the GPG signature of commits

### git-verify-tag
Check the GPG signature of tags

### git-version
Display version information about Git

### git-whatchanged
Show logs with difference each commit introduces

### gitweb
Git web interface (web frontend to Git repositories)

### Interacting with Others
These commands are to interact with foreign SCM and with other people via patch over e-mail.

### git-archimport
Import a GNU Arch repository into Git

### git-cvsexportcommit
Export a single commit to a CVS checkout

### git-cvsimport
Salvage your data out of another SCM people love to hate

### git-cvsserver
A CVS server emulator for Git

### git-imap-send
Send a collection of patches from stdin to an IMAP folder

### git-p4
Import from and submit to Perforce repositories

### git-quiltimport
Applies a quilt patchset onto the current branch

### git-request-pull
Generates a summary of pending changes

### git-send-email
Send a collection of patches as emails

### git-svn
Bidirectional operation between a Subversion repository and Git


