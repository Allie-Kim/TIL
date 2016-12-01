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
when unsync each other branch of local (local에서 각 브랜치가 각각 커밋된 상태)
```
git checkout kennel
git rebase master
git checkout master
git merge kennel
```
* ``` git rebase master ``` : master와 kennel에 공통 commit으로 돌아가고 그 이후는 temp area에 저장하고 master의 final commit을 kennel과 맞춤 -> master와 kennel은 sync가 맞게 되고 kennel의 새로운 commit만 새로운가지친 형태(master는 새로운 commit없고)

------
```
git rebase -i HEAD~3
```
when we need to alter last 3 commits in the same branch.  
can change order or comment at the editor.  
* HEAD^: last commit
 

### Stashing
Modified tracked files and files in staging area are saved on stack. (본통 작업하다말고 다른 브랜치로 옮길 때)

```
git stash save (= git stach)
```
```
git stash apply (= git stash apply stash@{0})
```
when confilting after apply command   
git reset --hard HEAD
-> git stash apply  

```
git stash list
```
```
git stash drop
```
```
git stash pop ( = git stash apply + git stash drop)
```


#### references
* [Code School: Git Real](https://www.codeschool.com/courses/git-real)







