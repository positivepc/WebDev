[Previous: Hyper Text Markup Language](HTML.md)

# GitHub Pages
Pranshu Gupta

## Git: A Version Control System
Git is a version control system used to track changes in files and coordinating work on those files among multiple people. It is built for speed, data integrity, and support for distributed, non-linear workflows. 

Git is available freely under the GNU General Public License for Windows, Linux and MacOS. See the follwing article to learn how to install Git on your machine: [Installing Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git). For Ubuntu Linux and Windows 10 with Bash the following commands work:

    $ sudo apt install git

After installing Git use the following commands for configuration:

    $ git config --global user.name "your name"
    $ git config --global user.email "your email"

To add a project to git, go to the project folder and e issue the `git init` command. Then, add the files which you want to track with Git `git add fileName`, if you want to add all the files in the project folder use command `git add .`

    $ cd projectFolder
    $ git init
    $ git add .

In order to keep track of the changes made, every time a developer modifies the project, he commits the changes and adds a descriptive message to the commit. If something is not right, the changes can be reverted by going back to a previous commit. 

    $ git add changedFileName
    $ git commit -m "descritive message"

A repository can have many branches, which may or may not be later merged with the development branch. This is useful in testing new ideas and features for the project, if a developer has some idea for a functionality to be added, he can create a new branch a write code and test the new feature. If all works well, this branch can be merged with the main branch. To create a new branch of code and start working in that branch use the following commands:

    $ git branch newBranchName
    $ git checkout newBranchName

To go to work in the old branch, simply enter `git checkout oldBranchName`. For merging the current branch with another branch, use the following command, you might have resolve conflicts if you make different changes in the same line of code on the two branches. Conflict resolution has to be done manually by inspecting the code. Git will show the two versions of the conflicting lines for each file, to resolve the conflict we just have to delete the line which we don't want. After resolving all the conflicts we can merge the branches as usual.

    $ git merge currentBranchName otherBranchName

[Git CheatSheet](https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf).

## GitHub Pages
GitHub is an online service which is built on top of Git. It allows teams of developers to work on the same project together, making their own changes in the repository and merging them time to time to a main release branch in a collaborative way. It is a great tool for Open Source Projects which are developed by thousands of developers from all over the world, e.g., Linux Kernel.

Here is a great introductory video of GitHub on YouTube, created by the GitHub team.

<iframe width="560" height="315" style="margin-top:2%;margin-bottom:2%;" src="https://www.youtube.com/embed/w3jLJU7DT5E" frameborder="0" allowfullscreen></iframe>

We can also use to publish our websites via GitHub. Creating a repository named "yourusername.github.io" is all it takes. We add a HTML file "index.html" as the home page along with other pages as per our requirements. We make changes to website, commit the changes and push them to the remote which makes the changes visible on the actual website.

<iframe width="560" height="315" style="margin-top:2%;margin-bottom:2%;"  src="https://www.youtube.com/embed/2MsN8gpT6jY" frameborder="0" allowfullscreen></iframe>

[Read this article: GitHub Pages](https://pages.github.com/)

In order to publish our website on github, we have create a repository named `username.github.io`, username should be your GitHub username. Now on our machine, we have to create an empty folder. In terminal (ubuntu) or in Git Bash (for windows), first enter in the folder which we just created by using the `cd` commamd:

    $ cd foldername

Now, we clone the repository by using the following command (please replace 'username' with your GitHub username in the command):

    $ git clone https://github.com/username/username.github.io

This will create the repository folder inside the folder we created in the previous step. Now enter into this folder (again by using the `cd foldername` command as per the folder name). After that, we create a HTML file named "index.html". In this file write HTML content as per your requirements, you can add CSS, Bootstrap etc. as well. 

Now, for each file that you have for your website, HTML, CSS, images, etc. issue the following command (or you can add all of them to Git in one go by using `git add .` command. Note that the '.' is important):

    $ git add filename

We have added the required files to git, we make our first commit:

    $ git commit -m "enter a short message here, describing the changes you made in the project"

To publish the website online, use the following command:

    $ git push origin master

The website should be online in a few minutes at username.github.io according to your username. For example, my username is 'Pranshu258' so my website will be up at:

[pranshu258.github.io](https://pranshu258.github.io)

[Next: Bootstrap](Bootstrap.md)