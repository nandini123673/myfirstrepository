[## This repository contains my git practice

## Topics covered : git restore, git log, git clone, git branches pull request, git pull, git fetch, git revert, git fork, git stash, .gitignore, git diff, git conflict.

 README.md: Documentation about my git practice.
 restore.txt: Practice file
 
Git installation
Git initialization using git init command
Git status
Git add using git add command
Git commit using Git commit -m ""
Git push


COMMANDS :

## git restore: The git restore command is used to restore the contents of a file or discard unwanted changes.
Syntax :
        git restore --staged restore.txt
        filename: git restore.txt Practice file for the git restore command

Steps:
Created a GitHub Repository.
Initialized a local git repository using git init
created restore.txt file using touch restore.txt.
add content to restore.txt using vi.restore.txt.
git add command and git commit commands used to add and commit git add restore.txt and git commit -m ""
pushed the repository to git hub using git push.


## git log : it is used to display the commit history of a git repository. It shows all the commits made in the repository.
syntax : 
        git log
        file name: restore.txt : Practice file for the git log command.
Steps :
Created a GitHub Repository.
Initialized a local git repository using git init
open restore.txt file using cat restore.txt. the content is visible already in that file.
git add command and git commit commands used to add and commit git add restore.txt and git commit -m ""
pushed the repository to git hub using git push.
used git log command to display commit history.


## git clone : It is used to Copies an entire remote repository to our local repository.
syntax :
        git clone (repository Url)
        git clone url

Steps:
Open GitHub.
open the repository i want to copy.
click the code button copy the repository url
press enter
git downloads the repository in our computer.
new folder with the repository name is created to display git history.


## git pull : update our local repository with the latest changes from a remote repository.
Syntax :
        git pull

Steps :
Open GitHub select repository inside repository we have to select one file for edit.
to add content or edit something in a repository file.
then select commit changes.
go to git and give git pull command.
open file in local machine.

## git help: it is used to get the documentation of all commands.
syntax: 
       git help command names

example: git help push
git help restore
git help pull
git help clone

## git branches: Pull request:
it is used to keeping a main branch from bug or error free
it is a separate path where we can work our code without effecting the main branch
if in case any errors occurs first we push or add development branch, after integrate we can push main branch.
there are two branches main branch and development branch.

syntax :
        git checkout development
        git checkout main
Steps :
select repository the name is firstrepository
then go to branches we are in main branch
then create another branch name like development
to check using git checkout.

## git pull: copies changes from remote repository to our local repository directly.
Syntax : 
        git pull
steps:
go to GitHub repository,select one repository
copy http url and paste using git clone command in a git bash.
go inside the folder using cd folde rname
go inside the folder using cd folder name
both older files are visible in gitbash
go to repo select one file and edit or add content or remove content and give commit changes.
in the git bash we use the command git pull it is changing directly.
using cat filename the added content is visible in git bash.

## git fetch: if any changes in remote repository after commit changes first it will give notification, using the command git fetch after using git merge command the content is merge.
Syntx:
      git fetch
       git merge
Steps:
go to GitHub then select repository  inside the repository file we add some content and commit changes
in git bash i gave the command git fetch it will give notification first
second time i gave git fetch it doesn't give
after git merge command it displays the content.

## .gitignore : A .gitignore file contains a list of file names, file types, or folder names that should git ig to keep sensitive files
 Syntax :
         touch .gitignore
         vi .gitignore
Steps:       
to create four files using touch .filename 
to use vi .gitignore command to insert  remove or add which file can be avoid
to add file in vi .gitignore that file is removed, and display other files.
to remove added file using vi .gitignore the file is add and display all files.

## git fetch: first it will give notification that there are some changes in central repository
Syntax:
        git fetch
        git merge
 
  Steps:
  go to GitHub repository
  select one repository
  select one file and add contents remove contents are modify the contents and give commit changes.
  come to Git bash give command git fetch it will give notification, first time only.
  after using git merge command we can see the modified content  otherwise it can not display
 
## git fork : git fork is not a git command it is a feature of git hub.

  Steps :
  login GitHub
  go to search bar and then type others account name/repository name the repository name is visible select that repository
  click the fork button in the top right corner of the repository page.
  a copy of the repository is created.
  copy your forked repository url and run using git clone.
  the repository is loaded to our computer.


## git revert : this command is used  for to discard or undo the content in repository what we push
 Syntax :
        git  revert commit ID

  Steps:
  create one file using touch command touch f1.txt then add some content in file using vi f1.tx
  then push file to the repository. check file the content stored in repository.
  to discard content or undo changes in the content using git revert command and then copy commit id of the repository file
  in git bash we give the command " git revert commit id " and content is deleted in git after push GitHub content also deleted.


## git stash : git stash is a git command to temporarily save uncommitted changes without committing them. store secretly in a hidden or secret file.  
 Syntax: 
         git stash content is stored in hidden file added content is not visible
         git stash list
         git stash apply content visible

 ## .gitignore : A .gitignore file is a special file used by git to tell itb which files and folders should not be uploaded to the repository
  Syntax:
         touch .gitignore
         vi .gitignore

   Steps :
   create some files using touch filenames
   create touch .gitignore file
   select one file to ignore and add using vi .gitignore 
   aded file is ignore it is not visible
   remove using vi .gitignore then it is visible 


 ## git diff : git diff command is used for to check difference between working area and central repository.
  Syntax:
         git diff
  
  Steps:
  create one file and add content in to the file using touch f1.txt and vi f1.txt
  give git diff command it will show given content in green colour with plus sign
  after pushing this content file in to the repository it shows green colour text with plus symbol 
  using vi .f1.txt to remove added content, then use the same command git diff it shows minus symbol and red colour 
  after push this file in to the repository it shows minus symbol and red colour line.

## git conflicts: it is used for to resolve conflicts after merging into different branches using same file or same content.
 Syntax :
         git checkout dev1
         git checkout dev2

 Steps :
 create two branches in repository pull branches into gitbash
 using git checkout dev1 branch and add content using vi f1.txt
 push file using git push to merge this branch using compare pull request there is no conflict occurs 
 it is merge aautomatically
 we followed same staps for dev 2 branch using same file and add content push  after compare pull request it showing conflicts 
 after resolving conflicts it is merged.
























](https://github.com/nandini123673/firstrepository.git)
