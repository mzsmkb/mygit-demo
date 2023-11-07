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


# 这是newbug分支里的东西
