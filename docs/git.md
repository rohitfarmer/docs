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

# Change Remote Origin

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
