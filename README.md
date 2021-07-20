![8ogqpfkvqqpyfbs3w6p7](https://user-images.githubusercontent.com/57607250/126332351-3557714b-b911-4cfe-a22e-c4baaa12203d.png)
# `GIT SETUP`
```
git config --global user.name "name"
git config --global user.email “[valid-email]”
git config --global color.ui auto
```
# `SETUP & INIT`
Initialize an existing directory as a Git repository :-
```
git init
```
Retrieve an entire repository from a hosted location via URL :-
```
git clone [url]
```
Add file to an entire repository from a hosted location :-
```
touch [filename]
```
# `STAGE & SNAPSHOT`
Show modified files in working directory, staged for your next commit :-
```
git status
```
Add a file as it looks now to your next commit (stage) :-
```
git add [file]
```
Unstage a file while retaining the changes in working directory :-
```
git reset [file]
```
Diff of what is changed but not staged :-
```
git diff
```
Diff of what is staged but not yet commited :-
```
git diff --staged
```
Commit your staged content as a new commit snapshot :-
```
git commit -m “[message]”
```
# `BRANCH & MERGE`
List your branches will appear next to the currently active branch :-
```
git branch
```
Create a new branch at the current commit :-
```
git branch [branch-name]
```
Switch to another branch and check it out into your working directory :-
```
git checkout
```
Merge the specified branch’s history into the current one:-
```
git merge [branch]
```
Show all commits in the current branch’s history :-
```
git log
```
# `INSPECT & COMPARE`
Show the commit history for the currently active branch :-
```
git log
```
Show the commits on branchA that are not on branchB :-
```
git log branchB..branchA
```
Show the commits that changed file, even across renames :-
```
git log --follow [file]
```
Show the diff of what is in branchA that is not in branchB :-
```
git diff branchB...branchA
```
Show any object in Git in human-readable format :-
```
git show [ ]
```
# `TRACKING PATH CHANGES`
Delete the file from project and stage the removal for commit :-
```
git rm [file]
```
Change an existing file path and stage the move :-
```
git mv [existing-path] [new-path]
```
Show all commit logs with indication of any paths that moved :-
```
git log --stat -M
```

# `IGNORING PATTERNS`

```
logs/
**.notes
pattern*/
```
Save a file with desired paterns as .gitignore with either direct string
matches or wildcard globs.

System wide ignore patern for all local repositories :-
```
git config --global core.excludesfile [file]
```
# `SHARE & UPDATE`
Add a git URL as an alias :-
```
git remote add [alias] [url]
```

Fetch down all the branches from that Git remote :-
```
git fetch [alias]
```

Merge a remote branch into your current branch to bring it up to date :-
```
git merge [alias]/[branch]
```

Transmit local branch commits to the remote repository branch :-
```
git push [alias] [branch]
```

Fetch and merge any commits from the tracking remote branch :-
```
git pull
```

# `REWRITE HISTORY`

Apply any commits of current branch ahead of specified one :-
```
git rebase [branch]
```
Clear staging area, rewrite working tree from specified commit :-
```
git reset --hard [commit]
```
# `TEMPORARY COMMITS`



list stack-order of stashed file changes :-
```
git stash list
```
write working from top of stash stack :-
```
git stash pop
````

Discard the changes from top of stash stack:-
```
git stash drop
```
