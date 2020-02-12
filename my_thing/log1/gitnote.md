### 率先有[廖雪峰的网红教程](https://www.liaoxuefeng.com/wiki/896043488029600)

附带自己的笔记



Git 常用代码笔记
git init 创建一个待管理仓库
git add readme.txt 把文件放到Git仓库
git commit -m “描述”把文件提交到仓库
git remote -v 查看远程仓库关联本地仓库的情况
git clone + <远程仓库URL>  直接将远程仓库克隆到本地
git pull 取回远程主机某个分支的更新，再与本地的指定分支合并。它的完整格式稍稍有点复杂
$ git pull <远程主机名> <远程分支名>:<本地分支名>
$ git pull origin next:master
取回origin主机的next分支，与本地的master分支合并
如果远程分支是与当前分支合并，则冒号后面的部分可以省略
注意多次add一次commit因为commit可以一次性把仓库里的所有的文件全部提交，文件内的内容只有add进入git仓库才能进行跟踪
git status 查看当前状态
git diff 比较staging area和working area的文件区别
git diff master 比较master分支和working area的文件区别
git diff HEAD 比较HEAD指向的内容和working area的文件区别
git log 显示最近到最远的提交日志
git log –pretty=oneline 加了这个参数看起来更好一点
git reflog 记录你的每一条命令
git reset –hard commit_id 允许我们在版本历史之间穿梭
git log 穿梭前使用该命令确定所要穿梭的过去版本
git reflog 查看历史命令以便确定回退到那个未来的版本
git checkout -b dev 创建并切换至dev分支相当于
git branch dev(创建分支)
git checkout dev(切换分支) 
两条命令
git branch 查看当前分支
git merge dev g命令用于合并指定dev支到当前分支
git branch -d dev 删除devf分支
git log --graph查看分支合并图


场景小结：
1、乱改了个的文件但是后悔了，git checkout file,直接丢弃工作区的修改，将工作区的状态和暂存区的状态保持一致
2、当不但乱改了某个文件，而且还添加到了暂存区，先git reset HEAD file将暂存区的文件覆盖为最新的指针指向的版本，再使用上一步同步

要关联一一个远程库,使用用命令 git remote add origin git@github:Vity-github/learngit.git
关联后,使用用命令 git push -u origin master 第一一次推送master分支支的所有内容;
此后,每次本地提交后,只要有必要,就可以使用用命令 git push origin master 推送最新修
改;



要克隆一一个仓库,首首先必须知道仓库的地址,然后使用用 git clone git@github:Vity-github/learngit.git




Git工作原理

