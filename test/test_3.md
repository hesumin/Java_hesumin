## 举出几个常用的 git 命令，描述什么情况下会产生代码冲突？如何解决？
1. 初始化git仓库命令
git init
2. 添加用户和邮箱 
$  git config --global user.name ""
$  git config --global user.email ""
3. git add 文件名 添加文件
4. git commit -m  0.1  提交代码库
5. git pull 更新代码
6. git push 提交代码

1. git checkout 文件名 还原本地文件
   git checkout 分支名称切换分支
2. git diff 比较工作区文件 和本地仓库文件 不加参数的话
3. git merge b   指定分支名 合并当前分支
4. git rebase b  把 b 合并到当前分支
5. git reset --hard   还原到上一个版本
6.. git  log 查看提交记录
7. git reset -- hard  23ddnndnfdd  还原到指定版本
8. git rm 文件名 删除暂存区文件
9. .git branch -a 查看远程分支
10. git push origin master  --force 强制推送文件到远程服务器 替换原来的文件
11. git reflog show dev 查看操作记录  git reset --hard  版本号     还原具体的版本


# 代码冲突往往会发生在以下情况：
1. 多个代码更改发生在同一行代码上
2. 一个提交删除了某一个文件而另一个提交尝试去编辑该文件

# 解决方法
1. 解决同行代码竞争引起的合并冲突
为了解决一个由更改同行代码引起的合并冲突，你必须决定在冲突方中哪一个提交的代码才是最终需要提交到分支上。
（1）打开Git Bash。
（2）进入发生代码冲突的本地Git仓库。
（3）获取受到合并冲突印象的文件列表。在本例中，文件styleguide.md有一个合并冲突。
（4）打开文本编辑器，并用他找到文件中冲突发生的地方。
（5）你可以查找“<<<<<<<”标记符出现的地方来定位合并冲突发生的位置。
（6）决定你是否只保留你分支上的代码，还是保留另一个开发人员提交的代码，
	或者编写一个全新的代码提交（包含两者）。
	删除冲突标记符“<<<<<<<”，“=======”，“>>>>>>>”，并对文件完成你想要的修改。
（7）增加你的修改。
（8）提交代码。

2. 解决文件删除引起的合并冲突
（1）打开Git Bash。
（2）进入发生代码冲突的本地Git仓库。
（3）获取受到合并冲突印象的文件列表。在本例中，文件styleguide.md有一个合并冲突。
（4）打开你最心爱的文本编辑器，例如Atom，并用他找到文件中冲突发生的地方。
（5）决定你是否要保留被移除的文件。你也许想在文本编辑器中查看被移除文件最后的修改。
（6）提交代码。



