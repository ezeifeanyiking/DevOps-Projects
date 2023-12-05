# INITIALIZING A GIT REPOSITORY AND MAKING COMMITS

## WHAT IS GIT?
Git is a free and open-source distributed version control system (VCS) that tracks changes in source code during software development. It was created by Linus Torvalds, the creator of the Linux operating system.

Git essentially solves the problem of sharing code efficiently and keeping track of changes made to source code.

Before git, there were other technologies that solves this problem and a good example is SVN. 

Subversion (SVN) is an open-source centralized version control system that manages changes to files and directories over time.

The way that SVN solved this problem posed some challenges. In SVN there exist a central source code repository. Every change by developers is made against this central repository. This setup makes it difficult to collaborate because changes can only be made one at a time. Secondly, if for any reason the central server goes down or is not reachable that effectively blocks the developers. 

Git adopted a different approach. It allows developers make their own copy of the central repository. That is why it is referred to as: **Distributed Version Control System**

## INITIALIZING A GIT REPOSITORY
### PREREQUISITE:
1. Install Git for your machine.
2. Install and Open your preferred terminal e.g: iTerm, GitBash etc.
3. Navigate to the directory where you want to create your repository using `cd` command in the terminal. 
```Bash
cd Desktop/Folder1
```
## Now Initialize a git repository 
1. Run the following commands on your terminal to create your working folder or directory e.g: DevOps folder:
```Bash
mkdir DevOps
```
2. cd into the working directory using this command:
```Bash
cd DevOps
```
3. While you are inside this working directory enter this command:
```Bash
git init
```
This will initialize a new git repository within your current directory. You can verify it by running: 
```Bash
ls -a
```



