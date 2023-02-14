# Git and GitHub + Pages

## What is git?

Git is a **source-control manager** made my Linus Torvalds, Mr. Linux himself. It is a tool that is used to track changes made to a project, add new features, and more. A git project is called a **repository** (repo for short). A repo is just a folder that you have told git to track changes in.

A source-control manager is most useful when used in teams, and teams need some way to synchronize their work. Now, you could send emails back and forth with zip files attached, but that is not very elegant. GitHub is a site that people use to host their git repositories, making it simple to share, find, and contribute to code! Git handles synchronization, merging code, forking code, and much more!

You can use git without ever using GitHub, just like you can use HTML without ever touching a server or watch a video without going to YouTube. GitHub is simply a place to put your git repos.

An example of a large code base is with an application and code editor called (Visual Studio Code) [https://github.com/microsoft/vscode]. This is an example of how large a repository can get, as well as showing that thousands of people can contribute to projects to make them better in a communitive effort.

We will be using Visual Studio code in a bit, don't worry, you do not have to install anything to do this. GitHub has some integration built in that makes for a easy way to make some touch ups.

## Setup

1. Make a free GitHub account
2. Install git on your local machine
3. Install the GitHub Desktop Client on your local machine

### Mac/Linux

Git should already be installed for you. Open a terminal and type `git --version`. If this does not work, you will have to install git.

### Windows

You may not have git installed. Open up a terminal and type `git --version`. If this does not work, install git from [git scm](https://git-scm.com/downloads). When prompted, we suggest that you select "use Git and optional Unix tools from the Windows Command Prompt" during the installation. 

###GitHub Desktop

The GitHub desktop client allows you to interact with Git through a Graphical User Interface (GUI). It makes it easier to see your changes, make commits, pull, push, and many other actions you can execute through the command line. The GUI executes the command line GIT commands when you push changes, or whatever else you are doing with the repository. As the wise Dr.Maletic said, "You can get yourself in trouble with GIT in about 30 seconds", using the desktop client will cut out possible mistakes in typing commands out would be.

First we need to sign into the GitHub account that was created previously to be able to commit our changes to a repository. To do so, follow the steps below
1. Open the GitHub Desktop client
2. In the top menu bar, click on File, then Options
3. In the left hand side of the options menu, click on Accounts
4. Click the "Log In" buttion under the GitHub.com option.
5. Click "Continue with browser", this will open GithHub. Sigin in and grant GitHub Desktop Client the permissions to your GitHub account.
6. You should now be signed in, to check, go back to the desktop app, click File and then Options. In the accounts section, you should see your profile
7. You are now ready to continue and get into the lesson, lets learn about Git!

## Lesson

### GitHub

To get started, open up the GitHub Desktop. First we need to create a repository, this is a place (or you can think of this as an container) to hold all of you project files and folders. To create a repository, first click File, then click New Repository. Type in a name, what ever you want to call it, a description if you desire to, then click "Create Respository".

We have created a repository, to save it to GitHub, as GitHub has its own servers that store your code on, we will publish the repository to GitHub. Click "Publish Respository". Double check the details of the repository and ensure they are correct. If you want the repository to be able to be viewed by anyone, ensure that the "Keep this code private" option is not checked and click publish.

If you visit GitHubs website and click your profile picture, then your repositories, you should see the repository we just made in the desktop app, you can click to view the contents, but there will be nothing in there. So lets add some content to this repository to make it more useful.

To create a file, go back to the desktop app and ensure that the repository you created is the current repository selected (This is found in the left corner under current repository). Next, click show in explorer this is the local version of the repository on you machine and where all of the files from pulled repositories will live.  Then open notepad on windows or text edit on mac. Be sure to go to Format, then plan text mode.

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


###Badges With Sheidls.io
We can add badges to our repository in the README file, this can give some information to the public about key parts of the repository. For example, what branches have passed security checks. Green could mean that it is secure and passed the checks and red could mean it failed.

To add a badge to the README.md in our repository, first go to (Shields.io)[https://shields.io/], then fill out the lable, message, and color boxes. Click Make Badge, you will be lead to a site with your badge.

To put this into GitHub, copy the link in your address bar, this points to the actual badge and put it into the README file.

To do this, we will use Visual Studio Code, which has an online version baked into GitHub. Navigate to your repository in GitHub, then press the full stop/ period(.). This will open an online version of VS Code. Then navigate and click on the icon with two files on the left menu bar, this opens the file explorer. Next click README in the list of files.

Then add the follow Makrdown to the top of your README and replace LINK TO BADGE with the link to the badge we just created.

![alt text for screen readers](LINK TO BADGE "Text to show on mouseover").

After doing so, you will notice a number appear near an icon with a branch. This is the source control section. To commit and save changes, click the source control icon, type in your description and message, then click Commit & Push.

Click back to go back to the repository page, then refresh the page.

You should now see your shiny new badge!


Issues is a list of changes that need to be made to the project, pull requests are possible fixes for those issues submitted by people who want to contribute to the project, and projects are collections of issues. If you click the "Settings" tab, you will be taken to your repo settings. On the left hand side, click the option called "Pages". 



### Pages

Right now, the repository does not have a website to show vistors.


To fix this problem, make a file in your local repo called `index.html` and insert some HTML into it. 

To do this, we will use Visual Studio Code, which has an online version baked into GitHub. Navigate to your repository in GitHub, then press the full stop/ period(.). This will open an online version of VS Code.

You can also add CSS and JavaScript files if you want and include them like usual. Use the desktop client to commit the files to the repository, then push them. If you try to visit your GitHub pages link now, it should work.

You can also use markdown to write your site if you prefer, and give it nice, responsive, pre-made styles using Jeckyll. This can be configured from the pages settings page. 

Commit and Push your changes, then visit your new site. The format for GitHub Pages links is usally https://{username}.github.io/{file}

Index.html is usally hidden in the address bar as GitHub is smart enought to know where to go for index.


###Pull Request Example

We have a github repository set up with a GitHub Page, the issue is, we have some large spelling mistakes in the site. To fix these, we will do pull requests withe the changes each person makes to give everyone an idea and a feel for pull requests.

Please visit the [GitHub Repository] () for the files. Next after you are at the repositories GitHub repository, click Code, then click, Open in Desktop Client. This will pull the repository to your local machine. Open the repsitory like normal, then make a change.

After the change is saved. 