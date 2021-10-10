# Git Notes

## Working with git locally

- 'git init': initialize a current folder as the git repostiory
- 'git clone <URL>': brings the git repo from <URL> to current folder
- 'git status': tells is wjat we meed to know about our repository

- 'git add <FILE>': adds <FILE> to the staging area
- 'git commit': open a text eidtor to write commit message
    - 'git commit -m "MESSAGE"': wrotes a MESSAGE as a commiet without a text editor

- 'git log': shows the log (history) of our commits
    - 'git log --oneline': shows the shorter oneline commit

- 'git diff': compare current unticmmeted state with teh last known git state
    - 'git diff --staged': runs git diff between the starging area and the last known state
- 'git diff HEAD~<NUMBER>': compares the HEAD with the commit <NUMBER> ago (relative)
- 'git diff <HASH>': compares the HEAD with the commit <HASH>

- 'git restore --source <HASH OR HEAD~> <FILE>': restore file to <HASH OR HEAD~>
    - 'git checkout <HASH OR HEAD~> <FILE>' restore file to <HASH OR HEAD>
        - 'git checkout <HASH OR HEAD~>': if you forget the file, you end  up in the detached head state
        - 'git checkout main': go back to the main
        - 'get switch main': go back to main

## Working with remotes 
    
- 'git remote add <NAME> <URL>': adds the <URL> as a remote wth the same name <NAME>
    - <NAME> is by convention called 'origin'
- 'git remote rm <NAME>': Removes the remote called <NAME>
- 'git remote -v': look at all the remotes you have
- 'git push <WHERE> <WHAT>': pushes the <WHAT> branch to the <WHERE>
    - 'git push origin main
- 'git pull <WHERE> <WHAT>': pulls the <WHAT> branch in <WHERE> to orig local computer

## Branches

- 'git branch <NAME>': create branch <NAME> where you are (HEAD)
- 'git switch <NAME>': move to the branch <NAME>
    - 'git checkoug <NAME>': alod moves to the branch <NAME>
- 'git swich -c <NAME>': create and move to the branch <NAME> in 1 command
    - "git checkout -b <NAME>': also create and move to the branch <NAME> in 1 command

- 'git merge <BRANCH>': merge <BRANCH> into your current branch
- 'git rebase': command to change the history of a commit
    - Commits from 'git merge' can be autmatically combined
- 'git rebase <BRANCH>': incoprpate changes from <BRANCH> into current branch
    - 'git status': is your friend
    - 'git add <FILE>': to mark conflict resolutions
    - 'git rebase --continue': move to next commit in rebase
    - 'git rebase --abort': undo git rebase steps
- 'git rebase -i <COMMIT>' 'HEAD~' or <HASH> of commit to go into interactive rebase
    - you can make multiple commit changes here, e.g., 'squash'/'s'
    - 'git rebase - <HASH>^': use ^ to include that commit in intractive rebase
- 'git stash' or 'git commit': to save work before moving branches
    - 'stash' is temporary
    - 'git stash list': see your stashed commits
    - 'git stash apply': apply your last stashed commit
    - 'git stash clear': clear up your stashes

- A 'merge' on the remote is called a "pull request" or a "merge request"
    - 'git push <WHERE> <WHAT>'
    - To update a PR, we make the changes to the branch locally and re-'push'
