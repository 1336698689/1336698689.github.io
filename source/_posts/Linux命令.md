47.97.91.151
---------------------------------day1--------------------------------
命令[参数][作用对象]
1、who（who am i）、w       -    查看谁连接服务器
2、last      -           最近一段时间服务器登录记录
3、clear     -     清屏
4、date     -     查看当前时间
5、cal    cal -3 1 2019(查看2019年1月分前后1个月，共3个月)   -      查看日历
6、[命令]--help    -   查看命令帮助
7、man [命令]      -   查看命令手册
8、wget https://www.sohu.com/index.html       -   下载(url)
9、cat     -    查看文件
10、 ctrl+c   ctrl+d     -   终止光标    系统
11、上下箭头，可以调出以前命令
12、ctrl+a   j   ctrl+e     -     光标移到行首，移动到行尾
13、ctrl+w     ctrl+u   -    删除一个单词/删除整行
14、init  6   0    -     初始化  重启6    关机0
15、shutdown   -c  -r    -h   -    关机，关闭服务器之前提示消息。 取消-c关机。  重启-r   定小时关机-h
16、write[]  wall     -   给[]指定用户发消历史息。给所有人发消息
17、history     -c -     查看历史命令。清除历史命令
18、！+历史命令编号    -     重复该命令
-------------------------------------------------重要命令
19、clear   /   history      清屏/历史 命令
20、pwd     -  print working directory     -   打印工作目录 
21、ls   -a  -l   -R  -    查看文件    查看所有文件-a  长格式详细信息-l  递归式查看-R
22、cd    -     切换文件夹
23、mkdir []  -p abc/ab/c  -    创建文件夹   创建多级文件夹  -p
24、rmdir []    -   删除空文件夹
25、touch    -   创建空文件或修改最后访问时间    
26、rm     -remove    -   删除文件或文件夹
27、rm   -rf       -  删除所有的文件和子类文件/文件夹   -f强制删除  -r递归删除
28、cp  [当前文件名或者路径名+文件名] [新文件地址]    -    拷贝文件
29、mv    -   移动文件（剪切），给当前文件重命名
30、cat/tac/headr/tail            -  顺序查看文件/倒序查看/从头看/从尾看
31、more/less                     -     分页查看
32、iconv -f gb2312 -t utf-8  qq.html   -     把文件的编码转换成utf-8
33、gunzip  [文件名.tgz .gz]  gzip[]  -    解压缩文件tgz/gz为.tar格式。压缩文件
34、xz -d[文件名.xz]  -z     -       解压缩文件xz为.tar格式。 压缩文件
35、tar -xvf[文件名.tar]     -    解归档.tar的文件为多个文件

-------------------------------day2--------------------------
useradd [名字]         -      创建用户
passwd [密码]          -      创建密码
su root  |  su wangdachui     -   切换为超级管理员|切换成王大锤     
wget    -    联网下载资源文件
---------------------------------------------vim
vim .vimrc           -     进入vim样式设置
imap <F3> if __name__=='main':    -   设置快捷键
vim -d a.txt b.txt   -   打开2个文件，区别不同
vim a.txt b.txt   -> 末行：sp  vs   将2个文件切换横屏，竖屏
                         ->   ctrl + w  切换窗口 
命令模式：
移动光标： -h j k l(左下上右)          -0 $ w      -gg/G/ <num>G头/尾/指定行数
                ctrl+e /ctrl+y  /ctrl+f  /ctrl+b 
编辑内容：
dd  -  删除整行
u/ctrl+r    -  撤销/重做
d0/d$     -   从头到光标位置删除/从光标到尾删除
dw     -      删掉一个单词
保存退出：
ZZ 
末行模式:(在命令模式下按冒号)
	set nu   -    显示行号
                syntax on/off -  开启高量模式
	set ts=4   -   设置字符符为4个空格
	q!/wq    -     不保存退出/保存退出
编辑模式（在命令模式下按i或者a）

vim .vimrc  -  进入vim后台设置
set nu    -开启行号
set ts=4   -开启缩进为4空格  set tabstop=4
set autoindent   -开启自动缩进
set expandtab    
set ruler   -开启光标位置提示
set nohls    -关闭匹配的高亮显示
syntax on    -开启高量

