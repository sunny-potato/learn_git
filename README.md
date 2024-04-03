# Learning git

## Basics

### Log

- git log : check if commit is updated well or not
- git log --pretty=oneline (to exit it, type "q")
- git status
- git config
- git init
- git rm (-rf .file_name (ex).git) Remove the file, which mean git will not manage the file)
- git add (--all Adds all modifications to the Staging Area) (-u Adds all changes to existing files to the Staging Area)
- git restore (--staged <file>... to unstage)
- git commit (-m 'commit_description') (without -m, "vi" editor worked so to quit the editor, press button "ESC"adn then write commit ":wp" (write, quit))
  => git commit -a = git add
  => git commit -am = git add & commit at the same time

- git diff : see the differences between before and after change of the file
- git remote (--help to pop up nanual page in browser ), (add [-t <branch>] [-m <master>] [-f] [--[no-]tags] [--mirror=(fetch|push)] <name> <url>)
- git pull (git pull = git fetch + git merge)
- git push (--all)
- git merge ("branch_name" to merge branch to main-> when conflict, modify or decide what i will take(git add or git merge -- abort),
- git checkout ("branch_name" to change to the branch), (-b "branch_name" to create new branch)

- git reset : go back to previously committed file without all uncommitted changes
- git revert : go back to previously committed file with all uncommitted changes (useful when teamarbeid)

### Remote-repo

- git remote : show name of remote-repo
- git remote -v : show addresss of remote-repo
- git remote show : show all
- git remote rename <old_name> <new_name> : change remoto-repo's name
- git remote remove <remote-repo_name>
- git remote fetch <remote_name> : bring all the data from remote-repo ex) git remote fetch origin
- git remote update

### Rebase

### Branch

- git branch : Show the list of local branches
- git branch -r : Show the list of remote branches
- git branch -a : Show the list of local + remote branches
- git branch -d <branch-name> : Delete the branch
- git branch <branch-name> : Create a new branch
- git checkout <branch-name> : Switch to the branch
- git merge <branch-name> : merge branch to main from main _For exemple git merge <new-branch> (in main)_
- git push -u origin <new-branch> : create a new branch named "new_branch" in remote and push code to the new branch
  (when commando "git push"after it above, automatically push to the new branch)
- (Merge conflict) git add or git merge -- abort : it can be modified manually or decided merge by the command
- git rebase <main/master-name> : to bring the latest code from main/master _For exemple git rebase main (in branch)_

:**Fetch code from a remote branch to a local branch**

- git checkout -t <remote-branch-name>: Create a new local branch with the same name as the remote branch and check out to the new local branch
- git checkout -b <new-local-branch-name> <remote-branch-name> : Create a new local branch with a new name for thelocal branch

### Stash

: **When I want to save the current modified files and then revert back to the files before their change, stash can be used**

- git stash: Save the current modified files. After that, the working directory will be clean. I can do this multiple times to create multiple stashes.
- git stash list: Check the stash list to see the saved stashes.
- git stash apply : bring the latest stash or
- git stash apply : Bring the latest stash, or alternatively, I can specify the stash name with "git stash apply <stash_name>".
- git stash drop: Remove the latest stash from the stash stack.
- git stash pop: It applies the latest stash and then removes it from the stash stack.(git stash apply + git stash drop.)

: **When merging updated code from the remote repository while I am working on a branch, follow these steps**

1. git stash: Save the current files on the branch.
2. git stash list: Check if the files are saved in the stash.
3. git checkout main: Move back to the main branch.
4. git pull (git fetch + git merge): Fetch and merge the updated code from the remote repository into the main branch.
5. git checkout <branch_name>: Move back to the working branch.
6. git merge main: Merge the changes fetched from the main branch into the working branch.
7. git stash apply: Apply the changes saved in the stash to the working directory.

### Sqaush

: Combine commits that were worked on in the local repository before merging into the remote repository.

1. git log --pretty=oneline : Check the history of commits on the working branch.
2. git rebase -i HEAD~<Number_of_commit> : Specify the number of commits I want to squash.
3. Choose to "pick" or "squash" commits. This action combines the commits as desired.
4. Enter a new commit message at the top of the file that appears and close the file.
5. Check the squashed commit by using "git log --pretty=oneline"

### Cherry-pick

this is test
