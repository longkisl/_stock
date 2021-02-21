这是B站  《git 基础7小时极速入门》 的练习



一、安装 git 后，需要先配置


$ git config --global user.name "longkisl"

$ git config --global user.email "1299893363@qq.com"

二、 基本命令

git status     # 查看状态， 

git add    文件名/ .    # 加入文件，或所有文件

git  commit -m  '版本号'   # 生成一个版本


git log    # 查看生成记录



git reflog 


git reset --hard   版本号



三、 分支

git branch    # 查看分支

git banch  分支名  # 创建一个新的分支

git checkout 分支名   # 切换到分支


git merge  待合并的分支    # 需要先切换当前分支到要合并到的分支



git branch -d  分支名   # 删除分支 【需要分支先被 合并了】

git branch -D  分支名    # 删除未合并的分支 


四、基于 github做代码托管

git remote add origin https://github.com/longkisl/_stock.git    #  给远程仓库起一个别名 origin

git push -u origin master 

