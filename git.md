##1. 初始化 git
```
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
ssh-keygen -t rsa -C "youremail@example.com"
```
##2. 基本命令
```
git add <file>
git rm <file>
git commit -m "description"
git status
git diff
git clone
```
##3. 版本命令
```
git reset --heard commit_id
git reset HEAD file
git checkout -- readme.txt
git log
git reflog
```
在Git中，用HEAD表示当前版本，上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100。

```
git reset --hard HEAD^
```

##4. 远程库命令
```
git remote add origin git@server-name:path/repo-name.git
git push -u origin master
git push origin master
git remote
git remote -v
```
第一次推送master分支的所有内容
##5. 分支命令
```
git branch
git branch dev
git branch -d dev
git branch -D dev
git checkout dev
git checkout -b dev
git checkout -b dev origin/dev
git merge <name>
git merge --no-ff -m "Description" <Branch Name>
git log --graph //分支合并图
```
###5.1 bug 分支
```
git stash
git stash apply
git stash drop
git stash pop
git stash list
```
##6. 标签命令
```
git tag
git tag v1.0
git log --pretty=oneline --abbrev-commit
git tag v0.9 6224937
git show v0.9
git tag -a v0.1 -m "version 0.1 released" 3628164
git show <tagname>
git tag -s v0.2 -m "signed version 0.2 released" fec145a
git tag -d v0.1
git push origin v1.0
git push origin --tag
git push origin :refs/tags/v0.9
