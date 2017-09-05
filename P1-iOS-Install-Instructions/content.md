---
title: "iOS Install Instructions"
slug: ios-install-instructions
---

# iOS Environment

You should update and install your iOS development environment before the Python one, as the Python installers actually have some dependencies on the iOS tools.

## Mac OS and Xcode

To install Xcode 8, you need Mac OS 10.11.5 or newer, so you should install/upgrade that first if yours is older than that.

Then Xcode 8 is an easy download in the Mac App Store. After it's installed, you should open Xcode to allow it to do some additional installation and configuration. Note that if you have been using the beta version of Xcode 8 before, you need to delete this from your computer and then your Xcode 7 version will just be upgraded through the App Store (so you should end up with only one version of Xcode). 

Xcode 9 is still in beta so you should not install it yet.

## Command Line Tools

Next you should install Command Line Tools, which is a bundle of command-line based software for developers. It includes things like `git`, `gcc` and `clang`. For a complete list, see [this article](http://osxdaily.com/2014/02/12/install-command-line-tools-mac-os-x/).

Once Xcode 8 is installed, you can install Command Line Tools by running this command in terminal:

  $ xcode-select --install

> [info]
> Whenever you see code prefixed with a dollar sign $, that indicates that it's a command to be entered in the command prompt.

## Homebrew

Homebrew is a package manager for Mac OS. It makes it easy to install software packages while also installing and managing their dependencies. For more information, see the [Homebrew website](http://brew.sh/)

To install Homebrew, run this terminal command, which will download and run an install script:

    $ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

If you already have Homebrew installed, you need to update your formulae by running:

    $ brew update

This may take several minutes to download updates, so be patient while it completes.
