git init 初始化本地库

##### 设置签名

git config user.name 用户名

git config user.eamail 邮箱

##### 状态查看操作

git status 查看工作区、暂存区状态

##### 添加操作

git add [文件名 ]     将工作区的新建修改添加到暂存区

##### 提交操作

git commit -m "描述备注信息" [文件名]  将暂存区内容提交到本地库

##### 查看历史记录

`git log` 

多屏显示控制方式  

空格向下翻页  b向上翻页  q退出

`git log --pretty=oneline`

`git log --oneline`

`git reflog` 显示所有历史记录

##### 版本前进后退

基于索引值考虑  `git reset --hard[局部索引]`

使用^符号 只能后退 `git reset --hard HEAD^`   <!--一个^表示后退一步，n个表示后退n步-->

使用~符号：只能后退 git reset --hard HEAD~n     <!--表示后退n步-->

比较文件的差异

git diff[文件名]   将工作区中的文件和暂存区进行比较

git diff[本地库中历史文件] [文件名] 将工作区的文件和本地库历史记录比较

#### 分支管理

创建分支 `git branch[分支名]`

查看分支 `git branch -v`  

切换分支 `git checkout[分支名]`

合并分支

第一步：切换到接受修改的分支（主合并，增加新内容）上

​                `git checkout[主合并分支名]`

第二步：执行merge命令

​                 `git merge[被合并，有新内容的分支名]`

##### 分支冲突的解决

第一步：编辑文件，删除特殊符号

第二部：把文件修改到满意的程度，保存退出

第三步：git add[文件名]

第四步： git commit -m "日志信息“            注意此时commit一定不能带具体文件名

##### 推送操作

远程连接 git remote add origin(origin是起的别名)  [github地址]

推送`git  push origin master`

##### 拉取操作

pull=fetch + mergin

git fetch[远程仓库地址别名 [远程分支名]

git merge [远程库地址别名/远程分支名]

git pull [远程库地址别名 [远程分支名]

##### 冲突解决

如果不是基于GitHub远程库的最新版所做的修改，不能推送，必须先拉取

拉取下来如果进入冲突状态，则按照分支冲突解决  操作



这里是二台

