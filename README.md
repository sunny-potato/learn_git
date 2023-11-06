# Learning git

## <<<<<<< HEAD

- git status
- git config
- git init
- git rm (-rf .file_name (ex).git) Remove the file, which mean git will not manage the file)
- git add (--all Adds all modifications to the Staging Area) (-u Adds all changes to existing files to the Staging Area)
- git restore (--staged <file>... to unstage)
- git commit (-m 'commit_description') (without -m, "vi" editor worked so to quit the editor, press button "ESC"adn then write commit ":wp" (write, quit))
  => git commit -a = git add
  => git commit -am = git add & commit at the same time
- git log : check if commit is updated well or not
- git diff : see the differences between before and after change of the file
- git remote (--help to pop up nanual page in browser ), (add [-t <branch>] [-m <master>] [-f] [--[no-]tags] [--mirror=(fetch|push)] <name> <url>)
- git pull (git pull = git fetch + git merge)
- git push (--all)
- git merge ("branch_name" to merge branch to main-> when conflict, modify or decide what i will take(git add or git merge -- abort),
- git checkout ("branch_name" to change to the branch), (-b "branch_name" to create new branch)

- git reset : go back to previously committed file without all uncommitted changes
- git revert : go back to previously committed file with all uncommitted changes (useful when teamarbeid)
- git branch ("branch_name")

git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/sunny-potato/typingGame.git
git push -u origin main

### remote-repo

- git remote : show name of remote-repo
- git remote -v : show addresss of remote-repo
- git remote show : show all
- git remote rename <old_name> <new_name> : change remoto-repo's name
- git remote remove <remote-repo_name>
- git remote fetch <remote_name> : bring all the data from remote-repo ex) git remote fetch origin

### new branch

- git branch : show the list of branches
- git branch <branch_name> : create new branch -> ex) git branch new_branch
- git checkout <branch_name> : switch to new branch/main -> ex) git checkout new_branch or git checkout main
- git merge <branch_name> : merge branch to main from main -> ex) git merge new_branch (in main)
- git push -u origin new_branch : create a new branch named "new_branch" in remote and push code to the new branch
  (when commando "git push"after it above, automatically push to the new branch)
- (Merge conflict) git add or git merge -- abort : it can be modified manually or decided merge by the command
- git rebase <main/master_name> : to bring the latest code from main/master -> ex) git rebase main (in branch)

### stash

: when I want to save current modified files and then go back to the files before their change.
the modified files are saved in stack

- git stash : save current modified files. after that working directory will be clean (possible to do several stash)
- git stash list : check stash list
- git stash apply : bring the latest stash or
- git stash apply <stash_name>
- git stash drop : remove stash saved in stacks
  git stash pop : git stash apply + apply
