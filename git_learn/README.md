# git_learn

## git创建分支
```
git branch <branch_name> 或 git checkout -b <branch_name>
```

## git查看当前分支的信息
```
git status
```

## git上传本地文件至分支上 

### 1.若多个文件，执行多次(1,2两步均在branch下执行)
```
git checkout <branch_name>
git add <filename> 
```

### 2.提交修改记录
```
git commit -m “修改说明” 或 git commit <filename>
```

### 3.分支合并至master
```
git checkout master
git merge <branch_name>
```

### 4.分支提交至远端

**master:**
```
git push origin <branch_name> 
```

**newbranch:**
```
git push origin <branch_name> 
```



