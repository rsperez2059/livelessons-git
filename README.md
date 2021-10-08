'git init': initialize a current folder as the git repostiory
'git clone <URL>': brings the git repo from <URL> to current folder
'git status': tells is wjat we meed to know about our repository

'git add <FILE>': adds <FILE> to the staging area
'git commit': open a text eidtor to write commit message
    - 'git commit -m "MESSAGE"': wrotes a MESSAGE as a commiet without a text editor
'git log': shows the log (history) of our commits
    - 'git log --oneline': shows the shorter oneline commit
'git diff': compare current unticmmeted state with teh last known git state
    'git diff --staged': runs git diff between the starging area and the last known state
'git diff HEAD~<NUMBER>': compares the HEAD with the commit <NUMBER> ago (relative)
'git diff <HASH>': compares the HEAD with the commit <HASH>
