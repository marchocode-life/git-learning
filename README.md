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


### 修改HEAD指向

查看当前的HEAD所在位置
```shell
cat .get/HEAD
```

#### 通过日志修改
```shell
git log
git checkout commit_hash
```

#### 相对引用^
在使用这个的时候，当前内容必须没有修改

```shell
git checkout HEAD^^
```
向上移动两个提交
`^` 操作符后也可以跟一个数字，可以在使用 `^` 进行移动的时候，选择不同的父节点

```shell
git checkout HEAD^^2
```
> 第一个^ 到达父节点,^2表示往第二条提交路线（假设有两个分支记录，第二条比较旧）
> 这样就会移动到第二条分支的下一个节点上

#### 相对引用~

```shell
git checkout HEAD~2
```
同样的效果，向上移动两个提交