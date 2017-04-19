1

起步
安装git

安装git for winodw : https://git-for-windows.github.io/
用户信息：
全局安装
git config --global user.name "tom"
git config --global user.email "tom@163.com"
- 针对特定项目使用新name 和 email 时 去掉 --global 参数
git 基础
获取git仓库

在现有目录中初始化仓库

初始化
git init
track 文件
git add *.md
commit 文件
git commit -m "information"
克隆现有的仓库

克隆
git clone http://github.com/learngit
- 克隆并重命名
```
git clone http://github.com/learngit newName
```
记录更新到仓库

检查文件状态

git status
文件状态信息、
on branch master // 当前所在分支
untracked file // 文件没有 add
changes to be committed: new file: // 文件已add, 没有commit
changes not staged for commit: modified: 文件已add, 但是内容修改未add
忽略文件

所有空行或者以 ＃ 开头的行都会被 Git 忽略。
以 / 结尾指定目录
*.md 忽略所有md文件
查看修改

git diff
提交更新

提交前应该git status 确保所有修改已经add
-m 参数表示提交信息
git commit -m "commit information"
跳过git add 直接commit
git commit -a
移除文件

移动文件

查看提交历史

撤销操作

远程仓库的使用

查看远程仓库

origin 是远程仓库的默认名称
git remote
添加远程仓库

shortname 不可省略
git remote add  <shortname> http:github.com/Learn_Git/git
从远程仓库中抓取

访问远程仓库，从中拉取新数据
git fetch 命令会将数据拉取到你的本地仓库，它并不会自动合并或修改你当前的工作。当准备好时你必须手动将其合并入你的工 作。
git pull :
git pull 命令来自动的抓取然后合并远程分支到当前分支;
默认情况下，git clone 命令会自动设置本地 master 分支跟踪克隆的远程仓库的 master 分支（或不管是什么名字的默认分支）
运行 git pull 通常会从最初克隆的服务器上抓取数据并自动尝试合并到当前所在的分支
git fetch [remote-name]
推送到远程仓库

git push [remote-name] [branch-name]
