# Terminal (Git and GitHub)
*Before getting into things we have to explain some terms and methodologies*  
## Version Control  
A **version control** is a system allows its user to revert a file or project to a previous version, track modifications and modifying individuals, and compare changes.  
A Version Control is divided into three sections:
1. Local Version Control  
Which entails one database on the hard disk that stores changes to files.  
  
2. Centralized Version Control (**CVCs**)  
This system entails a single server storing all changes and file versions, which can be accessed by various clients.  
  
3. Distributed Version Control (**DVCS**)  
A **DVCS** allows clients to create mirrored repositories. These data backups can be easily be placed on the server to replace any lost information. This allows for collaboration in work and the completion of joint projects.  
  
## Git  
Git is a **DVCS** that stores data in a file made up from snapshots (pieces). Git mostly relies on local operations and can detect the presence of any corruption in the data, through tracking. Git will minimize the possibility of irreversible damage to files. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.  
  
**States**

Files in Git can reside in three main states: committed, modified and staged.

***Committed***

Data is securely stored in a local database

***Modified***

File has been changed but not committed to the database

***Staged***

Flagged a file’s changed version to be committed in the next snapshot  

![CMS](https://blog.udemy.com/wp-content/uploads/2015/08/image066.png)  

## Starting to Git !  

1. Fisrt. You need to download the application
2. Second. Perform some customization steps, which should only need to be completed once on any machine. These customizations include:
   1-Configuration of Variables
   2-Identity Setting
3. Third. Configure a default text editor, through [$ git config --global core.editor "your text editor"]
4. Forth. Check Settings, through [git config --list]

## Setting up a Git Repository  
### Importing
To import an existing project or directory into Git, through the **Terminal** move to the project directory.  
Then use the git init command through [$ git init].  
And to start tracking perform these:  
[$ git add *.c]  
[$ git add LICENSE]  
[$ git commit -m “any message here”]  

### Cloning  
To create a copy of your Git file perfom this:  
[$ git clone **URL**]  

## Workflow  
### Local Repository Structure  
1. Working Directory: The actual files reside here
2. Index: The area used for staging
3. Head: Points to the most recent commit  

![LRS](https://blog.udemy.com/wp-content/uploads/2015/08/image036.png)  
  
### Saving Changes  
In this stage files gonna be either tracked or not tracked. I it's tracked, then the file can be modified, unmodified, or staged, they are part of the most recent file snapshot. If the file is not tracked, then they can not be modified, unmodified, or staged, because they are not part of the last snapshot and do not currently reside in the staging area.  
### The Life Cycle of File Status  
After you edit a file, Git flags it as modified because of changes made after the previous commit. Then, you stage the modified file. And then, you commit staged changes.
![LCS](https://blog.udemy.com/wp-content/uploads/2015/08/image006.png)  

### Check File Status  
just trown this at the Terminal : [$ git status]  

### Tracking and Staging a New File, Committing, and Pushing Changes  
to track a single or several file apply:  
[git add filename] single  
[$ git add *] multible  

for commiting change/changes:  
[$ git commit -m “made change x,y,z”] single  
[$ git commit -a] multible  

for pushing a file online to be saved:  
[$ git push origin master]  

If you are not ready to commit changes but do not want to lose them either use; [git stash] and when commiting to commit [git stash apply]  

## Remote Repositories  
**Remote Repositories** is for collaboration on Github.  
### Seeing Your Remotes  
by using [git remote -v] you can see all remote URLs.
