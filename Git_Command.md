# Git Commands

## Add Repository From Local

**Create from local**

```sh
$ curl -u USER https://api.github.com/user/repos -d '{ "name": "REPO" }'

$ git clone https://github.com/Ethanwireless/REPO.git
```

**Created from Github**

```sh
$ git init

# $ git add .
$ git touch readme.md
# Adds the files in the local repository and stages them for commit. To unstage a file, use 'git reset HEAD YOUR-FILE'.

$ git commit -m "First commit"
# Commits the tracked changes and prepares them to be pushed to a remote repository. To remove this commit and modify the file, use 'git reset --soft HEAD~1' and commit and add the file again.

$ git remote add origin REMOTE REPOSITYORY URL
# Sets the new remote

$ git remote -v
# Verifies the new remote URL

$ git push -u origin master
# Pushes the changes in your local repository up to the remote repository you specified as the origin
```

## Rollback Version
**Not committed**

```sh
$ git reset --hard HEAD^
```

**Committed**

```sh
$ git reset --hard HEAD^
```

**Log**

```sh
$ git log
$ git reflog
```

## Undo File Modifications
**Modified file only**

```sh
$ git checkout -- file
```

**modified file and added**

```sh
$ git reset HEAD file
$ git checkout -- file
```

## Branch

**Create branch**

```sh
$ git checkout -b dev
Switched to a new branch 'dev'
```
same as

```sh
$ git branch dev
$ git checkout dev
Switched to branch 'dev'
```
**Do modification in dev and switch back in master**

```sh
$ git merge dev
$ git branch -d dev
```

**Branch graph**

```sh
$ git log --graph
```

**Store work and get back**

```sh
$ git stash
$ git stash pop
```

**Update local and push branch**

```sh
$ git pull
$ git push origin branch-name
```

## Tag

```sh
# create new branch (default HEAD)
$ git tag <name>

$ git tag -a <tagname> -m "msg"

$ git tag -s <tagname> -m "msg"

# show the tags
$ git tag

# push local tag
$ git push origin <tagname>

# push all local tags
$ git push origin --tags

# delete local tag
$ git tag -d <tagname>

# delete remote tag
$ git push origin :refs/tags/<tagname>
```


