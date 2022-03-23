---
title: Git本地与云端的连接
date: 2022-03-22 16:32:19
tags:
---
**Quick setup — if you’ve done this kind of thing before**
> Set up in Desktop
>
or	

HTTPS: 
```shell script
https://github.com/Monologue-N/<Repo-Name>.git
```
SSH:
```shell script
git@github.com:Monologue-N/<Repo-Name>.git
```

Get started by creating a new file or uploading an existing file. We recommend every repository include a README, LICENSE, and .gitignore.

---

**…or create a new repository on the command line**

```shell script
echo "# Mono-Notes" >> README.md
git init

git add README.md
  或者全加
git add .

git commit -m "first commit"

git branch -M main

git remote add origin https://github.com/Monologue-N/<Repo-Name>.git
  或者用SSH
git remote add origin git@github.com:Monologue-N/<Repo-Name>.git

git push -u origin main
```
---

**…or push an existing repository from the command line**

```shell script
git remote add origin https://github.com/Monologue-N/<Repo-Name>.git
  或者用SSH
git remote add origin git@github.com:Monologue-N/<Repo-Name>.git

git branch -M main

git push -u origin main
```

---

**…or import code from another repository **

You can initialize this repository with code from a Subversion, Mercurial, or TFS project.
