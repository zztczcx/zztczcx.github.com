---
layout: post
title: "Pro Git Notes"
description: ""
category: 
tags: []
---
{% include JB/setup %}

##这里记录一下我看***Pro Git*** 的一些笔记##

Git是一个分布式版本控制系统（Distributed Version Control Systems).
在Git中每一次提交（commit）或者保存你项目的状态，Git就会记录下那一刻文件的样子并且记录一条参考。为了有效，文件如果没有变动，Git不会重写存储一遍而只是对之前文件的一个链接（link）。

Git下的文件有三种主要的状态：committed，modified和staged。
-Committed 意为数据安全的存储在了本地的数据库中。
-Modified 意为你已经改变了文件但并没有commit 到数据库中。
-Staged 意为你已经标记了一个改动过的文件在当前的版本中并将进入下一个commit snapshot。

###Git Setup###

~/.gitconfig file: Specific to your user. You can make Git read and write to this file specifically by passing the --global option.

###Checking Your Settings###

the git config --list command to list all the settings Git can find at that point:

``$ git config --list
user.name=Scott Chacon
user.email=schacon@gmail.com
color.status=auto
color.branch=auto
color.interactive=auto
color.diff=auto
...``

###Initializing a Repository in an Existing Directory###

``$ git init``

This creates a new subdirectory named .git that contains all of your necessary repository files

git add commands that specify the files you want to track

``$ git add *.c``

###Cloning an Existing Repository###

You clone a repository with git clone [url]

``$ git clone git://github.com/schacon/grit.git``

That creates a directory named grit, initializes a .git directory inside it, pulls down all the data for that repository, and checks out a working copy of the latest version.

###Checking the Status of Your Files###

The main tool you use to determine which files are in which state is the *git status* command.

###Ignoring Files###

you can create a file listing patterns to match them named *.gitignore*

###Committing Your Changes###

you can type your commit message inline with the commit command by specifying it after a -m flag

``$ git commit -m "Story 182: Fix benchmarks for speed"``

“Changed but not updated” (that is, unstaged)

###Unmodifying a Modified File###

Even commits that were on branches that were deleted or commits that were overwritten with an --amend commit can be recovered 

``$ git checkout -- benchmarks.rb``