-----------------------------------------CentOS安装软件
web服务器    ->   前端页面放到服务器上  -apache / nginx / iis
CentOS安装软件：
1.包管理工具安装（简单靠谱）
  -yum:  yellowdog updater modified
  	 -yum search <软件包名字>        -    搜索
 	 - yum install <软件包名字>        -  安装
 	 - yum upgrade<软件包名字>    -  更新
 	 - yum erase<软件包名字>         -  移除/删除
	 - yum info<软件包名字>            -   名称
	- yum list installed | grep <名字>  -  搜索指定安装的包
 systemctl start nginx    在web服务器上运行

  -apt / apt-get

  -rpm
        rpm -ivh [文件]      -   安装文件
        rpm -e 包名         - 删除
        rpm -qa | grep  包名    - 查询
2.源代码构建安装
gcc  --version  /  make --version
/下载/解压缩/解归档/补充依赖性/安装前配置/make && make install/配置环境变量

3.下载和系统对应的二进制文件
	配置PATH环境变量

安装Python3.x
1.下载源代码
wget https://
2.解压缩解归档
gunzip Python-3.7.4.tgz
tar -xvf Python-3.7.4.tar
cd Python-3.7.4
3.补充Python相关依赖项
yum -y install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel libdb4-devel libpcap-devel xz-devel libffi-devel
4.安装前的配置
./configure --prefix=/usr/local/python37 --enable-optimizations
5.构建和安装
make && make install
6.配置PATH环境变量
vim .bash_profile
export PATH=$PATH:/usr/local/python37/bin
7.重新登录或者通过下面的命令来激活环境变量
source .bash_profile

#!/usr/local/python37/bin/python3   -   程序自动找编译器
chmod u+x,g+x,o+x [py文件]             -    添加执行权限   
./[py文件]         -           执行文件

----------------------------------------day3-----------------------------------
今日内容：安装非关系型数据库redis  安装Git  安装MySQL数据库 
service mysqld start  - 启动数据库
service mysqld stop  - 关闭数据库

systemctl start mariadb   -   启动数据库
systemctl top mariadb    -   关闭数据库
systemctl restart mysqld  -  重启数据库
systemctl status mysqld   -  数据库状态
systemctl enable mysqld  -  开机启动
systemctl disable mysqld  -  关闭开机启动

create user 'root'@'112.23.255.5' identified by '123456';  -  设置IP连接
create user 'root'@'%' identified by '123456';   -   设置所有人都可以连接
grant all privileges on *.* to 'root'@'%'      -     设置root账号所有权限
grant all privileges on *.* to 'root'@'%' with grant option;     -  设置root用户所有权限,并且可以给其他用户授权
revoke all privileges on *.* from 'root'@'%';   -    收回root用户的权限
grant insert on school.* to 'root'@'%';    -    设置root用户可以插入school数据库下面的数据
cat /var/log/mysqld.log | grep password    -   查询初始密码
set global validate_password_policy = 0;    -   设置为弱口令
set global validate_password_length = 6;   -   设置为6位数密码
alter user 'root'@'localhost' identified by '123456';   -  更改密码

ps -ef    -  查看当前进行的进程
ps -ef | grep maria   -  模糊查询数据库
netstat -ntlp     -    查看使用端口      t-tcp  l-监听  p-进程名字
killra -9     -   关闭进程  -9为强行关闭

yum search mariadb    -查看数据库
yum install -y mariadb-server mariadb   -安装数据库，全部是（-y）
yum info mariadb    -    查看名字
yum upgrade mariadb    -    检查更新
yum erase mariadb mariadb-server   -  卸载
yum list installed | grep mariadb | awk '{print $1}' | xargs yum erase -y   -   老师应用卸载
yum list installed | grep mariadb    -   查看安装列表 ,查看指定文件

&& 第一个成功，就执行第二个     || 第一个没成功，执行第二个   ；一次执行

源代码构建安装Git      
下载注意：  nohup wget  [地址] > download.log &  -  服务器不中断就继续在后台下。&后台运行
ps  -ef  / jobs  -查看进程
1. wget https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.23.0.tar.gz   -  下载
2.gunzip git-2.23.0.tar.gz   -  解压
tar -xvf git-2.23.0.tar         -  解压归档
cd git-2.23.0                       -  进入文件夹
3. yum install -y libcurl-devel   -  安装一个网络运行包
4. ./configure --prefix=/usr/local  - 安装前的配置
5.make && make install    - 构建和安装
6.git --version         -   查看版本

---------------------------------老师代码【CentOS安装软件】
CentOS安装软件：
1. 包管理工具安装（简单靠谱）
	- yum：yellowdog updater modified
		- yum search <软件包名字>
		- yum install <软件包名字>
		- yum upgrade <软件包名字>
		- yum erase <软件包名字>
		- yum info <软件包名字>
		- yum list installed | grep <名字>
	- apt / apt-get
	- rpm：red-hat package manager
		- rpm -ivh RPM文件
		- rpm -e 包名
		- rpm -qa | grep 包名
