# 文件状态

两种状态：

* 未跟踪
  * 指文件没有被git管理
  * vscode中 显示绿色的 U标就是未跟踪
* 已跟踪
  * 已经被git管理
  * 三种状态
    * 暂存：文件修改已经保存，但是尚未提交到git仓库
    * 未修改：磁盘中的文件和git仓库中的文件相同，没有修改
    * 已修改：磁盘中的文件已被修改，和git仓库中的文件不同

命令：

* git add `<filename> `将文件切换到暂存状态
* git add * 将所有已修改（未跟踪）的文件暂存

  * 未跟踪--->暂存
* git commit -m "xxx" 将暂存的文件存储到仓库中
* git commit -a -m “xxx”  提交所有已修改的文件（未跟踪的文件不会提交）

  * 暂存--->未修改
* 修改代码后，文件会从未修改变成已修改状态

  * 未修改--->修改

其他：

* 重置文件
  * git restore `<filename>	恢复文件`
  * git restore --staged `<filename>	取消暂存状态`
* 删除文件
  * git rm `<filename> 删除文件`
  * git rm `<filename> -f 强制删除文件`
* 移动文件
  * git mv from to 移动文件  重命名文件

# 分支

git在存储文件时，每一次代码的提交都会创建一个与之对应的节点，git就是通过一个一个的节点来记录代码的状态码的。节点会构成一个树状结构，树状结构就意味着这个数存在分支，默认情况下仓库只有一个分支，为master。在使用git时，可以创建多个分支，分支与分支之间相互独立，在一个分支上修改代码不会影响其他的分支。

# aha现在这个分支不走newbranch那条线了
# 这是newbranch里的
* git branch  查看其他的分支情况
* git branch xxx 创建新的分支
* git branch -d xxx  删除xxx分支
* git switch xxx	切换到xxx分支
* git switch -c xxx  创建并切换到xxx分支
* git merge xxx 把xxx与当前选中的分支合并

在开发中，都是在自己的分支上编写代码，代码编写完成后，再将自己的分支合并到主分支当中.

# 变基rebase

还可以通过变基来完成分支的合并
