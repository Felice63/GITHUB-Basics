# Github basics

## Setting up GIT in VS Code

Once you create a **[Github Account](https://github.com/)**, you can connect VS Code directly to your remote account.

[SEE This article on how to get started setting up GIT for VS Code](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)

## First Time Git Setup

To set your account's default identity, open the terminal and run

```CLI
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
```

You can omit the --global flag to set the identity only in the specific repository that is open, otherwise include it for all repositories.


## How to Initiate a GitHub Repository from VS Code

You can create a GitHub repository directly from your local installation of Visual Studio Code:

1. **Create your project folder locally** and add your files³.
2. **Open your project folder with VS Code**¹.
3. **Initialize a new local Git repository**:
    - Click on the 'Source Control' icon on the left navbar in VS Code, which is third from the top, below the search icon¹².
    - This creates a new Git Repository in the current folder, allowing you to start tracking code changes².
4. **Commit your changes**:
    - You should be able to see files ready to be committed.
    - Press on the 'Commit' button, provide comments, stage the changes and commit the files¹.
    - Alternatively, you can run `git commit -m "With your comment,  inside quote marks, describing the changes you made to your files"` from the terminal¹.
5. **Publish to GitHub**:
    - Click on the source control menu on the sidebar (or press Ctrl+Shift+G), then click on 'Publish to GitHub'¹.
    - From there, just log in and follow the instructions¹.

Your VSCode Repository should now be available on GitHub³. Please note that you need to have Git installed on your computer to perform these actions². If Git is missing, the Source Control view shows instructions on how to install it². Make sure to restart VS Code afterwards².

**References**

(1) How to Create a Github Repository from VS Code (Example). https://www.jcchouinard.com/create-a-github-repository-vscode/.

(2) Introduction to Git in VS Code - Visual Studio Code. https://code.visualstudio.com/docs/sourcecontrol/intro-to-git.

(3) How to add a new project to Github using VS Code. https://stackoverflow.com/questions/46877667/how-to-add-a-new-project-to-github-using-vs-code.

## Using the VS Code Terminal to clone and edit a GitHub Repository

- If the repository already exists in your GitHub account, you can clone (copy) the repository to your local computer using the command line.
- For that you will need the URL of the repository in your Github account, so open your GitHub account and go to your repository.  
- The repository window shows a list of the files and folders, and there is a green "Code" button to the right. Clicking on that button reveals a list of options to copy or clone the files to your computer. Note that the URL for the repository is found here as well.


### Clone your repository to your local machine

- To clone your repository from GitHub to your local computer, go to your repository page on GitHub and click the green "Code" button and Clone or download a zipped archive of your repository. The “HTTPs” section displays the URL for your repository. You can copy this URL and then use the terminal (or command line) to sync any changes you make on the files of the cloned repository, to the original repository.

- On your local machine, open terminal and `cd` (change directory) to where you would like to clone your repository.

- Once you are in the directory, type in the terminal:

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

### Remove Mac OS .DS_Store file from repositories

- This is from the following repositiory: [
vybstat/ds_store_removal](https://gist.github.com/vybstat/1680bef4715bfbcb0268)

```GIT

# How to remove the .DS_Store file from GitHub that MAC OS X creates

# First find and remove .DS_Store
find . -name .DS_Store -print0 | xargs -0 git rm -f --ignore-unmatch

# Create .gitignore file, if you need to
touch .gitignore
echo .DS_Store > .gitignore

# Push changes to GitHub
git add .gitignore
git commit -m '.DS_Store removed'
git push

```

### Reference:

- **[This article](https://dev.to/g_abud/advanced-git-reference-1o9j)** provides more complete instructions for using GitHub.


- **[This URL](https://www.earthdatascience.org/workshops/intro-version-control-git/basic-git-commands/)** gives step-by-step instructions for using the Command Line to clone your GithHub repository to your local computer.
