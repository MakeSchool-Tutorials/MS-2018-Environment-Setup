---
title: "Node Install Instructions"
slug: node-install-instructions
---

[Node.js](https://nodejs.org/en/) is a **server-side JavaScript runtime** and everyone will be learning how to build APIs using Node.js. Follow these instructions to install Node.js on your machine.

# Node.js

You will need Node.js to run packagers such as [npm](https://www.npmjs.com/), web servers like [Express](https://expressjs.com/), and build systems like [Webpack](https://webpack.js.org/).

> [action]
>
> Let's use Homebrew (the package manager we used to install Python) to install node.
>
```bash
$ brew install node
```
>
> Now check your Node installation. Open the Terminal and type:
>
```bash
$ node -v
```
>
> You should see something like: `v6.11.3` or which ever version you installed.

Great work!

# npm & Nodemon

When you install Node.js you also get npm for free.

[npm](https://www.npmjs.com/) is the Node Package Manager—so as Homebrew is to Mac, so is npm to Node.js packages. npm is the fastest growing group of packages in the world of software engineering.

You can install node packages **globally** with the tag `-g` on your machine, or **locally** to one specific project with the tag `-s`. Let's install a web server watcher called [Nodemon](https://github.com/remy/nodemon) globally on your machine. We'll use Nodemon to start our node server projects and restart our projects as they change.

> [action]
>
> Let's install Nodemon with npm and then check it's current version.
>
```bash
$ npm install nodemon -g
$ nodemon -v
```

# Node.js Version Management with NVM

Node.js has many many versions, and different projects may require you to run a different version. To manage what version you are using, we'll use [nvm](https://github.com/nvm-sh/nvm/blob/master/README.md) - **Node Version Manager**.

> [action]
>
> **Step 1:** First we need to install NVM using a curl command. Follow the [install instructions](https://github.com/nvm-sh/nvm/blob/master/README.md#install--update-script) for installing using curl
>
```bash
$ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
```
>
> **Step 2:** Because we are using zsh ("Z-Shell") we need to add an nvm extension to our zsh configuration file: `.zshrc`. Open that file with this command.
>
```bash
$ atom ~/.zshrc
```
>
> **Step 3:** Edit that file and add the `zsh-nvm` plugin and the export command below. Follow the comments that say to ADD items. This should be somewhere around line 65 in the file
>
```bash
# ~/.zshrc
>
# ADD zsh-nvm to the plugins
plugins=(git zsh-nvm)
>
# this already exists
source $ZSH/oh-my-zsh.sh
>
# ADD THIS
# nvm
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```
>
> **Step 4:** either restart your terminal or source your rc with this command so the path you just exported is respected:
>
```bash
$ source ~/.zshrc
```
>
> **Step 5:** verify you got nvm installed correctly by running the following command. It should return the text `nvm` if your instance is working.
>
```bash
$ command -v nvm
# => nvm
```

Now you can list what versions of Node.js you have on your machine and see which one you are using!

    ```bash
    $ nvm ls
    $ nvm current
    ```

Great work!

> [info]
>
> **Read if Step 4 caused a `plugin 'zsh-nvm' not found` error:**
>
> 1. [Follow the removal instructions](https://github.com/nvm-sh/nvm/blob/master/README.md#removal) for nvm.
> 1. [Follow the installation steps for oh-my-zsh for this plugin](https://github.com/lukechilds/zsh-nvm#as-an-oh-my-zsh-custom-plugin).
>
> From there try running steps 4 and 5 again, and your error should hopefully be resolved! If not, please reach out to a Make School staff member for assistance.

# Postman REST Client

You'll be building APIs with Node.js (and other server stacks!) and you'll probably want to inspect them with a REST Client. There is a great free one called [Postman](https://www.getpostman.com/).

> [action]
>
> Please click the above Postman link and install the client for later use. You'll need it for BEW 1.1, which is part of the core curriculum that all students must take.


That's all for now, your environment should be ready to go!
