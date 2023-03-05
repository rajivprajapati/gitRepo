# gitRepo
In this Repository I'm going to put whatever i learnt about git
### Git vs GitHub
##### Git 
> Version Control tool work locally
##### GitHub 
> Hosting Plateform
## Basic Linux Commands:
```
ls
cd <folder-name>
cd ..
cd ../..
cd <path-of-folder>
mkdir <new-folder-name>
toch <file-name>
rm <file-name>
rm -d <folder-name>
```
![picture](https://git-scm.com/book/en/v2/images/lifecycle.png)

## Basic git commands:
```git init``` - to initialize your folder as a git repository, after this you will see that a __.git__ folder is created </br>.
```git status``` - to check the status of files.</br>
```git add <file-name>```- to add a single file into staging area.</br>
```git add .```- to add all newly created file into staging area </br>

### list staging files
```git ls-files```
### Git Commit:
> to save changes ( use this after the file get into staging area) </br>
```
git commit -m "your message"
```
> to add file into staging area and commit simultaniously use (note- this command works only for modified files not for newly created files).</br>
``` 
git commit -am "your message"
```
> to show all commits history (it will show history of branch in which you are)
```
git log
```
```
git log --oneline
```
![picture](https://blog.marvelapp.com/wp-content/uploads/2016/10/Git.png)
### Git Config:
>to configure your global config file </br>
```
git config --edit --global
```
> to change the default editor add follwing  
```
[core]
          editor = code --wait
 ```

> note that your default code editor will be vim to change in vim editor user following commands. <br>
> press ```i``` to insert text.<br>
> press ```wq``` to save and quit.<br>

### Timeline Travel:
```
git show commit-id
```
```
git show head~1
```
>to get into a specific commit state of project
```
git checkout commit-id
```
```
git checkout master
```
```
git checkout head
```
>
> checkout is read only command
> for example your made checkout to specific commit and after that you made some changes and then you make commits 
> but when you will come back to master branch head ```git checkout master``` all changes you made will disappear.<br>

### Git Revert:
> git revert is use to revert specific commit changes. it just changes that specific commit changes and not touch any other commit
```
git revert commit-id
```
### Git Reset:
>it is used to remove commit history till specific commit
>it can be used in three different forms
- ```git reset --mixed commit-id```
- ```git reset --hard commit-id```
- ```git reset --soft commit-id```
>in case of mixed commit history will be removed till commit-id and file in which will be affected will be removed from staging area<br>
>in case of hard commit history will be removed till commit-id and file which will be affected  will also be removed<br>
>in case of soft commit history will be removed till commit-id and file will be in staging area<br>

``` 
git reset <file-name>
```
>above command you can use to remove file from staging area.<br>
```
git checkout <file-name>
```
> you can use above command to remove changes made in file which is not in stagin area.<br>
> after reset to push the changes to remote repo <br>
```
git push -f
```
### GitHub :
> to host your local repo in github 
- create a repo in git hub 
```
git remote add origin <link of repo>
```
>to push your local repo in github
```
git push -u origin master
```
### Branching :
![picture](https://wac-cdn.atlassian.com/dam/jcr:389059a7-214c-46a3-bc52-7781b4730301/hero.svg?cdnVersion=962)
>when you crate a repo you are in a default branch master
>but you can create branch and work on that and when you are ok with your work you can merge that branch work on master branch
```
git branch <branch-name>
```
- to create a new branch
```
git branch
```
- to show list of branchees
```
git checkout <branch-name>
```
- to swith to a branch

```
git checkout -b <branch-name>
```
- the above command is used to  create and checkout to that branch simultaneously
```
git branch -D <branch name>
```
- to delete a branch
```
git pull origin <branch-name>
```
- to pull a branch from gitHub repo
```
git checkout --track origin/branch-name
```
```
git push origin --delete <branch-name>
```

### Merging Branches :
>branches can be merged in two ways 
- fast-forward
- 3 way merging

```
git merge <branch-name>
```
### Git Rebase :
![picture](https://git.logikum.hu/images/tutorials/merge-rebase/07.svg)
>git rebase is use to change the base point from where branch is created

### Fork and Clone :
> Fork is used to copy someones repo 
> clone is used to copy someones repo into you local machine
```
git clone <link>
```
### Collaboration and Contribution:
> in case of contribution you fork repo and make changes and then create pull request if the owner of repo would like to use your changes then he will merge
> in case of collaboration all collaborator can work like their own repo

### Removing a remote
> sometime you want to remove a added remote due to some reason<br>
> first check list of added remote
```
git remote -v
```
> to remote a remote 
```
git remote rm origin
```
>note if you added your remote with different name then replace origin with that name
### fatal: refusing to merge unrelated histories
> this error occurs due to the merge of unrelated project 
> to know more go to https://www.educative.io/edpresso/the-fatal-refusing-to-merge-unrelated-histories-git-error
![picture](https://www.educative.io/api/edpresso/shot/4755609222119424/image/5534126872461312)
```
git pull origin master --allow-unrelated-histories
```
### push empty commit
```
git commit --allow-empty -m "Empty-Commit"
```
### pick a commit from one branch and add to another branch  ( just reverse of revert)
```
git cherry-pick <commit id>
```

### ssl error
```
git config --global http.sslBackend schannel
```



#### END
