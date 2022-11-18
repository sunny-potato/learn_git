# Learning git

### concept 
- origin = remote repository
- master = local repository 


### git basics  
- git status
- git config
- git init :
- git rm <file_name> : Remove file, which mean git will not manage the file
- git add <option> : add modified files to the staging area (--all / -u) -> ex) git add --all 
- git restore --staged <file> : file from the staging area to unstaging area
- git commit <option> : commit files (-m 'commit_description') -> ex) git commit -m "initial commit" 
                        (without -m, "vi" editor worked so to quit the editor, press button "ESC"adn then write commit ":wp" (write, quit))
                         => git commit -a = git add
                         => git commit -am = git add & commit at the same time
                         what is commit? record as a snapshot of project(=repository) in timelines
- git log : check if commit is updated well or not
- git diff : see the differences between before and after change of file
- git fetch : check in local repository if any changes from remote repository 
- git merge origin/<branch_name> : merge changes into local repository
- git pull <option> : pull = fetch + merge (--all)
- git clone <web_url> : clone project/repository
- git reset : go back to previously committed file without all uncommitted changes
- git revert : go back to previously committed file with all uncommitted changes (useful when teamarbeid)


### basic command
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin <web_url>
git push -u origin main


### remote-repo
- git remote : show name of remote-repo
- git remote -v : show addresss of remote-repo
- git remote show : show all
- git remote rename <old_name> <new_name> : change remoto-repo's name
- git remote remove <remote-repo_name> : remove connection to remote ->  ex) git remote remove origin
- git remote update : update information on remote
- git remote add <option> <remote_name> <url> : add remote to local ([-t <branch>] [-m <master>])
                                            

### branch
- git branch <file_name> : create new branch -> ex) git branch new_branch
- git checkout <file_name> : switch to new branch/main -> ex) git checkout new_branch or git checkout main
- git branch -d <branch_name> : delete branch -> ex) git branch -d new_branch 
- git merge <branch_name> : merge branch to main -> ex) git merge new_branch
- git add or git merge -- abort : (merge conflict) it can be modified manually or decided merge by the command
- git branch : list of local branches
- git branch -r : list of local and remote branches
- git branch -v :
- git branch -vv :



