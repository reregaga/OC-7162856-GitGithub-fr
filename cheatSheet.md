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

