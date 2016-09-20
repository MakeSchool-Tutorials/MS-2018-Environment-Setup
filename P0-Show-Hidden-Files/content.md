---
title: "Show Hidden Files"
slug: show-hidden-files
---

As a developer, it's often very useful to be able to see hidden files and folders in Finder. They're hidden because messing with them can cause problems, but we're fancy-pants developers and we're not afraid.

It's useful, because command line tools are installed in hidden folders, Git repositories live in hidden `.git` directories, your bash path file is a hidden file, etc.

To do this, type this command into your command prompt:

	$ defaults write com.apple.finder AppleShowAllFiles YES
	
Then restart Finder by right clicking the Finder icon while holding the *option/alt* key and choosing relaunch.

![Relaunch Finder](finderRelaunch.png)

> [info]
> It's easy to reverse this change - just follow the same steps, replacing `YES` with `NO`.