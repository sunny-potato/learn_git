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
- git mreote show : show all
- git remote rename <old_name> <new_name> : change remoto-repo's name
- git remote remove <remote-repo_name>

### new branch

- git branch <file_name> : create new branch -> ex) git branch new_branch
- git checkout <file_name> : switch to new branch/main -> ex) git checkout new_branch or git checkout main
- git merge <branch_name> : merge branch to main -> ex) git merge new_branch
- (Merge conflict) git add or git merge -- abort : it can be modified manually or decided merge by the command
