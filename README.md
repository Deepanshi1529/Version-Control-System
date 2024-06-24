# Git and Github - Version Control System
Version Contol System also known as software tools are used to track the changes in the source code.<br>
Main goal of using version control system:

+ To maintain the history of project
+ To contribute to open source
## Git
It is an open source version control tool used to handle projects, track changes in the souce code and allow multiple developers to work together. It is being set up locally in your personal computer.
## Github
Platform that uses git or it hosts the git repositories (these are the hidden folder that is provided by git and it keeps the track of all the changes) so that other developers can contribute, share the projects. Other than github we also use Gitlab.
## Working in GIT
### Prerequites
+ Setup the Git Bash in your local computer.
### Change in current directory
Change the directory to desktop or in simple words it means we are inside the desktop now.
```
cd desktop
```
List all items present
```
ls desktop
```
Create a folder named as project inside the desktop.
```
mkdir project
```
### Initializing empty Git repository
It is like a starting point of Git. A hidden folder <code>(.git)</code> is present is inside the project folder. 
```
git init
```
### Creating a file in git
Create a file <code>names.txt</code> inside the project folder.
```
touch names.txt
```
### To Write inside the file
+ Vim/Vi is the default text editor when git has to write a message
+ In order to insert text, press <code>i</code>
+ In order to exit, press <code>esc</code> then type <code>:wq or :x</code>
```
vi names.txt
```

Displaying text inside the file
```
cat names.txt
```
### Defining File Status
It gives the info about the files whose history is being tracked or not.
```
git status
```
### Commit the files
For Eg. I have made changes in the file but no one knows that this file is being created or any change is being done in it. In order to do that we commit the file.
```
git add names.txt
```
To add a message to git committed file
```
git commit -m "changes has been made"
```
In order to remove a file from commit
```
git retore -- staged names.txt
```
### History of Project
```
git log
```
this command will show the history of the project by history it means time, date, name, email id etc. for every change or modification being made in the project.

## Hosting our Project on Github
By hosting our project on Github means whatever changes we have made so far to our local project in git bash, these changes will be displayed in our github repository.
<br>
It takes place in three steps:
+ Create a new repository in our Github profile.
+ attaching the url(git repository)
+ pushing the changes in the main branch

```
git remote add origin URL
```
```
 git push -u origin master
```
initially, the main branch is master here but we can change it to main either by change in settings or in git u can write the command as <code>git branch -M main</code>
## Warning alert
In git bash, if u are initializing the git in master branch then make sure that while pushing the changes it is being set to the master branch. It will bring an errror if initizalizing and pushing changes are being done in different branches.
<br> Steps for that:
+ In Github, our newly created git repository has main branch named as <code>main</code>
+ but, by default in git bash we are initizaling the git in <code>master branch</code>
```
git init (while the main branch : master)
```
Now, change master -> main
```
git branch -M main
```
```
git remote add origin URL
```
Now, main -> master
```
git branch -M master
```
Now, push the changes
```
git push -u origin master
```
but, if u don't want to go through all these steps then simply, change the <code>default</code> branch as master and just write code in master branch.

## Working on Existing Project (Contribution to open-source)
There are a lot of open-source projects in which developers from all around the world contribute to the source codes but there is a catch in that, other developers directly cannot make changes to someones repositories instead, there is a concept of <code>fork</code> which is being used.
<br><br>
Concept of fork is defined as making a copy of the project in your own repository, it basically means downloading all the folder,files or anything present in that targeted repository to your own computer. Whatever changes which are being done in the forked repository will not be visible in the targeted project. In order to do that we further have a concept of pull request and merging.
<br>
Steps invloved for creating a fork:
+ Create a folder in desktop or any other location
+ git init
then, clone the URL of the forked repo
```
git clone URL
```
now, every detail will be downloaded in that project folder and then changes can be made.

## Concept of Pull Requests
We have created the fork of the main project, and changes has also been made in the forked project but now, we want these canges to be visible in the main project and in order to do that there comes a concept of <code>Pull Requests</code> 
+ New Branches for New Pull Reuqest
lets say we create a new branch as hello
```
git branch hello
```
Main branch -> Hello branch
```
git checkout hello
```
then, commit the changes to keep track
```
git add .
git commit -m "new branch created"
```
Now, push the changes (changes has been pushed into the hello branch)
```
git push origin hello
```
After this, the main contributors will review the pull requests, and may suggest some changes and then they will merge these changes into their main project.
Finally, u have contibuted to open-source!!!




 
