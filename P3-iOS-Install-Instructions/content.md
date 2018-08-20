---
title: "iOS Install Instructions"
slug: ios-install-instructions
---

You should update and install your iOS development environment before the Python one, as the Python installers actually have some dependencies on the iOS tools.

# Command Line Tools (ALL STUDENTS)

Install the Xcode Command Line Tools, which is a bundle of command-line based software for developers. It includes things like `git`, `gcc` and `clang`. For a complete list, see [this article](http://osxdaily.com/2014/02/12/install-command-line-tools-mac-os-x/).

Install Command Line Tools by running this command in terminal:

```bash
$ xcode-select --install
```

> [info]
> Whenever you see code prefixed with a dollar sign $, that indicates that it's a command to be entered in the command prompt. Don't include the $ when you paste the command in.

# Download Xcode (ONLY MOBILE STUDENTS)

To install Xcode 9, you need Mac OS 10.13.2 or newer, so you should install/upgrade that first if yours is older than that.

Then Xcode 9 is an easy download in the Mac App Store. After it's installed, you should open Xcode to allow it to do some additional installation and configuration. Note that if you have been using the beta version of Xcode 9 before, you need to delete this from your computer and then your Xcode 8 version will just be upgraded through the App Store (so you should end up with only one version of Xcode).

**DO NOT INSTALL Xcode 10** as it is still in beta.
