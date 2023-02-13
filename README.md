# Git and GitHub + Pages

## What is git?

Git is a **source-control manager** made my Linus Torvalds, Mr. Linux himself. It is a tool that is used to track changes made to a project, add new features, and more. A git project is called a **repository** (repo for short). A repo is just a folder that you have told git to track changes in.

A source-control manager is most useful when used in teams, and teams need some way to synchronize their work. Now, you could send emails back and forth with zip files attached, but that is not very elegant. GitHub is a site that people use to host their git repositories, making it simple to share, find, and contribute to code! Git handles synchronization, merging code, forking code, and much more!

You can use git without ever using GitHub, just like you can use HTML without ever touching a server or watch a video without going to YouTube. GitHub is simply a place to put your git repos.

## Setup

1. Make a free GitHub account
2. Install git on your local machine
3. Install the GitHub Desktop Client on your local machine

### Mac/Linux

Git should already be installed for you. Open a terminal and type `git --version`. If this does not work, you will have to install git.

### Windows

You may not have git installed. Open up a terminal and type `git --version`. If this does not work, install git from [git scm](https://git-scm.com/downloads). When prompted, we suggest that you select "use Git and optional Unix tools from the Windows Command Prompt" during the installation. 

##REMOVE: 3. Configure your user information.

Make sure to run these two commands once you have installed git:

`git config --global user.name "Your name"`

`git config --global user.email "your@email.com"`


###GitHub Desktop

The GitHub desktop client allows you to interact with Git through a Graphical User Interface (GUI). It makes it easier to see your changes, make commits, pull, push, and many other actions you can execute through the command line. The GUI executes the command line GIT commands when you push changes, or whatever else you are doing with the repository. As the wise Dr.Maletic said, "You can get yourself in trouble with GIT in about 3 minutes", using the desktop client will cut out possible mistakes in typing commands out would be.

First we need to sign into the GitHub account that was created previously to be able to commit our changes to a repository. To do so, follow the steps below
	1. Open the GitHub Desktop client
	2. In the top menu bar, click on File, then Options
	3. In the left hand side of the options menu, click on Accounts
	4. Click the "Log In" buttion under the GitHub.com option. (It is important that it is the GitHub.com option, as the other is for enterprise accounts, 		which are set up diffrently).
	5. Click "Continue with browser", this will open your default web browser and direct you to the GitHub signin page. Sigin in and grant GitHub Desktop
		Client the permissions to your GitHub account.
		
	6. You should now be signed in, to check, go back to the desktop app, click File and then Options. In the accounts section, you should see your profile 	under GitHub.com
	7. You are now ready to continue and get into the lesson, lets learn about Git!

## Lesson

### GitHub

To get started, open up the GitHub Desktop. First we need to create a repository, this is a place (or you can think of this as an container) to hold all of you project files and folders. To create a repository, first click File, then click New Repository. Type in a name, what ever you want to call it, a description if you desire to, then click "Create Respository".

We have created a repository, to save it to GitHub, as GitHub has its own servers that store your code on, we will publish the repository to GitHub. Click "Publish Respository". Double check the details of the repository and ensure they are correct. If you want the repository to be able to be viewed by anyone, ensure that the "Keep this code private" option is not checked and click publish.

If you visit GitHubs website and click your profile picture, then your repositories, you should see the repository we just made in the desktop app, you can click to view the contents, but there will be nothing in there. So lets add some content to this repository to make it more useful.

To create a file, go back to the desktop app and ensure that the repository you created is the current repository selected (This is found in the left corner under current repository). Next, click show in explorer this is the local version of the repository on you machine and where all of the files from pulled repositories will live. 

A useful file that many GitHub repositories have is called a README file, this is what is displayed when someone views a repository. This file usally contains information on what the repository is, the tech stack/technologies used, credits to others that contributed, compiling instructions, running instructions, and many other details. This file will contain information about our repository written in [markdown](https://www.markdownguide.org/cheat-sheet/), a simple markup language like HTML. In fact, you are reading this repo's README right now. GitHub will show this file to anyone who visits your repo's page.

```markdown
# My first README

This is my first README! It uses *fancy* **shmancy** MARKDOWN!
```

Save the file and go back to the desktop client, the main part of the screen will be different now, and will show the new README file on the left hand side.

Next, to save it to the Git servers, we have to do a commit. If you are wondering what a commit is, it is submitting the files to a server to then save a currnt copy of. So if your laptop falls into a valcano, and if you commited your files, you will be able to pull those files down to your new device and keep working. 

In the bottom left hand corner of the desktop client, there is a place to put a title in and a description of your changes. Once you fill those out, it helps to be a bit descriptive if you can to help others understand what was chaged, click commit to main, then click push.

Main is a branch, in Git you have the idea of branches. Think of them like a tree, each branch has leaves (in our case files), but the trunk (in this case main) is where branches stem from. Branches allow for the main code base to be untouched will making changes to the code in a isolated verion of the files (branch), then a pull request is put in. This "Pulls the changes" up to the main branch. Merging then takes the code in a branch and updates the main branch with the new, changed code.

Refresh your browser and you should see your README being displayed! Now anyone with an internet connection could download your repo, make changes to it, and then ask you to bring the changes into the main repo. GitHub also offers more than just repository hosting. They offer a whole suite of project organization tools. They can be found in the tabs at the top, such as "Issues", "Pull Requests", and "projects".

Issues is a list of changes that need to be made to the project, pull requests are possible fixes for those issues submitted by people who want to contribute to the project, and projects are collections of issues. If you click the "Settings" tab, you will be taken to your repo settings. Scroll down and click on "Pages". 


### Pages

GitHub Pages is a way to host a webpage for your projects, yourself, or your organization right from a repo. It starts out disabled, and can be enabled by selecting a source branch from the repo. Do this by clicking on the dropdown that says "None" and selecting "master". Then hit save to make your changes take effect. Your site will be available at `https://YOUR_USERNAME.github.io/github_testing/`. The only problem is that GitHub will not know which file to show people who visit that link.

To fix this problem, make a file in your local repo called `index.html` and insert some HTML into it. You can also add CSS and JavaScript files if you want and include them like usual. Use `git add` to add all of these files to the repo, and then use `git commit` to commit them. Once this is done, push them to the remote repo by using `git push`. If you try to visit your GitHub pages link now, it should work.

You can also use markdown to write your site if you prefer, and give it nice, responsive, pre-made styles using Jeckyll. This can be configured from the pages settings page. 