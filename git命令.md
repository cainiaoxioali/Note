`git init`初始化该文件夹为git

` git remote add origin https://gitee.com/ming-xiaolizi/git-study.git`与对应网址的远程仓库建立连接

`git pull origin master`拉取远程仓库内容到本地仓库

`git commit -am "first one"`本地仓库并添加版本说明

`git push origin master`上传到远程仓库的 master分支

**分支**
默认 master

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
