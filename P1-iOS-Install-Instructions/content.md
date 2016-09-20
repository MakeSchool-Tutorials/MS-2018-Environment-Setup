---
title: "iOS Install Instructions"
slug: ios-install-instructions
---

#iOS Environment

You should update and install your iOS development environment before the Python one, as the Python installers actually have some dependencies on the iOS tools.

##OS X and Xcode

To install Xcode 7, you need OS X 10.10.4 or newer, so you should install that first.

Then Xcode 7 is an easy download in the Mac App Store. After it's installed, you should open Xcode to allow it to do some additional installation and configuration.

##Command Line Tools

Next you should install Command Line Tools, which is a bundle of command-line based software for developers. It includes things like `git`, `gcc` and `clang`. For a complete list, see [this article](http://osxdaily.com/2014/02/12/install-command-line-tools-mac-os-x/).

Once Xcode 7 is installed, you can install Command Line Tools by running this command in terminal:

	$ xcode-select --install

> [info]
> Whenever you see code prefixed with a dollar sign $, that indicates that it's a command to be entered in the command prompt.

##Homebrew

Homebrew is a package manager for OS X. It makes it easy to install software packages while also installing and managing their dependencies. For more information, see the [Homebrew website](http://brew.sh/)

To install Homebrew, run this terminal command, which will download and run an install script:

	$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

If you already have Homebrew installed, you need to update your formulae by running:
	$ brew update

This may take several minutes to download updates, so be patient while it completes.
