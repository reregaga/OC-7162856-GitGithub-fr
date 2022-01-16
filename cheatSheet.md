### Author set up:
```shell script
$ git config --global user.name "John Doe"
$ git config --global user.email john@example.com
```
If you want to **change your username for a specific project,** you will have to repeat this line, but without `--global`.

To make sure that your settings have been taken into account, as well as to **check** the rest of the **settings**, simply enter the command `git config --list`.

### Color set up:
```shell script
$ git config --global color.diff auto
$ git config --global color.status auto
$ git config --global color.branch auto
``` 

### Editor set up:
```shell script
$ git config --global core.editor notepad++
$ git config --global merge.tool vimdiff
```
By **default**, Git uses **Vim** as the editor and **Vimdiff** as the merge tool.

### Init repo
- Initialize repo in folder: `$ git init`
- Or clone existed repo: `$ git clone example.com/repo.git`

### Repo Areas
Let's take a closer look at the **different areas of the local repository**.
- **Working directory**. This area corresponds to the project folder on your computer.
- **Stage** or **index**. This zone mediates between the working directory and the repository. It represents all the changed files that you want to include in your next code release.
- **Repository**. When new versions of the project are created, they are saved here.

These 3 zones are present on your computer locally.

### Add files
- Show info: `$ git status`
- Index files: `$ git add myfile.html`
- Create version: `$ git commit -m "Add myfile"`

If you don't use `-m`, the `git commit` command will open a text editor where you can enter a commit message.

### Sending to remote repo
Your first push need set up:

```
$ git remote add origin https://github.com/user/proj.git
$ git branch -M main

$ git push -u origin main
```
`origin` it is default name for remote repo [githowto.com](https://githowto.com/what_is_origin)

The main branch (`main` (since October 2020) or `master`) will carry all modifications made. Therefore, the goal is not to make changes directly to this branch, but to make them to other branches and, after various tests, integrate them into the main branch.

### Branches
- Show existed branches: `$ git branch`
- Create new branch: `$ git branch myNewBrnach`
- Delete branch: `$ git branch -d myNewBrnach`
- Delete branch with changes: `$ git branch -D myNewBrnach`
- Switch to selected branch: `$ git checkout myNewBranch`

**Imagine branches as folders!** 

`$ git push -u origin myNewBranch`

### Merge:
```
$ git checkout main`
$ git merge myNewBranch
```

### Clone: 
- Download remote repo to pc: `$ git clone example.com/project.git`
- Set label `myShortName` to remote repo: `$ git remote add myShortName example.com/project.git`
- Get updates: `$ git pull myShortName main`

