#github基本操作命令
##从零开始创建项目远程仓库
- 在github页面上新建项目仓库
- 将github上的项目仓库克隆到本地`git clone https://github.com/Accumulations/github-operation-demo
`
- 将项目里所有文件添加到本地仓库`git add .`，并将文件上传到本地仓库且进行描述`git commit -m "github test"`
- 执行推送命令，将本地仓库推送到远程仓库`git push origin master`


##从远处仓库拉取项目
- 拉取项目`git pull https://github.com/Accumulations/github-operation-demo`
- `git add .`
- `git commmit -m "xxx"`
- `git push origin master`

##分支
- 建立分支，并切换到dev分支 `git checkout -b dev`
- 用`git branch`命令查看当前分支
- 再进行数据修改
- `git add .`....