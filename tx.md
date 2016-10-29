What are you dong?

cd E:/  进入目录

ls 显示文件或目录（相当于查看）  [ ls -al ] 查看当前目录下的所有文件，包括隐藏的

mkdir  创建目录

touch 创建文件-

echo Hello > README.md   创建文件 README.md 内容为 Hello


pwd 显示当前路径

clear 清屏

cat 查看文件内容

git init  在指定目录下创建 .git 可以认为就是仓库

git status 获取当前工作目录的状态，那些是添加的，那些是修改的

git add xxx.md  将文件添加到仓库

git commit 提交，把缓冲区的内容，提交到仓库内部的数据库，修改的历史
（跳转到页面 ，按 a 可以进行编辑  ， 按 Esc 键  再按 shift + :  输入 wq 退出）

git commit -am "提交时标记的名字"   （就直接提交了，不需要跳转页面）（ -a 代表提交了所有的修改， - m 后面跟随提交的日志）


git log 查看提交的日志

git log xxx.md  查看该文件每次的提交记录

git log --help 查看详细的日志

git  --help 查看 git 有哪些指令

gitk 所有的提交都显示出来，

git gui UI窗口操作



git 远程服务
1.创建应用
2， 在创建的应用中添加公钥，（ 公钥的生成 ，在 git Bush 命令行 输入 git gui 进入 UI 窗口，点击右上角的 help ，然后 SSE 公钥） 
3.命令行输入 cd  波浪线 / .ssh/    ( 公钥生成在  C:\Users\Administrator\.ssh)  
4.ls

5. git remote add origin git@git.oschina.net:www_wang/GitDemo.git （连接）

6.git push -u origin master （提交）




Git常用命令
查看、添加、提交、删除、找回，重置修改文件

git help <command> # 显示command的help

git show # 显示某次提交的内容 git show $id

git co -- <file> # 抛弃工作区修改

git co . # 抛弃工作区修改

git add <file> # 将工作文件修改提交到本地暂存区

git add . # 将所有修改过的工作文件提交暂存区

git rm <file> # 从版本库中删除文件

git rm <file> --cached # 从版本库中删除文件，但不删除文件

git reset <file> # 从暂存区恢复到工作文件

git reset -- . # 从暂存区恢复到工作文件

git reset --hard # 恢复最近一次提交过的状态，即放弃上次提交后的所有本次修改

git ci <file> git ci . git ci -a # 将git add, git rm和git ci等操作都合并在一起做　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　git ci -am "some comments"

git ci --amend # 修改最后一次提交记录

git revert <$id> # 恢复某次提交的状态，恢复动作本身也创建次提交对象

git revert HEAD # 恢复最后一次提交的状态

查看文件diff

git diff <file> # 比较当前文件和暂存区文件差异 git diff

git diff <id1><id1><id2> # 比较两次提交之间的差异

git diff <branch1>..<branch2> # 在两个分支之间比较

git diff --staged # 比较暂存区和版本库差异

git diff --cached # 比较暂存区和版本库差异

git diff --stat # 仅仅比较统计信息

查看提交记录

git log  <file> # 查看该文件每次提交记录

git log -p <file> # 查看每次详细修改内容的diff

git log -p -2 # 查看最近两次详细修改内容的diff

git log --stat #查看提交统计信息

tig

Mac上可以使用tig代替diff和log，brew install tig

Git 本地分支管理

查看、切换、创建和删除分支

git br -r # 查看远程分支

git br <new_branch> # 创建新的分支

git br -v # 查看各个分支最后提交信息

git br --merged # 查看已经被合并到当前分支的分支

git br --no-merged # 查看尚未被合并到当前分支的分支

git co <branch> # 切换到某个分支

git co -b <new_branch> # 创建新的分支，并且切换过去

git co -b <new_branch> <branch> # 基于branch创建新的new_branch

git co $id # 把某次历史提交记录checkout出来，但无分支信息，切换到其他分支会自动删除

git co $id -b <new_branch> # 把某次历史提交记录checkout出来，创建成一个分支

git br -d <branch> # 删除某个分支

git br -D <branch> # 强制删除某个分支 (未被合并的分支被删除的时候需要强制)

 分支合并和rebase

git merge <branch> # 将branch分支合并到当前分支

