---
layout: default
title: Git/GitHub
nav_order: 2
description: "Git/GitHub related commands."
---

# Git/GitHub
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

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
