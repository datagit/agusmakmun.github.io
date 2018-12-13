---
layout: post
title:  "Git Stash Tutorial"
date:   2018-01-01 19:31:43 +0700
categories: [bash, linux, git]
---

# Git stash
#### Stashing your work
The git stash command takes your uncommitted changes (both staged and unstaged), saves them away for later use, and then reverts them from your working copy. For example:

![demo](https://raw.githubusercontent.com/datagit/datagit.github.io/master/static/img/_posts/git_stash.png)
```
$ git status
On branch master
Changes to be committed:
new file: style.css
Changes not staged for commit:
modified: index.html
$ git stash
Saved working directory and index state WIP on master: 5002d47 our new homepage
HEAD is now at 5002d47 our new homepage
$ git status
On branch master
nothing to commit, working tree clean
```
#### Re-applying your stashed changes
```
$ git status
On branch master
nothing to commit, working tree clean
$ git stash pop
On branch master
Changes to be committed:
new file: style.css
Changes not staged for commit:
modified: index.html
#Dropped refs/stash@{0} (32b3aa1d185dfe6d57b3c3cc3b32cbf3e380cc6a)
```

```
# tracked files
$ git stash 

# untracked files
$ git stash -u

# Popping your stash removes the changes from your stash and reapplies them to your working copy.
$ git stash pop
$ git stash pop stash@{2}

# Alternatively, you can reapply the changes to your working copy and keep them in your stash with git stash apply
$ git stash aplly

$ git stash list
stash@{0}: WIP on master: 5002d47 our new homepage
stash@{1}: WIP on master: 5002d47 our new homepage
stash@{2}: WIP on master: 5002d47 our new homepage

$ git stash -p
diff --git a/style.css b/style.css
new file mode 100644
index 0000000..d92368b
--- /dev/null
+++ b/style.css
@@ -0,0 +1,3 @@
+* {
+ text-decoration: blink;
+}
Stash this hunk [y,n,q,a,d,/,e,?]? y
diff --git a/index.html b/index.html
index 9daeafb..ebdcbd2 100644
--- a/index.html
+++ b/index.html
@@ -1 +1,2 @@
#+<link rel="stylesheet" href="style.css"/>
Stash this hunk [y,n,q,a,d,/,e,?]? n

# Creating a branch from your stash
$ git stash branch add-stylesheet stash@{1}
Switched to a new branch 'add-stylesheet'
On branch add-stylesheet
Changes to be committed:
new file: style.css
Changes not staged for commit:
modified: index.html
#Dropped refs/stash@{1} (32b3aa1d185dfe6d57b3c3cc3b32cbf3e380cc6a)

# Cleaning up your stash
$ git stash drop stash@{1}
#Dropped stash@{1} (17e2697fd8251df6163117cb3d58c1f62a5e7cdb)

#Or you can delete all of your stashes with:
$ git stash clear


```


**Refference:** [https://www.atlassian.com/git/tutorials/saving-changes/git-stash](https://www.atlassian.com/git/tutorials/saving-changes/git-stash)

hope it usefull.
