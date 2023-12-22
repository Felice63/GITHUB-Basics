# Github basics

- See this URL for using GitHub:
  [https://www.earthdatascience.org/workshops/intro-version-control-git/basic-git-commands/](https://www.earthdatascience.org/workshops/intro-version-control-git/basic-git-commands/)
- It's best to clone the repository into the location where the repositry should live using the command line.
- You will need the URL of the repository from Github, so open your GitHub account and go to the "Clone" area. That is where the URL for the repository is found.
- See the link to the URL above for step-by-step instructions for using the Command Line to clone your GithHub repository.

### Clone your repository to your local machine

- To clone your repository from GitHub to your local computer, go to your repository page on GitHub and click the green button labeled Clone or download. In the “Clone with HTTPs” section, copy the URL for your repository.

- On your local machine, open terminal and `cd` (change directory) to where you would like to clone your repository.

- Once you are in the directory where you want to put your repository, type in the terminal:

- `git clone https://github.com/YOUR-URL-TO-REPO-HERE`

- When you run `git clone repo-path-here`, You should see output like this:

```
cloning into 'test-repo'...
remote: Counting objects: 5, done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (5/5), done.
Checking connectivity... done.
```

### Edit your file and upload to repository

- NOTE that the `.git` element is also downloaded and shows up in the copied directory. It is needed to keep track of changes (the commits that you make) to your file.
- Do not edit the `.git` element.

- After editing your file(s), save the changes, then in the terminal, type `git status` and hit return to execute the command. You should see:

```
On branch master
Your branch is up-to-date with 'origin/master'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

	modified:   NAME-OF-MODIFIED-FILE

no changes added to commit (use "git add" and/or "git commit -a")
```

### Add and Commit

- Use the `add` and `commit` functions to add and commit changes that you made to your files, and upload them to your repositiory from your local directory.

- `git add` --> takes a modified file in your working directory and places the modified version in a staging area.

- `git commit` --> takes everything from the staging area and makes a permanent snapshot of the current state of your repository that is associated with a unique identifier.

### Add files

- You can add an individual file or groups of files to git tracking. To add a single file, use:

```
git add file-name-here-with-extension
```

- To add ALL of the files that you have edited at the same time, you can use:

```
git add --all
```

### Commit files

- Once you are ready to make a snapshot of the current state of your repository, you can use `git commit`. It requires a commit message that describes the snapshot / changes that you made in that commit.

- A commit message should outline what changed and why. These messages help others understand what was changed and why.

- If you are not committing a lot of changes, you can create a short one line commit message using the `-m` flag:

```
git commit -m "Editing the README to try out git add/commit"
```

### Push changes to GitHub

- To add the changes from the files on your computer to the version of your repository on GitHub, you need to push them GitHub with:

```
git push
```

- You will then be prompted for your GitHub user name and password. After you’ve pushed your commits, visit your repository on GitHub and notice that your changes are reflected there, and also that you have access to the full commit history.


### A more complete reference article for using Git:

- [https://dev.to/g_abud/advanced-git-reference-1o9j](https://dev.to/g_abud/advanced-git-reference-1o9j)