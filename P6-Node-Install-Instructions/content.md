---
title: "Node Install Instructions"
slug: node-install-instructions
---

Node.js is a **server-side JavaScript runtime** and everyone will be learning how to build APIs using Node.js. Follow these instructions to install Node.js on your machine.

# Node.js

You will need Node.js to run packagers such as NPM, web servers like Express, and build systems like Webpack.

1. Let's use Homebrew (the package manager we used to install Python) to install node.

    ```bash
    $ brew install node
    ```

1. Now check your Node installation. Open the Terminal and type:

    ```bash
    $ node -v
    ```

1. You should see something like: `v6.11.3` or which ever version you installed.

Great work!

# npm & Nodemon

When you install Node.js you also get npm for free.

npm is the Node Package Manager—so as Homebrew is to Mac, so is npm to Node.js packages. npm is the fastest growing group of packages in the world of software engineering.

You can install node packages **globally** with the tag `-g` on your machine, or **locally** to one specific project with the tag `-s`. Let's install a web server watcher called [Nodemon](https://github.com/remy/nodemon) globally on your machine. We'll use Nodemon to start our node server projects and restart our projects as they change.

1. Let's install it with npm and then check Nodemon's current version.

    ```bash
    $ npm install nodemon -g
    $ nodemon -v
    ```

# Node.js Version Management with NVM

Node.js has many many versions, and different projects will require you to run a different version. To manage what version you are using, we'll use nvm - **Node Version Manager**.

1. Step one - Install NVM using a curl command:

    ```bash
    $ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash
    ```

1. Step two - Because we are using zsh ("Z-Shell") we need to add an nvm extension to our zsh configuration file: `.zshrc`. Open that file with this command.

    ```bash
    $ atom ~/.zshrc
    ```

1. Edit that file and add the `zsh-nvm` plugin and the export command below.

    ```bash
    # ~/.zshrc

    plugins=(git zsh-nvm)

    source $ZSH/oh-my-zsh.sh

    # nvm
    export NVM_DIR="$HOME/.nvm"
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
    ```

1. Step three - either restart your terminal or source your rc with this command so the path you just exported is respected.

    ```bash
    $ source ~/.zshrc
    ```

1. Step four - verify you got nvm installed correctly by running the following command. It should return the text `nvm` if your instance is working.

    ```bash
    $ command -v nvm
    # => nvm
    ```

1. Now you can list what versions of Node.js you have on your machine and see which one you are using.

    ```bash
    $ nvm ls
    $ nvm current
    ```

Great work!

# Insomina REST Client

You'll be building APIs with Node.js (and other server stacks!) and you'll probably want to inspect them with a REST Client. There is a great free one called [Insomina](https://insomnia.rest/). Please click this link and install the client for use.
