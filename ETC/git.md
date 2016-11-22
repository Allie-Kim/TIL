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
#### diff

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

 
#### reset
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

#### tagging
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







