---
layout: default
title: Git/GitHub
nav_order: 7
description: "Git/GitHub related commands."
---

# Git/GitHub
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---
# Configure your Git username/email

You typically configure your global username and email address after installing Git. However, you can do so now if you missed that step or want to make changes. After you set your global configuration, repository-specific configuration is optional.

Git configuration works the same across Windows, macOS, and Linux.
To set your global username/email configuration:

```
# Set your username:
git config --global user.name "FIRST_NAME LAST_NAME"

# Set your email address:
git config --global user.email "MY_NAME@example.com"
```

To set repository-specific username/email configuration:

From the command line, change into the repository directory.

```
# Set your username:
git config user.name "FIRST_NAME LAST_NAME"

# Set your email address:
git config user.email "MY_NAME@example.com"
```

Verify your configuration by displaying your configuration file:
`cat .git/config`

# Working with Remote Repositories
## Change Remote Origin

This is useful in case the remote repository (on GitHub maybe) is moved to a different user or organisation. 

```
# First, let's find out what your remote's name was:
$ git remote
origin

# Now, let's find out a bit more information about your remote:
$ git remote show origin
* remote origin
...
... yadda yadda yadda
...

# Neat, now let's get rid of it.
$ git remote rm origin

# Add, the new remote location.
$ git remote add origin path_to_new_remote
```

This can also be achieved by editing `.git/remotes/origin` file.

## Add Additional Remote Repository to an Existing Local Repository

```
# First create a repo on GitHub, but do not initialize it with a readme, gitignore or a liscence file.

git remote add <a name for the new remote repo> <link/path of the remote repo on GitHub>
git push -u <name of the newly added remote repo> master
```
# Fork a Repository and Create a Pull Request
## To Contribute
**Original tutorials:**  
[https://help.github.com/en/articles/fork-a-repo](https://help.github.com/en/articles/fork-a-repo)  
[https://help.github.com/en/articles/syncing-a-fork](https://help.github.com/en/articles/syncing-a-fork)  
[https://help.github.com/en/articles/about-pull-requests](https://help.github.com/en/articles/about-pull-requests)  
[https://help.github.com/en/articles/creating-a-pull-request-from-a-fork](https://help.github.com/en/articles/creating-a-pull-request-from-a-fork)  


* Fork a repo from repo's GitHub page.
* Clone the forked repo to your local computer. 
* To check for remote repository location.  
`git remote -v`
* To keep the local copy in sync with the original upstream repo upon pull.  
`git remote add upstream https://github.com/bioinfobot/bioinfobot.github.io.git`
* Fetch the branches and their respective commits from the upstream repository.     
`git fetch upstream`
* Check out your fork's local master branch.  
`git checkout master`
* Merge the changes from upstream/master into your local master branch. This brings your fork's master branch into sync with the upstream repository, without losing your local changes.  
`git merge upstream/master`

