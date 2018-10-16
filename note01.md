#First Day
##Afternoon
###Linux基本命令
    1.pwd   查看当前位置
    1.cd 路径  进入此文件内
    1.cd~ 回到根目录
    1.cd / 回到root的根目录
    1.ls  查看当前路径下的文件
    1.rm -rf 有*是删除当前路径下的所有文件+文件名，删除此文件
    1.echo “内容” >> 文件名  把“内容”写进“文件名里”，如果没有此文件，则新建后写入。
    1.mkdir 文件名 创建文件夹
    1.touch 文件名 创建新文件
###git命令（注意：创建文件一定要.md的）
####创建版本库
    1.git clone <url>  克隆远程版本库
    2.git init 初始化本地版本库
####修改和提交
    1.git status 查看状态
    2.git diff 查看变更内容
    3.git add 跟踪所有改动过的文件
    4.git add <file> 跟踪指定的文件
    5.git mv <old> <new> 文件更名
    6.git rm <file> 删除文件
    7.git rm --cached<file> 停止跟踪文件但不删除
    8.git commit -m “commit message” 提交所有更新过的文件
    9.git commit --amend 修改最后一次提交
####查看提交历史
    1.git log 查看提交历史
    2.git log -p <file> 查看指定文件的提交历史
    3.git blame <file> 以列表方式查看指定文件
####撤销
    1.git reset --hard HEAD 撤销工作目录所有未提交文件的修改内容
    2.git checkout HEAD <file> 撤销指定的未提交的文件的修改内容
    3.git revert <commit> 撤销指定的提交
####分支与标签
    1.git branch 显示所有本地分支
    2.git checkout<branch/tag> 切换到指定的分支或标签
    3.git branch <new-branch> 创建新分支
    4.git branch -d <branch> 删除本地分支
    5.git tag 列出所有本地标签
    6.git tag <tagname> 基于最新提交创建标签
    7.git tag -d <tagname> 删除标签
####合并与衍合
    1.git merge <branch> 合并指定分支到当前分支
    2.git rebase <branch> 衍合指定分支到当前分支
####远程操作
    1.git remote -v 查看远程版本库信息
    2.git remote show <remote> 查看指定远程版本库信息
    3.git remote add <remote> <url> 添加远程版本库
    4.git fetch <remote> 从远程库获取代码
    5.git pull <remote> <branch> 下载代码及快速合并
    6.git push <remote> <branch> 上传代码及快速合并
    7.git push <remote> :<branch/tag-name> 删除远程分支或标签
    8.git push --tags 上传所有标签
####其他
    1.ssh-keygen -t rsa -C “邮箱” 生成ssh秘钥，输入命令后，连按三个回车即可生成ssh秘钥
    2.git commit -m “标签名” 用commit推送修改到本地库中。此标签名可以用来当作坐标，以便回档
    3.git config --global user.email“邮箱号”
      git config --global user.name“名字”
    4.git push -u origin master 使用-u选项指定一个默认主机，这样后面就可以不参加任何参数使用git push 添加到服务器中
###创建博客
    ####用git bash 操作博客
    1.cd~ （用此口令之后口令可以用tab补全）
    2.pwd
    3.cd Desktop/
    4.git clone博客名（来自如下）（直接克隆克隆不到，需要先生成公钥）
    5.ssh-keygen -t rsa -C "邮箱名" 生成博客的公钥（按三次回车,得到一个文件，把文件里的公钥copy到博客里（点击用户的setting，找到SSH and GPG keys ,找到 New SSH key,copy进去）））））））） 
    6.git clone 博客名 
    7.cd博客文件夹，进入博客文件夹中
    8.ls查看当前文件夹里的文件
    9.git status 查看状态码
    10.touch文件名.md（创建文件，并编写文件）
    11.git add文件名.md（把内容放进缓冲区）
    12.git commit -m “first commit”（防止进行这步操作时系统崩溃，好回到上一步）
    13.git config --global user.email “邮箱名”
    14.git config --global user.name “博客名”
    15.git commit -m “first commit”
    16.git push -u origin master（把文件上传）