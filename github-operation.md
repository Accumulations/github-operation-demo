#github基本操作命令
##从零开始创建项目远程仓库
- 在github页面上新建项目仓库
- `git clone https://github.com/Accumulations/github-operation-demo`将github上的项目仓库克隆到本地
- `git add .`将项目里所有文件添加到本地仓库
- `git commit -m "github test"`
将文件上传到本地仓库且进行描述
- `git push origin master`执行推送命令，将本地仓库推送到远程仓库

##从远处仓库拉取项目
- `git pull https://github.com/Accumulations/github-operation-demo`拉取项目
- `git add .`
- `git commmit -m "xxx"`
- `git push origin master`

##分支
- `git checkout -b dev`建立分支，并切换到dev分支 
- `git branch`命令查看当前分支
- 再进行数据修改
- `git add .`,`git commit -m "xxx"`
- `git checkout master` dev分支的工作完成，我们就可以切换回master分支 (需要本地仓库已经没有内容被修改，若有，则需要重新add)
- `git merge dev`把dev分支的工作成果合并到master分支上
- `git branch -d dev`合并完成后，就可以放心地删除dev分支了
- `git push origin master`再push到远程仓库