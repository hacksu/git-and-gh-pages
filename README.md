# Git and GitHub + Pages

## What is git?

Git is a **source-control manager** made my Linus Torvalds, Mr. Linux himself. It is a tool that is used to track changes made to a project, add new features, and more. A git project is called a **repository** (repo for short). A repo is just a folder that you have told git to track changes in.

A source-control manager is most useful when used in teams, and teams need some way to synchronize their work. Now, you could send emails back and forth with zip files attached, but that is not very elegant. GitHub is a site that people use to host their git repositories, making it simple to share, find, and contribute to code! Git handles synchronization, merging code, forking code, and much more!

You can use git without ever using GitHub, just like you can use HTML without ever touching a server or watch a video without going to YouTube. GitHub is simply a place to put your git repos.

## Setup

1. Make a free GitHub account
2. Install git on your local machine

### Mac/Linux

Git should already be installed for you. Open a terminal and type `git --version`. If this does not work, you will have to install git.

### Windows

You may not have git installed. Open up a terminal and type `git --version`. If this does not work, install git from [git scm](https://git-scm.com/downloads). When prompted, we suggest that you select "use Git and optional Unix tools from the Windows Command Prompt" during the installation. 

3. Configure your user information.

Make sure to run these two commands once you have installed git:

`git config --global user.name "Your name"`

`git config --global user.email "your@email.com"`

## Lesson

### Git

The first thing that we will do is create a folder to be our git repo. Wherever you want, create a folder by typing `mkdir github_testing` and then navigate to the folder by typing `cd github_testing`. 

Now that we have a folder, we can tell git to track what's inside of it by typing `git init` to make a **local** repo. If you list the files in the folder you won't see anything different, but there is a hidden .git directory inside of it now, visible by typing `ls -a`. We will never need to interact with this folder directly.

Now that we have an empty git repo, let's make a file inside of it called `README.md`. This file will contain information about our repository written in [markdown](https://www.markdownguide.org/cheat-sheet/), a simple markup language like HTML. In fact, you are reading this repo's README right now. GitHub will show this file to anyone who visits your repo's page.

Inside of your README.md, insert this text:

```markdown
# My first README

This is my first README! It uses *fancy* **shmancy** MARKDOWN!
```

Save your file and then type `git add README.md` to tell git that you want to add the changes you made to this file.

After that, type `git commit -m 'added README'` to commit your changes to the repo. This makes a checkpoint that you can send to GitHub or come back to later.

### GitHub

Now that we have a repo that we want to share, we can make a space for it on GitHub and then **push** our existing code onto GitHub. Click the '+' at the top right of GitHub and then click "New repository". 

On the next page, you will need to name the repo on GitHub (the **remote** repo). We will name it similarly to how the local repo is named: `github_testing`. Make the repo public, and uncheck all of the boxes at the bottom. Finally, click "create repo".

Now we have a local repo and a remote repo. The last step is to link them together. On your local machine, type `git remote add origin https://github.com/YOUR_USERNAME/github_testing.git`. This command tells your local repo that there is a space for it to go online at that url and to call it "origin". Next, we are going to create the branch to work on with `git branch -M master`. And finally we will put our README on the remote repo by typing `git push -u origin master` which **pushes** our commited changes on branch **master** to the remote **origin**.

Refresh your browser and you should see your README being displayed! Now anyone with an internet connection could download your repo, make changes to it, and then ask you to bring the changes into the main repo. GitHub also offers more than just repository hosting. They offer a whole suite of project organization tools. They can be found in the tabs at the top, such as "Issues", "Pull Requests", and "projects".

Issues is a list of changes that need to be made to the project, pull requests are possible fixes for those issues submitted by people who want to contribute to the project, and projects are collections of issues. If you click the "Settings" tab, you will be taken to your repo settings. Scroll down and click on "Pages". 

### Pages

GitHub Pages is a way to host a webpage for your projects, yourself, or your organization right from a repo. It starts out disabled, and can be enabled by selecting a source branch from the repo. Do this by clicking on the dropdown that says "None" and selecting "master". Then hit save to make your changes take effect. Your site will be available at `https://YOUR_USERNAME.github.io/github_testing/`. The only problem is that GitHub will not know which file to show people who visit that link.

To fix this problem, make a file in your local repo called `index.html` and insert some HTML into it. You can also add CSS and JavaScript files if you want and include them like usual. Use `git add` to add all of these files to the repo, and then use `git commit` to commit them. Once this is done, push them to the remote repo by using `git push`. If you try to visit your GitHub pages link now, it should work.

You can also use markdown to write your site if you prefer, and give it nice, responsive, pre-made styles using Jeckyll. This can be configured from the pages settings page. 