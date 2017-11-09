# Git Manual

https://matthew-brett.github.io/curious-git/curious_git.html

## Removing the last commit

To remove the last commit from git, you can simply run ˋˋgit reset --hard HEAD^ˋˋ 
If you are removing multiple commits from the top, you can run ˋˋgit reset --hard HEAD~2ˋˋ to remove the last two commits. You can increase the number to remove even more commits.

If you want to "uncommit" the commits, but keep the changes around for reworking, remove the "--hard": ˋˋgit reset HEAD^ˋˋ which will evict the commits from the branch and from the index, but leave the working tree around.

If you want to save the commits on a new branch name, then run git branch newbranchname before doing the git reset.


## Using git from Visual Studio Code

Click on the git symbol at the left menu and and write commit message.  
(press Ctrl+Enter to commit)

To push to origin on github:  
Ctrl+Shft P,  `Git Push`

## Basic configuration

We need to tell git our name and email address before we start.

Git will use this information to fill in the author information in each
**commit message**, so we don't have to type it out every time.

```git
    git config --global user.name "Matthew Brett"
    git config --global user.email "matthew.brett@gmail.com"
```

The ``--global`` flag tells mgit to store this information in its default
configuration file for your user account.  On Unix (e.g. OSX and Linux) this
file is ``.gitconfig`` in your home directory.  Without the ``--global`` flag,
git only applies the configuration to the particular **repository** you are
working in.

## Create a new repository on the command line

```git
echo "# Languages" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/hesand/Languages.git
git push -u origin master
```

…or push an existing repository from the command line

```git
git remote add origin https://github.com/hesand/Languages.git
git push -u origin master
```

# Installing latest version of git on Ubuntu

```bash
sudo apt-add-repository ppa:git-core/ppa
sudo apt-get update
sudo apt-get install git
```