git merge origin/master --no-ff # 不要Fast-Foward合并，这样可以生成merge提交

git rebase master <branch> # 将master rebase到branch，相当于： git co <branch> && git rebase master && git co master && git merge <branch>

 Git补丁管理(方便在多台机器上开发同步时用)

git diff > ../sync.patch # 生成补丁

git apply ../sync.patch # 打补丁

git apply --check ../sync.patch #测试补丁能否成功

 Git暂存管理

git stash # 暂存

git stash list # 列所有stash

git stash apply # 恢复暂存的内容

git stash drop # 删除暂存区

Git远程分支管理

git pull # 抓取远程仓库所有分支更新并合并到本地

git pull --no-ff # 抓取远程仓库所有分支更新并合并到本地，不要快进合并

git fetch origin # 抓取远程仓库更新

git merge origin/master # 将远程主分支合并到本地当前分支

git co --track origin/branch # 跟踪某个远程分支创建相应的本地分支

git co -b <local_branch> origin/<remote_branch> # 基于远程分支创建本地分支，功能同上

git push # push所有分支

git push origin master # 将本地主分支推到远程主分支

git push -u origin master # 将本地主分支推到远程(如无远程主分支则创建，用于初始化远程仓库)

git push origin <local_branch> # 创建远程分支， origin是远程仓库名

git push origin <local_branch>:<remote_branch> # 创建远程分支

git push origin :<remote_branch> #先删除本地分支(git br -d <branch>)，然后再push删除远程分支

Git远程仓库管理

GitHub

git remote -v # 查看远程服务器地址和仓库名称

git remote show origin # 查看远程服务器仓库状态

git remote add origin git@ github:robbin/robbin_site.git # 添加远程仓库地址

git remote set-url origin git@ github.com:robbin/robbin_site.git # 设置远程仓库地址(用于修改远程仓库地址) git remote rm <repository> # 删除远程仓库

创建远程仓库

git clone --bare robbin_site robbin_site.git # 用带版本的项目创建纯版本仓库

scp -r my_project.git git@ git.csdn.net:~ # 将纯仓库上传到服务器上

mkdir robbin_site.git && cd robbin_site.git && git --bare init # 在服务器创建纯仓库

git remote add origin git@ github.com:robbin/robbin_site.git # 设置远程仓库地址

git push -u origin master # 客户端首次提交

git push -u origin develop # 首次将本地develop分支提交到远程develop分支，并且track

git remote set-head origin master # 设置远程仓库的HEAD指向master分支

也可以命令设置跟踪远程库和本地库

git branch --set-upstream master origin/master

git branch --set-upstream develop origin/develop






			Linux 常用指令



ls　　        显示文件或目录

     -l           列出文件详细信息l(list)

     -a          列出当前目录下所有文件及目录，包括隐藏的a(all)

mkdir         创建目录

     -p           创建目录，若无父目录，则创建p(parent)

cd               切换目录

touch          创建空文件

echo            创建带有内容的文件。

cat              查看文件内容

cp                拷贝

mv               移动或重命名

rm               删除文件

     -r            递归删除，可删除子目录及文件

     -f            强制删除

find              在文件系统中搜索某文件

wc                统计文本中行数、字数、字符数

grep             在文本文件中查找某个字符串

rmdir           删除空目录

tree             树形结构显示目录，需要安装tree包

pwd              显示当前目录

ln                  创建链接文件

more、less  分页显示文本文件内容

head、tail    显示文件头、尾内容

ctrl+alt+F1  命令行全屏模式

 

系统管理命令

stat              显示指定文件的详细信息，比ls更详细

who               显示在线登陆用户

whoami          显示当前操作用户

hostname      显示主机名

uname           显示系统信息

top                动态显示当前耗费资源最多进程信息

ps                  显示瞬间进程状态 ps -aux

du                  查看目录大小 du -h /home带有单位显示目录信息

df                  查看磁盘大小 df -h 带有单位显示磁盘信息

ifconfig          查看网络情况

ping                测试网络连通

netstat          显示网络状态信息

man                命令不会用了，找男人  如：man ls

clear              清屏

alias               对命令重命名 如：alias showmeit="ps -aux" ，另外解除使用unaliax showmeit

