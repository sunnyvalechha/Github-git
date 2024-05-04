Git: Git is a version control system that is used to track changes in source code. Version controled can be done for anything like file, images, folder.

Repository in Git: The repositories of Github act as essential places for storing the files with maintaining the versions of development. By using GitHub repositories developers can organize, monitor, and save their changes of code to their projects in remote environments. 

Version control is of two types:
1. Centralized version control (CVCS)
2. Distributed version control system (DVCS)

CVCS: A central repository is a singular storage location for all data. There will be just one repository and that will contain all the history or version of the code and different branches of the code but if the repository had failed due to any issue so all the data will be lost.

DVCS: The only major difference you will find here is, instead of one single repository which is the server, here every single developer has their own server and they will have a copy of the entire history or version of the code and all of its branches in their local server or machine.

**Git is Distributed version control system**

Substitute of GitHub:
1. Gitlab
2. Bitbucket
3. Azure Devops
4. Aws cloud formation

Git is a technology and GitHub is a platform which uses Git's technology.  

If we put anything in git it will have following features.
1. Version (v1, v2)
2. Time
3. Author
4. Hash Id

Practical:

mkdir git-project
cd git-project/
mkdir project{1..3}

Note: To create a repository run 'git init' inside a folder where we want to make a repository. There a hidden file is created called '.git'.

Tip: Once we transform a folder into repository do not create another repository into a repository.

/root/git-project/project1  >> git init

**Git Stages**

1. Working Directory
2. Staging Area
3. Git repo

1. Any files which are placed in '**Working directory**' are **untracked**

 ![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/2217d92b-2dce-4c56-953b-6558231b2511)

2. Any file which is add by command 'git add filename' moved into staging area.

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/ef8664a1-dc6b-433e-9f59-245b13b5ccdc)

git reset >> Again move file from staging to working directory.

3. git commit -m "payment code commit 1" > This command move file from staging area to git repo.

* Suppose this file is deleted from our local system which is project1, we can recover the file by using 'git restore filename'

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/c7bacefa-53a2-489b-81d2-e06a1c61e466)

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/de9da6a5-e423-4d07-9aaa-62183b70605f)

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/f5d862f9-62cd-4d47-9411-e6ca98069789)


# Set Global Username and email

git config --global user.name sunny

git config --global user.email sunny@gmail.com

git config --list

* Any user is doing nasty things to the code, it can be tracked easily by using **global** settings and using command **'git log'**

git log

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/6726e8f8-7777-4ad2-8b34-86089d6f6ab8)

