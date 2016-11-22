# git

### .gitignore 
sample file
```
#.gitignore
.idea
server/node_modules
npm-debug.log
```



# git commands  
### diff  

```
git diff
```
show unstaged differences since the last commit.  
If all changes are staged(after 'add'), show nothing.  

-------  
```
git diff --staged
```
show staged differences  

 
### reset
```
git reset HEAD <file>
```
stage to unstage
* HEAD: refers to last commit on the current branch

--- 
```
git reset --soft HEAD^
```
will undo the last commit, reset to stage  
* ^: move to commit befere HEAD (바로 전 commit으로 step back)

---
```
git reset --hard HEAD^
```
undo last commit and all changes

### tagging
A tag is a reference to a commit (used mostly for release versioning)
```
git tag
```
tag list (usually version.. ex) v0.0.1)  

---
```
git checkout [tagname]
```
check out code at commit 

---
```
git tag -a v0.0.3 -m "version 0.0.3"
```
add a new tag  

---
```
git push --tags
```
push new tags

### rebasing
MERGE COMMITS ARE BAD.
Alternatively, rebase is better.

**case of conflict when push**   
1. git fetch: sync with remote (not merge) - 같은 파일 충돌날때마다 git fetch & rebase 반복  
2. git rebase: move all changes to master which are not in origin/master to a temp area (sync이후의 수정사항을 임시공간에 이동)  
  ```
  git fetch
  git rebase
  ```
3. solve the conflicted file (ex.remove conflict msg like <<< HEAD..)  
4. ``` git add [file] ```  
5. ``` git rebase --continue ```  
6. ``` git push ```   

**in case of not conflict**
```
git checkout kennel
git rebase master
git checkout master
git merge kennel
```

#### references
* [Code School: Git Real](https://www.codeschool.com/courses/git-real)







