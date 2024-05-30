连接github第一次上传必须输密码
使用加速器时 要输入` git config --global http.sslVerify false`//关闭SSL认证,才能上传成功

克隆仓库：
`git clone <git地址>`
初始化仓库：`git init` 

添加文件到暂存区：`git add -A`
把暂存区的文件提交到仓库：`git commit -m "提交信息"`
查看提交的历史记录：`git log --stat`

工作区回滚：`git checkout <filename>`
撤销最后一次提交：`git reset HEAD^1`

以当前分支为基础新建分支：`git checkout -b <branchname>`
列举所有的分支：`git branch`
单纯地切换到某个分支：`git checkout <branchname>`
删掉特定的分支：`git branch -D <branchname>`
合并分支：`git merge <branchname>`

推送当前分支最新的提交到远程：`git push`
拉取远程分支最新的提交到本地：`git pull`

简易的命令行入门教程:
Git 全局设置:

git config --global user.name "李佳明"
git config --global user.email "2939760167@qq.com"
创建 git 仓库:

mkdir learning-c
cd learning-c
git init 
touch README.md
git add README.md
git commit -m "first commit"
git remote add origin https://gitee.com/ming-xiaolizi/learning-c.git
git push -u origin "master"
已有仓库?

cd existing_git_repo
git remote add origin https://gitee.com/ming-xiaolizi/learning-c.git
git push -u origin "master"

`git init`初始化该文件夹为git

` git remote add origin https://gitee.com/ming-xiaolizi/git-study.git`与对应网址的远程仓库建立连接

`git pull origin master`拉取远程仓库内容到本地仓库

`git commit -am "first one"`本地仓库并添加版本说明

`git push origin master`上传到远程仓库的 master分支

**分支**
默认 master
`git branch -M main` 命令用于将本地分支 main 重命名为 main
`git checkout -b feature_1` 创建一个feature_1分支；并切换到该分支

`git checkout master` 切换主分支

`git push origin frature_1` 添加feature_1分支到远程仓库

_合并分支_
`git pull` 更新本地仓库至最新改动

`git merge <branch>`合并其他分支到当前分支

`git add <filename>`合并可能需要手动修改文件冲突，修改完成执行此命令表示合并成功

`git diff<source_branch><target_branch>`合并之前使用该命令预览分支差异

**标签**
获取标签：`git log`

`git tag 1.0.0 <ID前十位或具有唯一性的前几位>` 为一个ID(commit)添加1.0.0标签
**更改与替换**

`git checkout --<filename>`将本地仓库中的最新内容替换掉工作目录中的文件 加到暂存区的文件以及新文件不会受到影响

如果要丢弃本地的所有改动与提交，可以到远程仓库上获取最新的版本历史，并将你的<u>本地z主分支指向它</u>：

`git fetch origin` \\获取远程仓库版本

`git reset --hard origin/master`

**状态**
`git reset`	命令撤回提交到缓存区的操作

`git status`命令查看当前的提交状态,确定需要撤回的操作所在的分支

**忽略文件**
在.git目录下创建`.gitignore`

忽略所有 .log 文件
*.log
 
忽略特定文件 mysecretfile.txt
mysecretfile.txt
 
忽略整个目录
node_modules/
 
忽略所有 .pdf 文件，但跟踪特定的 mydoc.pdf
*.pdf
!mydoc.pdf
 
忽略所有文件，但跟踪 .gitignore 和 foo.bar 文件
*
!.gitignore
!foo.bar

** 查看关联的远程库**

`git remote`查看远程仓库的简要信息(列出所有远程仓库的名称及地址)

`git remote -v` 列出所有远程仓库及其URL。
```
以下结果表示只有一个origin的远程仓库 并且具有 fect 和 push 操作的url（仓库地址）
origin  https://github.com/username/repo.git (fetch)
origin  https://github.com/username/repo.git (push)
```