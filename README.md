#龚
1.在window环境下当打开cmd,一般是在默认的document目录下，如果进入d盘，快捷键为d:

2.进入某个目录，为cd + 目录名称

3.创建新目录为mkdir+你想起的目录名称
###git bash命令
1.cd 进入某某目录，example: cd d: 进入d盘。`pwd`查看当前目录

2.在某个目录下使用命`git init`,这个目录就成为了一个仓库，目录中的所有文件就可以被git管理了。

3.使用`git add`加文件名添加文件。

4.第四部，使用`git commit -m "操作说明"`保存

5.`git status`查看状态，`git diff`查看不同

6. 修改的时候要提交使用的也是git add git commit liang'bu这两步

 . 使用`git log`查看历史记录 使用`git log --pretty="commit id"`查看特定版本号
 
 . 使用`git reset --hard HEAD^`退回到特定版本，退回上100个版本为HEAD~100。`git set --hard +commit号`可以到特定版本
 
 . `git reflog`在关闭电脑之后仍然可以找到历史的各个版本号用于退回
 
 . **暂存区的概念**，git add 是把内容先放到暂存区。git commit就是放到分支上。
 
 . 如果只是修改了内容，没有git add 和git commit 可以通过 `git checkout -- +文件名丢弃`。如果已经add了，可以通过git reset HEAD file和checkout撤销
 如果add、和commit之后就可以版本回退。
 . **删除内容**。删了文件之后，实际是把工作区的文件删除了，如果要把版本库的文件也删除，则使用git rm + 文件名。然后再git commit。如果是误删的则可以，checkout 回复。
 ###远程仓库
 1. 将本地git仓库添加到远程github仓库，并用这两个仓库进行远程同步。先在github上建立一个同名的repository，然后使用命令`$ git remote add origin git@github.com:+github的用户名/+repository名称.git`，然后使用`$ git push -u origin master`,以后再更新用`$ git push origin master`即可

2.将远程库克隆到本地使用`git clone`
    