2. 源代码构建安装
	- gcc --version / make --version
	- 下载 / 解压缩 / 解归档 / [补充依赖项] / [安装前配置] / make && make install / [配置环境变量]
3. 下载和系统对应的二进制文件
	- 配置PATH环境变量

ln -s /usr/local/python37/bin/python3 /root/python  - 软链接
ln /usr/local/python37/bin/python3 /root/python      -  硬链接

----------------------------------------day4-----------------------------------
github.com   -   代码托管平台   -  Git服务器   -  国外服务器
gitee.com   -  码云  -  Git服务器    -   中国服务器（学习使用）
版本控制（软件控制管理） -  Git
CVS/VSS锁定模式 -> SVN合并模式（必须要有版本控制服务器） ->Git合并模式（分布式版本控制系统）
git init   -   把文件夹变成版本控制仓库
git status   -   查看版本控制状态
git add []  -     添加文件到仓库缓存区
git rm --cached []  -  将文件从仓库缓存区中取出到工作区
git restore --staged[]  -  将文件从仓库缓存区中取出到工作区
git config --global user.name "Mr Tao"
git config --global user.email "133..@qq.com"
git commit -m '提交原因'   -   将仓库缓存区的文件上传到版本控制
git reset --hard head^   --hard [版本号]   -    工作区恢复到上一个版本/回复到版本号那个版本
git relog   -  查看增删日志
git log  -   查看提交日志
git restore[]  -    将删除的文件回复到控制版本
-----------------------------------------分支操作
git branch -a   -    查看所有的分支
git branch work  -   创建分支
git branch -b work   -  创建切换到work
git checkout    -     切换分支
git branch -d work   -   删除分支
git merge []           -    合并分支
git diff  -    查看分支记录
-----------------------------------------码云
git remote add origin https://gitee.com/tao_chao/tao_chao.git    -   连接码云仓库 
git remove origin     -      删除远端仓库 
git push -u origin master       -    把master分支上传到我的码云仓库
git pull origin master        -    把码云仓库跟新的内容更新到本地

git clone [远端仓库的url]    -     把远端服务器的仓库克隆到本地

ssh-keygen -t rsa -b 2048 -C "1336698689@qq.com"    -    创建密码
cat id_rsa.pub   -   复制连接
添加ssh公钥  ->  复制ssh连接   -> 切换到.ssh目录  -> git clone ssh_url  下载证书 yes




------------------------------------------------老师代码
版本控制（软件控制管理）
1990s - CVS / VSS - 锁定模式
2000 - Subversion（SVN）- 合并模式 - 中央集权型版本控制系统 - 必须要有版本控制服务器
BitKeeper
2005 - Git - 合并模式 - 分布式版本控制系统 

1. 初始化版本仓库
git init
2. 查看状态
git status
3. 将文件放到缓存区（暂存区）
git add <filename>
git add .
4. 将文件移除缓存区
git rm --cached <filename>
5. 用缓存区恢复工作区
git restore --staged <filename>
6. 将缓存区内容提交到仓库
git config --global user.name "用户名"
git config --global user.email "邮箱"
git commit -m '提交日志(原因)'
7. 查看提交日志
git log
git reflog
8. 回退版本
git reset --hard HEAD^
git reset --hard 版本代码

---------------------------------------------day5-----------------------------------
命令 &  - 把进程（命令）扔到后台运行
jobs  -   查看后台任务（暂停/运行/已完成）
fg %<num>  -   将后台任务至于前台运行
bg %<num> -   让任务在后台运行
Ctrl+z     -          将前台任务暂停放到后台

ps -ef / ps -aux
pgrep - 根据进程名搜索进程

wget   -   下载文件
ifconfig  -   查看网卡信息
ip     -     获取和网络相关的各种信息
netstat -na    -   网络状态
	-t/-u/-a  查看协议
	-l      
	-n     -ip地址
	-p     -进程

sftp   -   安全文件传输
sftp root@1.2.3.4
sftp>   ls cd get(下载) 
            put(上传) 
            bye

远程安全文件拷贝
scp 源文件 目标文件
scp hell.txt root@120.77.222.217:/root/abc.text

cp [] []


-------------------------------------pycharm
生成依赖项清单
pip freeze > requirements.txt
根据依赖项清单安装三方库：
pip install -r requirements.txt -i https://pypi.doubanio.com/simple
不纳入版本控制的文件和文件夹的清单  ->  .gitignore

