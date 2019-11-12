命令名称 [命名参数] [命令对象]



一、日常操作

1.cd指令   	- 进入指定文件夹

cd  目录	 - 进入指定目录(也可以是文件夹对应的路径)

​			   ~相对路径 — 绝对路径



cd  ..  	 - 返回上层目录

cd  ~	- 回到根目录

cd  /    - 进入系统根目录





\2. ls指令		- 查看当前目录中的内容

ls

ls  -l/-lh              -  查看详情

ls -a   			- 隐藏文件也一起显示

ls -R			- 递归显示所有内容

ls -S/-t			- 按大小/时间排序



注意: 多个功能不冲突的参数可以同时使用，中间用空格隔开, 例如 -  (ls -lh -S)





3.pwd指令 		- 显示当前完整目录

pwd







4.文件操作指令

touch  文件名		- 新建文件

cat 文件名   		- 查看文件内容

vim/vi  文件名          -打开文件



rm	文件名		- 删除文件(询问是否删除)

rm -f  文件名  - 强制删除文件(不询问)

rm - r 目录		- 删除文件夹

rm -rf   目录、 rm -r  -f 目录       -  删除文件夹(不询问)







cp  文件名1  文件名2	- 将文件1中的内容拷贝到文件2中

cp  文件  目录    -  将指定文件拷贝到指定目录中

cp -r  文件名/目录名   目录2	- 将文件/目录拷贝到目录2中



mv	文件名1  文件名2	- 将文件1中的内容移动到文件2中 ,并且删除文件1（文件重命名）

mv  文件1路径   文件2路径

mv 文件名1  新文件名    -   重命名





mv	文件名1  文件目录	- 将文件1移动到指定目录中  

注意: mv指令不能加-r来操作目录



(注意：cp/mv/rm 后面可以跟： -i询问  -f强制  -n不覆盖)



mkdir  目录名		- 新建文件夹

mkdir -p a/b/c		- 按层级创建a,b,c三个文件夹

mkdir -p a/{b,c}/{d,e,f}	-同一层级常见多个



rmdir  目录名		- 删除指定空目录





7.history		- 显示历史指令记录

bashrc 配置显示时间：export  HISTTIMEFORMAT="[%y‐%m‐%d_%T] " 

修改bashrc 后使其生效:  source ~/.bashrc  或 .  .bashrc   







6.链接

ln -s 源路径  目标路径		- 给源路径对应的文件在目标路径下创建一个软链接(可以看成是快捷键)(源路径是绝对路径) (掌握！)

ln 源路径  目标路径			- 给源路径对应的文件在目标路径下创建一个硬链接(看成一个数据的多个引用)（了解）



注意: 源文件不存在的时候，软件无效，硬链接变成普通文件





8.快捷键

ctr + f 		- 前进一个字符

ctr + b		- 后退一个字符

ctr + a		- 回到行首

ctr + e 		- 回到行尾

ctr + w		- 向左删除一个单词

ctr + u		- 向左删除全部

ctr + k		- 向右删除全部

ctr + y		- 粘贴上次删除的内容

ctr + l		- 清屏  



二、进程相关指令(用得较少)

1.ps指令

ps						- 进程状态

ps -aux  或者  ps ex			- 查看进程

ps -aux|grep 进程名		- 查看指定进程

ps grep  进程ID



