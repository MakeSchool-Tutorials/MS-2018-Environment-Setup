---
title: "Setting Up Atom"
slug: setup-atom
---

Download and install Atom. Atom is a an open-source text editor maintained by Github, that we will use to write code.

[https://atom.io/](https://atom.io/)

## Quick Aside on Alternatives

For the purpose of this set up, we'll use Atom as our default text editor. However, [VS Code](https://code.visualstudio.com/) is another highly recommended editor. It includes Git integration, and a solid debugger that will be helpful for finding issues in your code. You can customize it in a similar way to how we describe Atom below.

Choose whichever seems more appealing to you. You can always switch later, try both to see what you like! There's other text-editor options to explore as well!

# Atom General Settings

There's long been a religious war between proponents of tabs and spaces in source code. It's a particularly important topic in Python programming, because white space is actually part of the syntax. The Python Style Guide, known as [PEP8](https://www.python.org/dev/peps/pep-0008/) says that Python code should use only spaces, you cannot mix spaces and tabs, and that code blocks should be indented by 4 spaces each.

To make sure we don't mess this up, let's have Atom help us out by emitting 4 spaces when pressing the tab key.

> [action]
>
> 1. Go to Atom Preferences & Settings Tab
> 1. Find the Soft Tabs option.
> 1. Make sure it's checked.
>
> ![Soft Tabs Checked](softTabs.png)
>
> Then scroll down and make sure tabs emit 4 spaces:
>
> ![Tab Length 4](tabsLength.png)

# Embedded Terminal Window Package

Let's install a new package to our Atom instance to make it work better for us.

First we're going to get an embedded terminal in our Atom instance.

> [action]
>
> 1. In Atom hit `command` + `shift` + `p` and type "install package" and hit "enter". Now you are on the Install Packages settings page of Atom.
> 1. In the search bar type and install this package:
>
	```
	platformio-ide-terminal
	```
>
> 1. To turn this terminal on and off hit `control` + `~`.
>
> ![terminal window](terminal.gif)

# Column Select (Many Cursors!)

Atom already lets you use multiple cursors at the same time.

> [action]
>
> 1. Open a new file and type a Bart Simpson classic.
>
	```
	There is no such month as Rocktober
	There is no such month as Rocktober
	There is no such month as Rocktober
	There is no such month as Rocktober
	```
>
> 1. Now `command` + `click` anywhere on the text. You'll see you can make many cursors and make edits.
> 1. Now click on any of the "Rocktober's" and hit `command` + `D`. You can select and edit multiple instances.
> 1. To select and edit all the instances, put your cursor on "Rocktober" and hit `command` + `ctrl` + `G`.

But what about clicking and dragging many cursors? Let's install a package for that.

> [action]
>
> 1. Go back to the install settings page and type in this package and install it.
>
	```
	sublime-style-column-selection
	```
>
> 1. Now go back to your Bart Simpson phrases and hold `alt` and drag down the right side. of the text. Huzzah! Many cursors.
