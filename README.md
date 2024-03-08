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

### Adding file to the staging environment

To add a file to a commit, you first need to add it to the staging environment. To stage modified files in Git, you use the **git add** command followed by the filenames or paths of the files you want to stage. For example:

```
$ git add <file1> <file2>
```
Alternatively, you can use the **git add .** command to stage all modified files in the current directory and its subdirectories:
```
$ git add .
```