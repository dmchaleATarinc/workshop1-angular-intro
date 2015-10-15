# workshop1-angular-into
###Goal###
Initial tutorial to clone and install repo. Collaborators to decouple and enhance app logic to industry standards.

### Getting Started
We will be working from your local computer to clone down a public repo from github.com to your desktop. Once in this directory is cloned locally, all files will be under .git version control. We will start with the initial boiler plate html file within the repo with the goal of decoupling and enhancing the logic of a very simple angular application. We will assume that you are working from a shell window from Desktop on your computer and an IDE of choice.

Type the following:

    git config --global url."https://".insteadOf git://

<br />
**Prequisite Actions**

**1.** Install an IDE of your choice (both are free and light weight)
* **Brackets.io**
[![Brackets](http://brackets.io/img/hero.png "Adobe Brackets")](http://brackets.io/)


* **VS Code**
[![VC Code](https://code.visualstudio.com/Content/images/hero-osx.png "VS Code IDE")](https://code.visualstudio.com/)


**2.** Install latest node.js <br />
* [Install Node.js](https://nodejs.org/en/) | [How to install Git on Windows](http://blog.teamtreehouse.com/install-node-js-npm-windows) | [How to install node on Mac](http://blog.teamtreehouse.com/install-node-js-npm-mac)

*If you already have node installed, and want to upgrade type the following:*

    sudo npm cache clean -f
    sudo npm install -g n
    sudo n stable

[See more about upgrading Node](http://davidwalsh.name/upgrade-nodejs)

*Verify node and it's package manager npm is installed correctly by typing the following:*

    node -v
This should output a version number **v0.12.0+**

    npm -v
This should output a version number **2.0.3+**


**3.** Install .git <br />
* [How to install git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
* [Git Cheatsheet](https://training.github.com/kit/downloads/github-git-cheat-sheet.pdf)

**4.** Configure .git profile

[Configure global .git profile](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)


If you haven't configured your global .git configuration on your computer, the first time you execute a command, you should be prompted to set a username and email at minimum- This is how public .git repositories will know who you are when you interact with them.

    git config --global user.name "John Doe"
    git config --global user.email johndoe@example.com
    git config to use *https://* instead of *git://

***Sidenote*** There are common problems with accesing github and other package registries under a firewall. A common log error for github is 'unable to connect to github.com' when running any commands to clone resources (`npm install, bower install, git clone`). The last git config command should fix this.

*Verify is installed correctly by typing the following:*

    git --version
This should output **1.9.0+**

<br/>


**Step One** - ***Cloning Repo***

This following command will reach out to the github.com to grab the repo listed the url, make an exact clone of it from the name, at you are running the command from

    git clone https://github.com/addevonly/workshop1-angular-intro.git

Navigate inside the repo

    cd workshop1-angular-intro

Verify repo is under version control and you have no local changes

    git status

<br/>

**Step Two** - ***Installing Repo***

The following command will point to a package.json file at root of your current your in to install required node modules

    npm install

The following command will point to a bower.json file at root of your current directory your in to install required bower packages (js,css,html)

    bower install

***Sidenote*** In Windows, npm doesn't recognize bower, try running: `./node_modules/bower/bin/bower install`

Open your IDE, and open the current folder from your desktop: **workshop1-angular-intro**. From here you can navigate around the directory and edit files that git will reflect

In your shell window run the following command to serve up the index.html in the browser:

    npm run serve
