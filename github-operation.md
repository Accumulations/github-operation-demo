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

##查看历史
`git log`

##强制覆盖远程
- `git push -f origin master`当上传到远程报错的时候
- 如果第一次从本地文件夹上传到远程，且远程有文件（非第一次，或者第一次已创建README.md），则无法将本地文件上传到远程。

##第一次从本地上传文件到远程
- `mkdir file_name`创建一个本地的版本库（其实也就是一个文件夹）
- `cd file_name`进入文件夹
- `git init`将文件夹变成Git可管理的仓库
- 把你的项目粘贴到这个本地Git仓库里面，且可通过`git status`查看状态
- `git add .`和`git commit -m "xx"`将文件上传到本地库
- 在Github上创建一个Git仓库`file_name` （第一次可以不点README.md,如果点了，则需要先将远程仓库文件pull拉取下来，否则需要进行强制覆盖远程）
    - 如果你勾选了Initialize this repository with a README（就是创建仓库的时候自动给你创建一个README文件），那么到了第九步你将本地仓库内容推送到远程仓库的时候就会报一个failed to push some refs to  https://github.com/guyibang
TEST2.git的错。这是由于你新创建的那个仓库里面的README文件不在本地仓库目录中，这时我们可以通过以下命令先将内容合并以下
    - `git pull --rebase origin master`

- `git remote add origin https://github.com/Accumulations/file_name.git`将本地仓库与远程仓库进行关联
- `git push -u origin master`把本地库的所有内容推送到远程仓库， 由于新建的远程仓库是空的，所以要加上-u这个参数，等远程仓库里面有了内容之后，下次再从本地库上传内容的时候只需下面这样就可以了`git push origin master`