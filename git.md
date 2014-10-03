In the terminal (or git bash), create a new directory:

```
$ mkdir my_new_git_repo
```

Change into that directory:

```
$ cd my_new_git_rep
```

Initialize the directory to be a Git powered directory:

```
$ git init
Initialized empty Git repository in /home/moorepants/src/my_new_git_repo/.git/
```

Create a text file in your text editor and save it in the `my_new_git_repo`
directory as `my_file.txt`.

Check the status of the repository:

```
(master)$ git status
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	my_file.txt

nothing added to commit but untracked files present (use "git add" to track)
```

Git sees a file in the directory but is not tracking it. So add the file so git
starts to track it:

```
(master)$ git add my_file.txt
```

Now the status of the repository has changed:

```
(master)$ git status
moorepants@moorepants-2170p:my_new_git_repo(master)$ git status
On branch master

Initial commit

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   my_file.txt
```

Git says you have a new file but that it needs to be committed, so commit the
changes to record the first version of that file:

```
(master)$ git commit my_file.txt -m "This is the first commit"
[master (root-commit) 33ec736] This is my first commit.
 1 file changed, 1 insertion(+)
 create mode 100644 my_file.txt
```

Now the repository status shows that is is clean. No files that have not been
added or anything that needs to be committed.

```
(master)$ git status

On branch master
nothing to commit, working directory clean
```

The repository log shows that you have one commit:

```
(master)$ git log
commit 33ec736b4638f6efdb0bd943d3fe1a2f4f8d5609
Author: Jason K. Moore <moorepants@gmail.com>
Date:   Sat Sep 13 15:59:56 2014 -0400

    This is my first commit.
```

Now edit the file in your text editor and check the status:

```
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   my_file.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

Git sees that you modified the file. You can see the difference in the current
version and the last committed version with:

```
(master)$ git diff
diff --git a/my_file.txt b/my_file.txt
index 197d1d0..c8a19aa 100644
--- a/my_file.txt
+++ b/my_file.txt
@@ -1 +1,2 @@
 This is my file.
+My second line.
```

which shows that you have changed the file. In this case, I have added a line.
Now commit the changes:

```
(master)$ git commit my_file.txt -m "My second commit, added a line."
```

The log will now show the two commits:

```
(master)$ git log
commit 2914c88c35fb9c6d6e07d7ab90e0500761a58ca8
Author: Jason K. Moore <moorepants@gmail.com>
Date:   Sat Sep 13 16:08:11 2014 -0400

    My second commit, added a line.

commit 33ec736b4638f6efdb0bd943d3fe1a2f4f8d5609
Author: Jason K. Moore <moorepants@gmail.com>
Date:   Sat Sep 13 15:59:56 2014 -0400

    This is my first commit.
```

# More Info

Software Carpentry's lesson on version control with Git:

http://software-carpentry.org/v5/novice/git/index.html


