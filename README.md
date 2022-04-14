## Learning Git

### git commit
添加一条提交记录
```shell
git command -m "message"
```

### git branch
切换并且创建一个分支
```shell
git checkout -b dev
```

### git merge
进行合并，将dev分支合并到master上面
```shell
git checkout master
git merge dev
```

### git rebase
另外一种合并的方式，将提交记录整体复制
```shell
git merage dev
```
此操作会将dev分支进行复制，并且dev分支将会移动