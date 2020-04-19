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

