# git-demo
自己的仓库 需要git init初始化仓库
默认master分支

1.创建一个status分支
git branch status  

2.查看仓库分支
git branch -v
git branch -vv  查看远程和本地分支
git branch -a    查看远程和本地所有分支关系

3.新建本地分支 并切换到新分支
git checkout -b 分支名
3.2切换分支
git checkout 分支名
3.3从git远程分支拉去更改
git checkout -b 新建本地分支名 远程分支名
例：git checkout -b test origin/test

4.修改后添加到暂存区
git add .  注意后边加点

5.提交到分支
git commit -m '修改内容'

6.推送到远程分支
git push origin 远程分支名

7.删除本地分支
git branch -d  本地分支名

8.删除远程分支
git branch -r -d origin/远程分支名

9.把本地操作推送到远程
git push origin : 远程仓库名    注意：冒号前后加空格

10.重命名分支
git branch -m 旧分支名 新分支名


五、git 中一些选项解释
-d --delete：删除

-D --delete --force的快捷键

-f --force：强制

-m --move：移动或重命名

-M --move --force的快捷键

-r --remote：远程

-a --all：所有

1.github 管理
本地项目与github仓库关联：
1.创建本地仓库
2.将本地仓库变成git可管理的仓库：git init
3.把项目文件添加到缓存区：项目文件添加到已有的仓库，然后git add .（. 表示当前目前所有文件，也可以指定文件）。
4.提交项目：git commit -m "说明"
5.github创建git仓库
6.关联本地仓库：git remote add origin git@github.com:wpbxin/hello-world.git。（在此之前需要可以使用SSH进行验证配置，可以自行度娘或谷歌）
推送：git push -u origin master，由于新建的远程仓库是空的，所以要加上-u这个参数，等远程仓库里面有了内容之后，就不需要使用-u。
7.sshkey  不匹配 推送会报错
  7.1（如果客户端与服务端的SSH Key 不匹配，可以先删除本地电脑中的“id_rsa”和“id_rsa.pub”这两个文件，在输入此命令即可生成匹配的SSH Key）
  当然你也可以在桌面空白处单击鼠标右键，选择Git Bash here，然后在窗口中输入ll -d ~/.ssh也可以查询到.ssh目录的位置
8.生成新的rsa秘钥
输入命令：ssh-keygen -t rsa -C '注册GitHub的邮箱'git@github.com:zhaohui794/git-demo.git
