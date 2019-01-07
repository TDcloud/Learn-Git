# git pull命令的用法

git pull命令的作用是：取回远程主机某个分支的更新，再与本地的指定分支合并。

一句话总结git pull和git fetch的区别：git pull = git fetch + git merge

git fetch不会进行合并执行后需要手动执行git merge合并分支，而git pull拉取远程分之后直接与本地分支进行合并。更准确地说，git pull使用给定的参数运行git fetch，并调用git merge将检索到的分支头合并到当前分支中。

## 基本用法：

```git pull <远程主机名> <远程分支名>:<本地分支名>```
例如执行下面语句：

```git pull origin master:brantest```
将远程主机origin的master分支拉取过来，与本地的brantest分支合并。

后面的冒号可以省略：

```git pull origin master```
表示将远程origin主机的master分支拉取过来和本地的当前分支进行合并。

上面的pull操作用fetch表示为：

```git fetch origin master:brantest```
```git merge brantest```

相比起来 git fetch 更安全一些，因为在merge前，我们可以查看更新情况，然后再决定是否合并。