kill                 杀死进程，可以先用ps 或 top命令查看进程的id，然后再用kill命令杀死进程。

 

打包压缩相关命令

gzip：

bzip2：

tar:                打包压缩

     -c              归档文件

     -x              压缩文件

     -z              gzip压缩文件

     -j              bzip2压缩文件

     -v              显示压缩或解压缩过程 v(view)

     -f              使用档名

例：

tar -cvf /home/abc.tar /home/abc              只打包，不压缩

tar -zcvf /home/abc.tar.gz /home/abc        打包，并用gzip压缩

tar -jcvf /home/abc.tar.bz2 /home/abc      打包，并用bzip2压缩

当然，如果想解压缩，就直接替换上面的命令  tar -cvf  / tar -zcvf  / tar -jcvf 中的“c” 换成“x” 就可以了。

 

关机/重启机器

shutdown

     -r             关机重启

     -h             关机不重启

     now          立刻关机

halt               关机

reboot          重启

 

Linux管道

将一个命令的标准输出作为另一个命令的标准输入。也就是把几个命令组合起来使用，后一个命令除以前一个命令的结果。

例：grep -r "close" /home/* | more       在home目录下所有文件中查找，包括close的文件，并分页输出。

 

Linux软件包管理

dpkg (Debian Package)管理工具，软件包名以.deb后缀。这种方法适合系统不能联网的情况下。

比如安装tree命令的安装包，先将tree.deb传到Linux系统中。再使用如下命令安装。

sudo dpkg -i tree_1.5.3-1_i386.deb         安装软件

sudo dpkg -r tree                                     卸载软件

 

注：将tree.deb传到Linux系统中，有多种方式。VMwareTool，使用挂载方式；使用winSCP工具等；

APT（Advanced Packaging Tool）高级软件工具。这种方法适合系统能够连接互联网的情况。

依然以tree为例

sudo apt-get install tree                         安装tree

sudo apt-get remove tree                       卸载tree

sudo apt-get update                                 更新软件

sudo apt-get upgrade        

 

将.rpm文件转为.deb文件

.rpm为RedHat使用的软件格式。在Ubuntu下不能直接使用，所以需要转换一下。

sudo alien abc.rpm

 

vim使用

vim三种模式：命令模式、插入模式、编辑模式。使用ESC或i或：来切换模式。

命令模式下：

:q                      退出

:q!                     强制退出

:wq                   保存并退出

:set number     显示行号

:set nonumber  隐藏行号

/apache            在文档中查找apache 按n跳到下一个，shift+n上一个

yyp                   复制光标所在行，并粘贴

h(左移一个字符←)、j(下一行↓)、k(上一行↑)、l(右移一个字符→)

 

用户及用户组管理

/etc/passwd    存储用户账号

/etc/group       存储组账号

/etc/shadow    存储用户账号的密码

/etc/gshadow  存储用户组账号的密码

useradd 用户名

userdel 用户名

adduser 用户名

groupadd 组名

groupdel 组名

passwd root     给root设置密码

su root

su - root 

/etc/profile     系统环境变量

bash_profile     用户环境变量

.bashrc              用户环境变量

su user              切换用户，加载配置文件.bashrc

su - user            切换用户，加载配置文件/etc/profile ，加载bash_profile

更改文件的用户及用户组

sudo chown [-R] owner[:group] {File|Directory}

例如：还以jdk-7u21-linux-i586.tar.gz为例。属于用户hadoop，组hadoop

要想切换此文件所属的用户及组。可以使用命令。

sudo chown root:root jdk-7u21-linux-i586.tar.gz

 

文件权限管理

三种基本权限

R           读         数值表示为4

W          写         数值表示为2

X           可执行  数值表示为1



如图所示，jdk-7u21-linux-i586.tar.gz文件的权限为-rw-rw-r--

-rw-rw-r--一共十个字符，分成四段。

第一个字符“-”表示普通文件；这个位置还可能会出现“l”链接；“d”表示目录

第二三四个字符“rw-”表示当前所属用户的权限。   所以用数值表示为4+2=6

第五六七个字符“rw-”表示当前所属组的权限。      所以用数值表示为4+2=6

第八九十个字符“r--”表示其他用户权限。              所以用数值表示为2

所以操作此文件的权限用数值表示为662 