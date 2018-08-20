---
title: "Terminal Setup"
slug: terminal-setup
---

# Making Your Terminal Professional

A developer lives in their terminal. So we're going to make our terminal pretty :D.

Use the keyboard shortcut `command` + `spacebar` and type "terminal" to open your terminal.

Now use the keyboard shortcut `command` + `,` to open your preferences (this keyboards shortcut works for every program on your computer!).

Set your profile to "Pro" and click "Default".

# Adding Oh-My-Zsh

Next we're going to enhance our terminal with [Oh-My-Zsh](https://github.com/robbyrussell/oh-my-zsh), a zsh shell configuration. (It will make your terminal pretty and work better).

Install oh-my-zsh by pasting in this command. (remember that the `$` is the beginning of you shell line, and do not include it when you paste.)

```bash
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Now close and restart your terminal and you should see a colorful little terminal prompt now.  

```bash
-> ~
```

# Making a dev or code directory

Any good developer has a well organized computer. Always keep your folders, files, and desktop clean and organized.

A best practice to organize your code projects is to create one folder called either `dev` or `code` in the root of your computer. Use your terminal to make this now.

```bash
-> ~ mkdir dev
-> dev
-> dev mkdir courses
```

Now you are in your dev folder. You should move your portfolio coding projects into this folder and also where you should instantiate all new portfolio coding projects.

Let's add more more thing which is a folder for your courses. In this folder you can make directories for your coursework.

```bash
-> dev
-> dev mkdir courses
```

# Cheatsheet

The faster you are on your keyboard, the faster you can learn to code.

As you start at Make School dedicate time to learning and improving your keyboard speed, especially manipulating text and keyboard shortcuts.

Here is a tool to find the keyboard shortcuts for any application you are using.

[Cheatsheet](https://www.mediaatelier.com/CheatSheet/)

Download and install it. Spend some time finding the keyboard shortcuts for your browser and Atom.

# Show Hidden Files

As a developer, it's often very useful to be able to see hidden files and folders in Finder. They're hidden because messing with them can cause problems, but we're fancy-pants developers and we're not afraid.

It's useful, because command line tools are installed in hidden folders, Git repositories live in hidden `.git` directories, your bash path file is a hidden file, etc.

To do this, type this command into your command prompt:

	$ defaults write com.apple.finder AppleShowAllFiles YES

Then restart Finder by right clicking the Finder icon while holding the *option/alt* key and choosing relaunch.

![Relaunch Finder](finderRelaunch.png)

> [info]
> It's easy to reverse this change - just follow the same steps, replacing `YES` with `NO`.