--------------------------------------安装hexo
yum install -y nodejs     -   安装node.js
npm install -g hexo-cli     -   安装hexo命令行工具
hexo init blog      -     初始化博客项目
cd blog               -   进入blog文件
npm install          -    安装项目依赖项
hexo g               -    通过markdown文件生成（generate)页面
systemctl stop nginx   -  停止nginx 80端口
hexo s -p 80               启动服务器（server)运行博客项目


总结：
第一天：FinalShell安装（操作使用）
第二天：1、vim的操作使用； 2、包管理工具:yum-rpm-wget;3、安装pythono3.0流程
第三天：1、安装非关系型数据库redis ； 2、安装Git ；3、 安装MySQL数据库
第四天：1、git基本操作。2、本地git上传码云服务器的流程
第五天：1、剩余FinalShell的操作讲解；2、pycharm安装及克隆GIT服务器；3、安装使用hexo，搭建博客

---------------------------------day6--------------------------------
---------------------------------shell脚本使用
printf      - 输入
read 变量名      -等待输入
alias         -  别名
unalias     -取消别名   
vim /etc/bashrc    -   42行更改
vim .bash_profile   -   设置登录欢迎
bash a.sh            - 执行.sh脚本语 言
chmod 755 a.sh   -给权限       
	./a.sh    -执行.sh脚本语言
----------------------------------at计划的使用
at 14:00+3days     -   预约3天后下午2点要做的事
	at rm -f /root/a.sh   - 到时间删除root下面的a.sh
atq        -     查看预约任务的队列
strm[编号]     -     取消预约[编号]
----------------------------------crontab定时任务执行
crontab -e      -  开启定时任务
	* * * * *       分 时 日 月 星期
	59 23 * * *

----------------------------------------数据库
关系型数据库： Oracle / DB2 / MySQL / Sybase / SQLServer / SQLite / postgreSQL
编程语言：SQL  -  结构化查询语言
	-DDL   - 数据定义语言       create / drop / alter
	-DML  - 数据操作语言        inster / delete / update / select    -CRUD
	-DCL   - 数据控制语言        grant / revoke
非关系型数据库：MongoDB / Redis / ElasticSearch

----------------------------------------mysql
systemctl start mysqld   -  开启mysql
netstat -ntlp  -   查看端口  netstat -ntlp | grep mysqlc
 create database school default charset utf8;   -  创建数据库
alter table tb_student add constraint pk_student_stuid primary key (stuid);
drop table tb_student;
insert into tb_student values (1001,'王大锤',1,'1992-2-2','四川成都');
insert into tb_student(stuid,stuname) values (1002,'露易斯');

SQLyog Community  (海豚)

-------------------------------------------------老师代码
数据库 - 数据的集散地（仓库）- database
关系型数据库 - 1970s 
Oracle / DB2 / MySQL / Sybase / SQLServer / SQLite / PostgreSQL

理论基础：关系代数 + 集合论
具体表现形式：用二维表来保存数据
	- 行：记录（record）
	- 列：字段（field）- 主键列（primary key）
编程语言：SQL - 结构化查询语言
	- DDL - 数据定义语言 - create / drop / alter
	- DML - 数据操作语言 - insert / delete / update / select - CRUD
	- DCL - 数据控制语言 - grant / revoke

rpm包管理工具安装MySQL
rpm -ivh mysql-community-common-xxx.rpm
rpm -ivh mysql-community-libs-xxx.rpm
rpm -ivh mysql-community-client-xxx.rpm
rpm -ivh mysql-community-server-xxx.rpm

systemctl start mysqld
journalctl -xe / systemctl status mysqld
netstat -ntlp | grep mysql

mysql [-h 主机IP地址] -u 用户名 -p

create database school default charset utf8;
drop database school;

use school;

create table tb_student
(
stuid integer not null,
stuname varchar(20) not null,
stusex boolean default 1,
stubirth date,
stuaddr varchar(250)
);

alter table tb_student add constraint pk_student_stuid primary key (stuid);

drop table tb_student;

insert into tb_student values (1001, '王大锤', 1, '1992-2-2', '四川成都'); 
insert into tb_student (stuid, stuname) values (1002, '白元芳');
insert into tb_student (stuid, stuname, stusex) values 
(1004, '白洁', 0),
(1005, '武则天', 0),
(1006, '冷面', 1);

非关系型数据库 - 1998 - NoSQL
MongoDB / Redis / ElasticSearch
No SQL
No, SQL
Not Only SQL 









