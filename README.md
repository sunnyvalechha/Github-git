* Git is Free
* Git is opensource
* Git is Fast & Small as most of the operations are performed locally.
* Git is a version control system that is used to track changes in source code. Version controled can be done for anything like file, images, folder.

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

Some terms we used in a company:

Hotfix: A hotfix in Git is a type of branch that is used to quickly fix a critical bug in production. Hotfixes are typically created from the master branch and are merged back into master and develop once the fix is complete.

Practical:

git --version

mkdir git-project
cd git-project/
mkdir project{1..3}

Note: To create a repository run 'git init' inside a folder where we want to make a repository. There a hidden file is created called '.git'.

Tip: Once we transform a folder into repository do not create another repository into a repository.

/root/git-project/project1  >> git init  / git init repo-name 

**Git Stages**

1. Working Directory
2. Staging Area
3. Git repo

1. Any files which are placed in '**Working directory**' are **untracked**

git status

 ![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/2217d92b-2dce-4c56-953b-6558231b2511)

 git status -s >> See files which are not tracked

 A > added
 D > Deleted
 AM > Added & Modified
 ?  > Not added

git status -v  >> See modifications of file

2. Any file which is add by command 'git add filename' moved into staging area.

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/ef8664a1-dc6b-433e-9f59-245b13b5ccdc)

git reset >> Again move file from staging to working directory.

Note: If the directory is empty it will not go in Staging area

3. git commit -m "payment code commit 1" > This command move file from staging area to git repo.

* Suppose this file is deleted from our local system which is project1, we can recover the file by using 'git restore filename'

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/c7bacefa-53a2-489b-81d2-e06a1c61e466)

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/de9da6a5-e423-4d07-9aaa-62183b70605f)

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/f5d862f9-62cd-4d47-9411-e6ca98069789)

* **Add and commit specific file**

git add file1.txt

git commit file1.txt -m '1st comit of file1'


# Set Global Username and email

git config --global user.name sunny

git config --global user.email sunny@gmail.com

git config --list

git config --global core.editor '/usr/bin/vim'   > Set the default editor

* Any user is doing nasty things to the code, it can be tracked easily by using **global** settings and using command **'git log'**

git log

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/6726e8f8-7777-4ad2-8b34-86089d6f6ab8)

# Clone GitHub repository with Git

git clone command is clone the already created repository with CLI.

Go to Github > Go to repository which want to clone with CLI > Go to Code option > HTTPS > Copy URL > Example: https://github.com/sunnyvalechha/Azure-Dev.git

Go to CLI > run command 'git clone <URL>' 

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/7ab63f75-c65c-434f-87db-6581fe683ea1)

git remote -v  > Check, if this repository is connected with any GitHub or GitLab or Bitbucket Repository

In Git, "origin" is a repository in which we want to send data using push command.

To add remote connection with repository:

git remote add origin <url of repository>

git remote add origin https://github.com/sunnyvalechha/Azure-Dev.git

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/8b47f3e6-4eea-4269-ad90-d1cdc97728f8)

git status > Branch **master**

git push origin master > We have to create a branch master

Note: To run the above command, we must add and commit a file, means nothing should present on working directory, everything must be commited.

It will ask for password > Go to developer settings > Get you token > run command 

origin url is developer token url

another url is remote -v command url

git remote set-url origin https://abcxyz-your-dev-token@github.com/sunnyvalechha/Azure-Dev.git

git push origin master

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/dad3b61a-b0fe-4fa3-9f23-32bd82f5aadc)

# Git Fork

Forking a repository means creating a copy of the repo. When you fork a repo, you create your own copy of the repo. When several developers want to work on a project but need to make changes that are inappropriate for the original repository.

Note: Fork and Clone both have different features, clone will sync the local and remote only once and not update the content if there is any new changes in main, fork just create a copy of remote repo to your local and can be updated via 'sync fork', and the .git file also different in local and remote when done fork.

Sync Fork: Any changes in the main repository will updated in the fork repository.

# Git Branch

Branches allow you to work on different parts of a project without impacting the main branch.

When the work is complete, a branch can be merged with the main project.

You can even switch between branches and work on different projects without them interfering with each other.

Practical:

git branch > check how many branches

git checkout -b sunny-br-1  > created branch named 'sunny-br-1'

Note: If my branch is not main/master of any other branch so my origin of push will be that branch. Ex, below 

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/cdcb16f5-9800-422c-9c4f-521325f7609f)

* To see this > Go to repository > Go to Branches [1] > 

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/5da877b0-0e68-444e-be3d-528841297d40)

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/2f369765-9468-4868-9e16-041d6bace679)

