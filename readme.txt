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

git push -u origin 分支    # 将版本推送至  github    -u 可以省略？


# 克隆 远程仓库代码，内部已经设置别名 origin ，不需要再次设置了
git clone 远程仓库地址    # 克隆 远程仓库内容


git pull origin  分支名    # 更新远程仓库内容


五、 冲突的解决
问题：
在公司写了功能  merge.txt 中的50%，忘了push到 github 就回了家
回家后根据记忆写了 merge.txt中的其他功能，  然后又写了 merge_home.txt，push到了github
==》第二天到公司时，pull后会发现， merge.txt发生冲突：

CONFLICT (add/add): Merge conflict in merge.txt
Auto-merging merge.txt
Automatic merge failed; fix conflicts and then commit the result.

处理：

ls    # 列出文件名

vim merge.txt   # 打开提示冲突的文件，手动处理。 

【vim 操作 esc退出编辑模式，i进入编辑模式； esc到非编辑模式后， 两次 d d 键可删除行】


处理好冲突后，继续开发，提交。




【小知识】

git pull origin dev 相当于两句：

git fetch origin dev     # 从远程仓库拉取dev到本地版本库。 再合并
git merge origin/dev     #  origin/dev  中间有 /,前面有 origin ，表示合并的是远程仓库拉来的 dev





