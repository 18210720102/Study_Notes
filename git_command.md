## Git命令行

[教程](https://www.liaoxuefeng.com/wiki/896043488029600)


mkdir 目录名称（最好是全英文）	//创建一个目录

cd 目录名称 	//转到目录下          
cd ..			//返回上一级目录            
ls				//显示当前目录下的所有文件                

git init   		//创建空的仓库(repository)

git add 文件名称	//将文件添加到repository

git commit -m "提交说明(用于说明本次提交的意义)"	//提交文件

git log 		//查看提交历史记录

git reset --hard HEAD^		//将当前版本退回到上一个版本             
git reset --hard HEAD^^		//将当前版本退回到上上一个版本            
git reset --hard HEAD~100	//将当前版本退回到上100个版本           

git reset --hard 版本号(不用写全)  	//将当前版本转到任意版本

cat 文件名称		//查看文件内容

git reflog		//记录每一次命令

git diff HEAD -- 文件名称	//查看工作区和版本库里最新版本的区别

git checkout --文件名称		//将文件回到最近一次 git add 或 git commit 时的版本

git reset HEAD 文件名称		//将暂存区的文件退回至工作区

rm 文件名称			//删除文件

git rm 文件名称			//在版本库中删除文件                
gir commit -m "说明"	//一般在删除版本库中的文件后，需再次commit

git remote add origin git@github.com:18210720102/仓库名称.git      
//将本地仓库与远程库连接，远程库的名字为origin             
git push -u origin 分支名称 	//将本地库的内容推送到远程库，第一次推送，加-u参数，后面推送可不用加

git clone git@github.com:18210720102/仓库名称.git              
//将远程库中仓库克隆到本地

git checkout -b 分支名称		//创建分支，并切换到此分支                    
//等效于以下两句命令            
git branch 分支名称		//创建分支               
git checkout 分支名称	//切换分支    

git switch -c 分支名称		//创建分支，并切换到此分支                  
git switch 分支名称		//切换分支		使用switch命令更容易理解


git branch			//查看当前分支              
git branch -d 分支名称 		//删除分支            
git branch -D 分支名称		//强行删除分支 

git merge 分支名称		//将指定分支合并到当前分支

git merge --no-ff		//表示禁用 Fast forward 模式进行分支合并

git stash 		//将工作现场“储存”起来，等以后恢复现场后继续工作

git stash list  //查看被储存的工作现场

git stash apply 	//恢复现场，但stash内容不删除                     
git stash drop  	//删除stash内容

git stash pop 		//恢复的同时删除stash内容

git cherry-pick commit序列号（部分即可）	//用于复制一个特定的提交到当前分支

git tag 标签名称		//在当前分支打一个标签，打在最新的commit上                 
git tag 标签名称 commit序列号（部分即可）		//在当前分支的某一个commit上打标签

git tag 		//查看所有标签

git tag -d 标签名称		//删除标签

git push origin 标签名称	//推送某个标签到远程

git push origin --tags		//一次性推送全部标签

//要删除远程标签             
git tag -d 标签名称						//删除本地标签            
git push origin :refs/tags/标签名称		//删除远程标签       

























