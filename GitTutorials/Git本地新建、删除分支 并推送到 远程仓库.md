# [Git本地新建、删除分支 并推送到 远程仓库](https://blog.51cto.com/u_3664660/3834161)

## 一、常用增删命令(本地&远程)

- 1、在本地新建一个分支

```git
git branch newBranch
```

- 2、切换到你本地新建的分支

```git
git checkout newBranch
```

- 3、创建并切换到新建本地分支

```git
git checkout -b newBranch
```

- 4、将新创建本地分支推送到远程仓库
  
```git
git push origin newBranch
```

或者

```git
git push 远程仓库名 newBranch
```

- 5、删除一个本地分支
  
```git
git branch -d newBranch
```

- 6、删除远程一个分支
  
```git
git push origin :newBranch (分支名前的冒号代表删除)
```

或者

```git
git push origin --delete <remote-branch-name>
```

## 二、常用设置命令（本地&远程)

直接使用`git pull`和`git push`的设置
两种方式：意思是默认将本地的dev分支的推送到origin/dev

```git
git branch --set-upstream-to=origin/dev dev 
```

```git
git branch --set-upstream dev origin/dev
```

```git
git config --global push.default matching
```
