# An Introduction to Git and GitHub

## Git and Github
A quick aside: git and GitHub are not the same thing.

Git is an open-source, version control tool created in 2005 by developers working on the Linux operating system;

GitHub is a company founded in 2008 that makes tools which integrate with git.

You do not need GitHub to use git, but you cannot use GitHub without using git. There are many other alternatives to GitHub, such as GitLab, BitBucket

### Step 0: Install git and create a GitHub account 

Install git on your local machine [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

Create github account https://github.com/

### Step 1: Create a local git repository 
Create a new directory for your project and navigate to it in your terminal.

for Windows:
```
$ cd C:/Users/user/my_project
```
To initialize a git repository in the root of the folder, run the git init command: 

```
$ git init
```

### Step 2: Add a new file to the repo

Go ahead and add a new file to the project, using any text editor 

We can use VS Code
1. Open the folder in vs code, or simply in the root folder of the project, run in the terminal the command:
```
$ code .
```
2. create a new file and made some changes
3. Save the file or check autosave

Once you've added or modified files in a folder containing a git repo, git will notice that  the file exists inside the repo. 

But, git won't track the file unless you explicitly tell it to. Git only saves/manages changes to files that it tracks, so we’ll need to send a command to confirm that yes, we want git to track our new file.

```
$ git status      
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        <yourfile>

nothing added to commit but untracked files present (use "git add" to track)
```
### The concept of commit

A commit, or "revision", is an individual change to a file (or set of files). When you make a commit to save your work, Git creates a unique ID (a.k.a. the "SHA" or "hash") that allows you to keep record of the specific changes committed along with who made them and when. Commits usually contain a commit message which is a brief description of what changes were made.

**commit message** 
Short, descriptive text that accompanies a commit and communicates the change the commit is introducing.

Commits make up the essence of your project and allow you to jump to the state of a project at any other commit.

### Step 3: Add a file to the staging environment

To add a file to a commit, you first need to add it to the staging environment. To stage modified files in Git, you use the **git add** command followed by the filenames or paths of the files you want to stage. For example:

```
$ git add <file1> <file2>
```
Alternatively, you can use the **git add .** command to stage all modified files in the current directory and its subdirectories:
```
$ git add .
```
When you checl the status

```
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   <your file>
```
### Step 4: Create a commit

It's time to create your first commit!

Run the command git commit -m "Your message about the commit"

For example

```
$ git commit -m "this is the first commit"
[master (root-commit) f6b305d] this is the first commit
 1 file changed, 78 insertions(+)
 create mode 100644 README.md
```
The message at the end of the commit should be something related to what the commit contains - maybe it's a new feature, maybe it's a bug fix, maybe it's just fixing a typo. 

![git file changes](https://git-scm.com/book/en/v2/images/lifecycle.png)

### Step 5: Create a new branch

Say you want to make a new feature but are worried about making changes to the main project while developing the feature. This is where git branches come in. 

Branches allow you to move back and forth between 'states' of a project. 

Official git docs describe branches this way: 
"A branch in Git is simply a lightweight movable pointer to one of these commits.’ 

For example, if you want to add a new page to your website you can create a new branch just for that page without affecting the main part of the project. Once you're done with the page, you can merge your changes from your branch into the primary branch. When you create a new branch, Git keeps track of which commit your branch 'branched' off of, so it knows the history behind all the files. 

Let's say you are on the **primary branch** and want to create a **new branch** to develop your web page. Run **git checkout -b <my branch name>**. This command will automatically create a new branch and then 'check you out' on it, meaning git will move you to that branch, off of the primary branch.

```
$ git branch
* master
```
By default, every git repository’s first branch is named `master` (and is typically used as the primary branch in the project). 

```
$ git checkout -b branch-example  
Switched to a new branch 'branch-example'

$ git branch
* branch-example
  master
```