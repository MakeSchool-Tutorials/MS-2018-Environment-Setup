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

# Show Hidden Files

As a developer, it's often very useful to be able to see hidden files and folders in Finder. They're hidden because messing with them can cause problems, but we're fancy-pants developers and we're not afraid.

It's useful, because command line tools are installed in hidden folders, Git repositories live in hidden `.git` directories, your bash path file is a hidden file, etc.

To do this, type this command into your command prompt:

	$ defaults write com.apple.finder AppleShowAllFiles YES

Then restart Finder by right clicking the Finder icon while holding the *option/alt* key and choosing relaunch.

![Relaunch Finder](finderRelaunch.png)

> [info]
> It's easy to reverse this change - just follow the same steps, replacing `YES` with `NO`.

# Setting Up Git and Github

Git and Github are super important and awesome tools for tracking, revising, and collaborating on code projects. Let's get your computer setup to use Git and Github.

# First - install Git

	```bash
	$ brew install git
	```

Head over to [github.com](github.com) and sign up for an account using your personal email address if you don't already have one.

# Second - Configuring Git

1.  Configure your global username and email address.

**‼️ IMPORTANT: If you skip this step, Git will produce a warning each time you push to a remote branch.**

    ```bash
    $ git config --global user.name "Dani Roxberry"
    $ git config --global user.email "dani@bitoriented.com"
    ```

1.  Optional. Configure additional, helpful settings:

    * [**macOS/Linux**] Set the default text editor to VSCode:

      ```bash
      $ git config --global core.editor atom
      ```

1.  Double-check your settings:

    ```bash
    $ git config --list

    credential.helper=osxkeychain
    user.name=Dani Roxberry
    user.email=dani@bitoriented.com
    url.ssh://git@github.com/.insteadof=https://github.com/
    mergetool.keepbackup=false
    core.excludesfile=/Users/dani/.gitignore_global
    core.editor=code
    filter.lfs.required=true
    filter.lfs.clean=git-lfs clean -- %f
    filter.lfs.smudge=git-lfs smudge -- %f
    filter.lfs.process=git-lfs filter-process
    ```

# Generating and Configuring SSH Keys

1.  Run the following commands.

    **‼️ IMPORTANT: DO NOT ENTER A PASSWORD WHEN PROMPTED**. Just hit enter.

    ```bash
    $ ssh-keygen -t rsa -C "your.email@example.com" -b 4096
    $ cat ~/.ssh/id_rsa.pub

    ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQC+SJSGSCeSeLnOg543Hyqh3OcAENvugks8ygkoOkEA4g652gK0ES7CjjpBy4GS/XnaUWiD9iaoE4soE8dqhe/psCoiU+QxGmkjNapLtQAOu1W2v/SEh3Jao+rtfop0S+Ak96fiOVgUgupFAN1FXV1iYdpwyk7rR3Kv/T2M9Ce06Bk5KupdgNzF7Eg/tmFx8H2yVmeQ2J3MWM948ZvWmbBwtbcDRQ6ZtnXSoEof1Wg8agzyisq0Yoi3rXqAIxr1Hevs4g79Lrf65548yTfqZqyljSFA/h4VntXsZYKIWoXti5uPstrwRF6oaH8dm1l74jLAKC/XlqnsqVkRWn/Updj+x8g3+EdtFiWpUwEIMWWDbjPk0HHTfOS06716Hcji0hg4Kfipe03QjhD8Vqp/snaYCb8R3OSZOK1H3Zj9n1JgHhOoFYzk0gstV9DGRmrm2ywrQh3Q7fs23pzrZARGBhRHwk5XfFQl85D7oJffBbfpqjDdyzcHYOAo3mlDfwkfl1nHxynWrwCk+0KKD0zLVsqtkSVlNfQv2JqSSc6ox6vktO7RWKg5/T0b9r0fnNcYfGBVnoJDulJPJr7ynSUDRi2hX5WpMDomylUahVYN/VlAZBwvuWdOM0h3ZUsQEPjauN0k+mY3nQVTIa0hWl1vszTddcxLZKK5mJsvlnL7HMBQxQ== dani@bitoriented.com
    ```

1.  With your mouse, highlight the entire [public key](https://en.wikipedia.org/wiki/Public-key_cryptography), beginning with `ssh-rsa` and ending with your email address. Copy the highlighted public key to the clipboard.

1.  Add the key to [**GitLab**](http://ucb.bootcampcontent.com/profile/keys):

    * Click the above link and paste your key in the 'Key' section and give it a relevant 'Title'. Use an identifiable title like 'Work Laptop - Windows 7' or 'Home MacBook Pro 15'.

    * **Make sure you copied the entire key starting with `ssh-rsa` and ending with your email.**

    * Test your setup by running `ssh -T git@example.com` (replacing `example.com` with your GitLab domain) and verifying that you receive a `Welcome to GitLab` message.

      * Test using our Class Repository with this command: `ssh -T git@ucb.bootcampcontent.com`

      * You should receive the following output:

        ```bash
        $ ssh -T git@ucb.bootcampcontent.com

        Welcome to GitLab, Dani Roxberry!
        ```

1.  Add the key to [**GitHub**](https://github.com/settings/ssh/new):

    * Click the above link and paste your key in the 'Key' section and give it a relevant 'Title'. Use an identifiable title like 'Work Laptop - Windows 7' or 'Home MacBook Pro 15'.

    * **Make sure you copied the entire key starting with `ssh-rsa` and ending with your email.**

    * Test your setup by running `ssh -T git@github.com`:

      ```bash
      $ ssh -T git@github.com

      Hi droxey! You've successfully authenticated, but GitHub does not provide shell access.
      ```