[2.top](http://2.top)指令

top 						- 动态监控进程

top  -p PID1,PID2,….		- 动态监控指定进程



3.free指令

free -单位					- 以指定单位查看内存, 例如 free -m (以Mb为单位显示内存状况), -g,  -k等！



4.kill指令



kill 进程号					- 杀死指定的进程

kill -1/-9/-15 进程号		- -1(HUP)不间断重启，-9(KILL)强制杀死进程, -15(TERM)正常终止进程  

pkill  进程名				- 按名字处理进程

killall 进程名				- 处理名字匹配的进程



5.uptime					- 查看系统状态





三、权限管理

1.user和group : 一个系统可以有多个用户和多个分组； 一个分组中可以有多个用户，一个用户在不同的分组中(多对多)



users 									- 查看当前用户

groups 								- 查看当前分组



groupadd  分组名							- 添加分组   (能在/etc/group文件中查看到新的分组, root才有的权限)



useradd  用户名    							- 创建新的用户(还是在home中自动创建这个用户对应的文件夹， root才有的权限)

useradd ‐G 分组列表 ‐m ‐s /bin/bash 用户名		- 创建一个用户添加到指定的分组中(在home创建相应的文件夹)



usermod -G 分组列表 用户名					- 修改分组(root才有的权限)



passwd 用户名							- 修改密码（root才有权限）

passwd                                            - 修改当前账号密码





su  用户名								- 切换用户身份(root不需要密码，其他用户需要密码)





sudo										- 以管理员执行其他程序

注意： a.在ubuntu需要将用户添加到sudo分组中，才能使用sudo以管理员的身份执行程序

​          b.在centOS中需要先执行vi 指令进入/etc/sudoers文件中在指定的位置添加内容

​		## Allow root to run any commands anywhere

​		root    ALL=(ALL)       ALL

​		xiaoming ALL=(ALL)      ALL		(自己添加的，xiaoming是用户名)











2.chmod(记住！) 

chmod 	  权限值   文件			- 修改指定文件的权限



chmod    [a,u,g,o][+,-][r,w,x]  文件			- 为指定文件，给所有用户添加相应的权限

​								  			(a:所有，u:自己，g:同组，o:其他；

​											+：添加， -: 取消；

​											r:读，w:写，x:执行)

chown  用户名	 文件			- 改变文件所有者





[![file-mode.png](/Users/yuting/Library/Application Support/typora-user-images/17C12B13-6680-4C3A-8E21-C9C9250DEAE1/file-mode.png)](https://github.com/jackfrued/Python-100-Days/blob/master/Day31-35/res/file-mode.png)







(权限制是三组二进制值)

self      group    other

rwx      rwx        rwx

111       101		001            - 自己读写可执行，同一分组的只读可执行，其他的只可执行

110      100        000



chmod  644  文件

chmod  777   文件

chmod 666    文件





三、日志管理

1.cat指令

cat 	  文件				- 查看文件内容



2.查看部分

head -n  N  文件		- 查看前N行内容

tail  -n  N    文件 		- 查看后N行内容



3.

less  文件

​	- 按 j 向下

​	- 按 k 向上

​	- 按 f 向下翻屏

​	- 按	b 向上翻屏

​	- 按 g 到全文开头

​	- 按 G 到全文结尾

​	- 按 Q 退出  







more [-N]  文件    		- 和less差不多，这个是尽可能多，less是尽可能少的加载



4.处理(对通过其他指令获取的结果进行处理)

sort  				- 排序  (cat 文件 |sort)

uniq				- 去重  (cat 文件 |uniq) - 只会去重相邻的重复是数据，一般结合sort一起使用:  |sort|uniq

awk ‘{print $N}’	- 打印第N列的内容(netstat -natp|awk ‘{print $4}’)

awk ‘{print $N1,$N2,$N3,…}’







history |awk '{print $4}' |sort |uniq ‐c | sort ‐rnk 1 | head ‐n 3   		-获取历史指令中，使用最频繁的三个指令



uniq ‐c       -去重的时候统计每一行内容的重复出现的次数

sort -nk 1    - 数值大小从小到大排序

sort -nk 2   - 字符大小从小到大排序(默认)

sort -rnk 1    - 数值大小从大到小排序

sort -rnk 2   - 字符大小从大到小排序(默认)



5.重定向

执行获取数据的指令  > 文件  （将执行指定的结果存储到文件中 - 覆盖原文件中内容）

执行获取数据的指令 >> 文件   (将执行指定的结果存储到文件中 - 在原文件的最后追加)



5.统计  

wc -c(字符)/-w(单词)/-l(行)  文件









6.查找

grep  查看对象	目录/文件  参数

​	

​	参数：

​		-i	忽略大小写:         grep you bb.txt   -i

​		-n   显示行标号：      grep you bb.txt -n   /   grep you bb.txt -i -n

​		-E   通过正则表达式匹配:     grep -E  ‘正则表达式’  文件

​		注意： Linux中，正则不支持: \d, \s,\w,\b,\D,\S,\W,\B

​                                           支持：.   +, *, ?, {N,M}, [], ^, $





​		-v   忽略字段:   grep you bb.txt -v  (在bb.txt中找不包含you的所有行)



​						grep -E  '[0-9]+\.[0-9]+'  abb.txt  -v



​		-rn  递归查找目录，并打印行号

​		grep -r  you ./   (在当前文件夹下中所有文件中去找包行’you’的行)

​						



​		// 对文件格式进行约束

​		—include=‘*.py’	仅包含 py文件: grep -r you ./ --include=‘*.txt'



​		—exclude=‘*.js’	不包含 js 文件: grep -r you ./ --exclude='*.c'



​	例如：

​		grep you bb.txt  

​		grep you bb.txt -i

​		grep you bb.txt -i -n

​		grep -E '[0-9]+' bb.txt 







//  在文件夹下找满足条件的文件

find	   DIR	-name  ‘*.xxx’		找到目录下所有名字匹配的文件:  find a1 -name '*.txt’(在文件夹a1中找所有txt文件)



find 路径  -size  +/-文件大小      例如: find ./  +20k  (在当前目录下找文件大小大于20k的文件)





​	例：find ./ -size +20k -size -100k -name '*.txt'   (找当前目录下大于20k并且小于100k的所有txt文件)







// 查指令

which  指令		- 精确查找当前可执行的指令

whereis  指令	- 查找所有匹配的命令



man 指令   -使用指令手册









四、网络管理





ifconfig     查看网卡状态



netstat   -natp					- 查看网络连接状态

netstat   -natp|grep  端口号			- 查看指定端口的网络连接状态	



*ping  地址 

ping  -i   时间	地址

ping  -c  次数    地址



telnet  ip地址	端口		 - 查看远程主机网络连接状况（需要telnet环境）



dig 地址			- 查看DNS   (需要环境支持)



** wget  地址			- 下载  







五、使用包管理工具(掌握)

包管理工具：yum 

- yum search：搜索软件包，例如yum search nginx。
- yum list installed：列出已经安装的软件包，例如yum list installed | grep zlib。
- yum install：安装软件包，例如yum install nginx。
- yum remove：删除软件包，例如yum remove nginx。
- yum update：更新软件包，例如yum update可以更新所有软件包，而yum update tar只会更新tar。
- yum check-update：检查有哪些可以更新的软件包。
- yum info ：显示软件包的相关信息，例如yum info nginx。



源代码构建安装

1. wget  安装包的路径        -下载安装包
2. gunzip/tar  压缩包         - 解压、解归档
3. (设置安装路径)
4. cd 安装包目录 执行: make && make install       -编译安装包程序
5. 给可执行文件添加软连接到usr/bin目录下            -添加快捷方式





压缩/解压缩和归档/解归档 - **gzip** / **gunzip** / **xz** / **tar**

 



发送远程文件 - scp指令：

scp 文件   root@IP地址:服务器上保存被发送文件的路径