**Create new Branch**

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/f1c5ba1c-eb08-49c3-9dac-ea6df53cb6da)

Note: Every time we create a new branch all the content of the old branch will copied to the new branch, but it will copy the content for the 1 time only. If any content will be added in the old branch will not updated in the new branch.

Get all commit list or get hash Id

git log 

git log --oneline

**Head** - Latest or Last commit is the Head

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/b5ad08ce-8583-4530-8a47-5fae6d14394d)

If created another branch and create another commit, then

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/47b16e00-c53a-4a62-a970-d7f9aa52adad)

Developer 2 has made some changes in feat-3 and commited

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/ea3119a0-e5ee-4f5b-82fb-4e3f3a0ab398)

Suppose, we want to revert the above commit that is '3.1'

git revert <commit id> # It will create another commit that will pointed to this reverted commit

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/1a801769-3ac5-4c93-9c8b-151fd572411b)

* We can reset the recent commits.

I want to reset the feature 3 in snap

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/961d3c42-9a61-42a4-a052-1819442032ca)

git reset 7946169

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/b4f2d4bd-23f6-4819-bb95-823ff59a3d55)

**Branching strategy**: 

Master (Protected Branch) No one can commit into this branch, this is where production code is kept.
Dev: Where all the developers will create their own branch names feat/b1, feat/b2

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/87526906-b21d-4318-874d-cc30b8ac02f7)

Option 2

Master (Protected Branch) nothing will be commit to master unless it test on staging and both environment code will be same.

Before staging a new branch will added called quality assurance (QA).

After QA a Dev branch will created where all the code have been commited.

So the flow will run like:

Dev (feat1, feat2) ---> QA (clone of Staging, run a code here in smaller env) ---> Staging Branch (clone of Master, test code at big env)  ---> Master (If everything runs good, code move here).

Note: If any issue reported into master a new branch will created called HOTFIX and once the bug is fixed again code pushed into master. Will not wait here to create multiple branches.

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/03d6df30-999e-4831-95e2-658fe99841f4)

# Inter ques - What are the branching strategy you follow in your Co.?

Branch:
1. Dev
2. Master
3. Staging

Dev: Developers use this branch, and every developer have their own branch like below, and all the tickets and features will merge in Dev.
     feat/color of UI
     feat/payment
     ticket/jira123
     
Master / Staging: Generally master and staging will be in sync. Staging also called as Production.

We merge our code from Dev branch to Master branch and Master to Staging.

Final: Based on my previous project we use 3 main branches Dev, Master and Staging, where Master was the main base branch, Dev was a branch where development use to happen and inside the development branch we used to create branches based on feature request.

Suppose we are using instagram to the feature we are using is the staging/production version and any changes will come in future is held in dev branch.


# Cherry Pick

Choosing a commit from one branch and applying it to another branch.

When to use cherry-pick?
Suppose a developer fails to recognize which branch he is currently on, and by mistake, he commits to another branch instead of committing to the main branch. Now to fix it, he has to first run git show, then save the commit, check out the main branch, apply a patch there, and commit with the same commit message. But all this can be done automatically by using just one command i.e. cherry-pick.

Practical:

Added feature in feat-2

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/64516772-1107-4997-8fde-0b14b5e707fd)


Then change branch again to Master, note that we have our commit id from old commit (4e044d2)

* Run from master branch

      git cherry-pick 4e044d2

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/9c8e9fa3-e362-4c10-b545-23c8c6db87aa)

# Git Merge

When you are sure that your code is ready to merge use.

git merge branch-name

I am at branch 3, I want to merge 2 with 3

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/4fe03998-f561-41e8-8939-83367cc2a0d5)

git merge sunny-br-2  > If asking any comments to add in file, put statement why we are doing this.

**Merge from UI**

After pushing a commit to github, from the UI it gave option if we want to merge. Preferred method is from UI

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/1a9d8309-37e2-42d3-89a1-ecc4a61cd62d)

# Git Rebase

Git rebase can integrate the changes from one branch to another by overcoming the problems that we might have faced while using the git merge command. The changes we will do will be recorded in the form of logs which are useful to go through if any mistakes happen.

Rebase and merge used for same purpose.

I am at master branch and have 2 commits 

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/1be63896-07c6-4f66-b2c5-ff049258b99d)

I want to merge the HISTORY of both branches, Switch to branch Dev

Run: git remote add origin https://github.com/sunnyvalechha/Azure-Dev.git

    git pull origin main --rebase

![image](https://github.com/sunnyvalechha/Github-git/assets/59471885/2f0e768a-4177-4e5c-80cb-57e6668bf2e3)

If all fine, then run 'git push origin master' with the help of Personal access token




