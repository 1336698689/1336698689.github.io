47.97.91.151
---------------------------------day1--------------------------------
����[����][���ö���]
1��who��who am i����w       -    �鿴˭���ӷ�����
2��last      -           ���һ��ʱ���������¼��¼
3��clear     -     ����
4��date     -     �鿴��ǰʱ��
5��cal    cal -3 1 2019(�鿴2019��1�·�ǰ��1���£���3����)   -      �鿴����
6��[����]--help    -   �鿴�������
7��man [����]      -   �鿴�����ֲ�
8��wget https://www.sohu.com/index.html       -   ����(url)
9��cat     -    �鿴�ļ�
10�� ctrl+c   ctrl+d     -   ��ֹ���    ϵͳ
11�����¼�ͷ�����Ե�����ǰ����
12��ctrl+a   j   ctrl+e     -     ����Ƶ����ף��ƶ�����β
13��ctrl+w     ctrl+u   -    ɾ��һ������/ɾ������
14��init  6   0    -     ��ʼ��  ����6    �ػ�0
15��shutdown   -c  -r    -h   -    �ػ����رշ�����֮ǰ��ʾ��Ϣ�� ȡ��-c�ػ���  ����-r   ��Сʱ�ػ�-h
16��write[]  wall     -   ��[]ָ���û�������ʷϢ���������˷���Ϣ
17��history     -c -     �鿴��ʷ��������ʷ����
18����+��ʷ������    -     �ظ�������
-------------------------------------------------��Ҫ����
19��clear   /   history      ����/��ʷ ����
20��pwd     -  print working directory     -   ��ӡ����Ŀ¼ 
21��ls   -a  -l   -R  -    �鿴�ļ�    �鿴�����ļ�-a  ����ʽ��ϸ��Ϣ-l  �ݹ�ʽ�鿴-R
22��cd    -     �л��ļ���
23��mkdir []  -p abc/ab/c  -    �����ļ���   �����༶�ļ���  -p
24��rmdir []    -   ɾ�����ļ���
25��touch    -   �������ļ����޸�������ʱ��    
26��rm     -remove    -   ɾ���ļ����ļ���
27��rm   -rf       -  ɾ�����е��ļ��������ļ�/�ļ���   -fǿ��ɾ��  -r�ݹ�ɾ��
28��cp  [��ǰ�ļ�������·����+�ļ���] [���ļ���ַ]    -    �����ļ�
29��mv    -   �ƶ��ļ������У�������ǰ�ļ�������
30��cat/tac/headr/tail            -  ˳��鿴�ļ�/����鿴/��ͷ��/��β��
31��more/less                     -     ��ҳ�鿴
32��iconv -f gb2312 -t utf-8  qq.html   -     ���ļ��ı���ת����utf-8
33��gunzip  [�ļ���.tgz .gz]  gzip[]  -    ��ѹ���ļ�tgz/gzΪ.tar��ʽ��ѹ���ļ�
34��xz -d[�ļ���.xz]  -z     -       ��ѹ���ļ�xzΪ.tar��ʽ�� ѹ���ļ�
35��tar -xvf[�ļ���.tar]     -    ��鵵.tar���ļ�Ϊ����ļ�

-------------------------------day2--------------------------
useradd [����]         -      �����û�
passwd [����]          -      ��������
su root  |  su wangdachui     -   �л�Ϊ��������Ա|�л�������     
wget    -    ����������Դ�ļ�
---------------------------------------------vim
vim .vimrc           -     ����vim��ʽ����
imap <F3> if __name__=='main':    -   ���ÿ�ݼ�
vim -d a.txt b.txt   -   ��2���ļ�������ͬ
vim a.txt b.txt   -> ĩ�У�sp  vs   ��2���ļ��л�����������
                         ->   ctrl + w  �л����� 
����ģʽ��
�ƶ���꣺ -h j k l(��������)          -0 $ w      -gg/G/ <num>Gͷ/β/ָ������
                ctrl+e /ctrl+y  /ctrl+f  /ctrl+b 
�༭���ݣ�
dd  -  ɾ������
u/ctrl+r    -  ����/����
d0/d$     -   ��ͷ�����λ��ɾ��/�ӹ�굽βɾ��
dw     -      ɾ��һ������
�����˳���
ZZ 
ĩ��ģʽ:(������ģʽ�°�ð��)
	set nu   -    ��ʾ�к�
                syntax on/off -  ��������ģʽ
	set ts=4   -   �����ַ���Ϊ4���ո�
	q!/wq    -     �������˳�/�����˳�
�༭ģʽ��������ģʽ�°�i����a��

vim .vimrc  -  ����vim��̨����
set nu    -�����к�
set ts=4   -��������Ϊ4�ո�  set tabstop=4
set autoindent   -�����Զ�����
set expandtab    
set ruler   -�������λ����ʾ
set nohls    -�ر�ƥ��ĸ�����ʾ
syntax on    -��������

-----------------------------------------CentOS��װ���
web������    ->   ǰ��ҳ��ŵ���������  -apache / nginx / iis
CentOS��װ�����
1.�������߰�װ���򵥿��ף�
  -yum:  yellowdog updater modified
  	 -yum search <���������>        -    ����
 	 - yum install <���������>        -  ��װ
 	 - yum upgrade<���������>    -  ����
 	 - yum erase<���������>         -  �Ƴ�/ɾ��
	 - yum info<���������>            -   ����
	- yum list installed | grep <����>  -  ����ָ����װ�İ�
 systemctl start nginx    ��web������������

  -apt / apt-get

  -rpm
        rpm -ivh [�ļ�]      -   ��װ�ļ�
        rpm -e ����         - ɾ��
        rpm -qa | grep  ����    - ��ѯ
2.Դ���빹����װ
gcc  --version  /  make --version
/����/��ѹ��/��鵵/����������/��װǰ����/make && make install/���û�������

3.���غ�ϵͳ��Ӧ�Ķ������ļ�
	����PATH��������

��װPython3.x
1.����Դ����
wget https://
2.��ѹ����鵵
gunzip Python-3.7.4.tgz
tar -xvf Python-3.7.4.tar
cd Python-3.7.4
3.����Python���������
yum -y install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel libdb4-devel libpcap-devel xz-devel libffi-devel
4.��װǰ������
./configure --prefix=/usr/local/python37 --enable-optimizations
5.�����Ͱ�װ
make && make install
6.����PATH��������
vim .bash_profile
export PATH=$PATH:/usr/local/python37/bin
7.���µ�¼����ͨ����������������������
source .bash_profile

#!/usr/local/python37/bin/python3   -   �����Զ��ұ�����
chmod u+x,g+x,o+x [py�ļ�]             -    ���ִ��Ȩ��   
./[py�ļ�]         -           ִ���ļ�

----------------------------------------day3-----------------------------------
�������ݣ���װ�ǹ�ϵ�����ݿ�redis  ��װGit  ��װMySQL���ݿ� 
service mysqld start  - �������ݿ�
service mysqld stop  - �ر����ݿ�

systemctl start mariadb   -   �������ݿ�
systemctl top mariadb    -   �ر����ݿ�
systemctl restart mysqld  -  �������ݿ�
systemctl status mysqld   -  ���ݿ�״̬
systemctl enable mysqld  -  ��������
systemctl disable mysqld  -  �رտ�������

create user 'root'@'112.23.255.5' identified by '123456';  -  ����IP����
create user 'root'@'%' identified by '123456';   -   ���������˶���������
grant all privileges on *.* to 'root'@'%'      -     ����root�˺�����Ȩ��
grant all privileges on *.* to 'root'@'%' with grant option;     -  ����root�û�����Ȩ��,���ҿ��Ը������û���Ȩ
revoke all privileges on *.* from 'root'@'%';   -    �ջ�root�û���Ȩ��
grant insert on school.* to 'root'@'%';    -    ����root�û����Բ���school���ݿ����������
cat /var/log/mysqld.log | grep password    -   ��ѯ��ʼ����
set global validate_password_policy = 0;    -   ����Ϊ������
set global validate_password_length = 6;   -   ����Ϊ6λ������
alter user 'root'@'localhost' identified by '123456';   -  ��������

ps -ef    -  �鿴��ǰ���еĽ���
ps -ef | grep maria   -  ģ����ѯ���ݿ�
netstat -ntlp     -    �鿴ʹ�ö˿�      t-tcp  l-����  p-��������
killra -9     -   �رս���  -9Ϊǿ�йر�

yum search mariadb    -�鿴���ݿ�
yum install -y mariadb-server mariadb   -��װ���ݿ⣬ȫ���ǣ�-y��
yum info mariadb    -    �鿴����
yum upgrade mariadb    -    ������
yum erase mariadb mariadb-server   -  ж��
yum list installed | grep mariadb | awk '{print $1}' | xargs yum erase -y   -   ��ʦӦ��ж��
yum list installed | grep mariadb    -   �鿴��װ�б� ,�鿴ָ���ļ�

&& ��һ���ɹ�����ִ�еڶ���     || ��һ��û�ɹ���ִ�еڶ���   ��һ��ִ��

Դ���빹����װGit      
����ע�⣺  nohup wget  [��ַ] > download.log &  -  ���������жϾͼ����ں�̨�¡�&��̨����
ps  -ef  / jobs  -�鿴����
1. wget https://mirrors.edge.kernel.org/pub/software/scm/git/git-2.23.0.tar.gz   -  ����
2.gunzip git-2.23.0.tar.gz   -  ��ѹ
tar -xvf git-2.23.0.tar         -  ��ѹ�鵵
cd git-2.23.0                       -  �����ļ���
3. yum install -y libcurl-devel   -  ��װһ���������а�
4. ./configure --prefix=/usr/local  - ��װǰ������
5.make && make install    - �����Ͱ�װ
6.git --version         -   �鿴�汾

---------------------------------��ʦ���롾CentOS��װ�����
CentOS��װ�����
1. �������߰�װ���򵥿��ף�
	- yum��yellowdog updater modified
		- yum search <���������>
		- yum install <���������>
		- yum upgrade <���������>
		- yum erase <���������>
		- yum info <���������>
		- yum list installed | grep <����>
	- apt / apt-get
	- rpm��red-hat package manager
		- rpm -ivh RPM�ļ�
		- rpm -e ����
		- rpm -qa | grep ����
2. Դ���빹����װ
	- gcc --version / make --version
	- ���� / ��ѹ�� / ��鵵 / [����������] / [��װǰ����] / make && make install / [���û�������]
3. ���غ�ϵͳ��Ӧ�Ķ������ļ�
	- ����PATH��������

ln -s /usr/local/python37/bin/python3 /root/python  - ������
ln /usr/local/python37/bin/python3 /root/python      -  Ӳ����

----------------------------------------day4-----------------------------------
github.com   -   �����й�ƽ̨   -  Git������   -  ���������
gitee.com   -  ����  -  Git������    -   �й���������ѧϰʹ�ã�
�汾���ƣ�������ƹ��� -  Git
CVS/VSS����ģʽ -> SVN�ϲ�ģʽ������Ҫ�а汾���Ʒ������� ->Git�ϲ�ģʽ���ֲ�ʽ�汾����ϵͳ��
git init   -   ���ļ��б�ɰ汾���Ʋֿ�
git status   -   �鿴�汾����״̬
git add []  -     ����ļ����ֿ⻺����
git rm --cached []  -  ���ļ��Ӳֿ⻺������ȡ����������
git restore --staged[]  -  ���ļ��Ӳֿ⻺������ȡ����������
git config --global user.name "Mr Tao"
git config --global user.email "133..@qq.com"
git commit -m '�ύԭ��'   -   ���ֿ⻺�������ļ��ϴ����汾����
git reset --hard head^   --hard [�汾��]   -    �������ָ�����һ���汾/�ظ����汾���Ǹ��汾
git relog   -  �鿴��ɾ��־
git log  -   �鿴�ύ��־
git restore[]  -    ��ɾ�����ļ��ظ������ư汾
-----------------------------------------��֧����
git branch -a   -    �鿴���еķ�֧
git branch work  -   ������֧
git branch -b work   -  �����л���work
git checkout    -     �л���֧
git branch -d work   -   ɾ����֧
git merge []           -    �ϲ���֧
git diff  -    �鿴��֧��¼
-----------------------------------------����
git remote add origin https://gitee.com/tao_chao/tao_chao.git    -   �������Ʋֿ� 
git remove origin     -      ɾ��Զ�˲ֿ� 
git push -u origin master       -    ��master��֧�ϴ����ҵ����Ʋֿ�
git pull origin master        -    �����Ʋֿ���µ����ݸ��µ�����

git clone [Զ�˲ֿ��url]    -     ��Զ�˷������Ĳֿ��¡������

ssh-keygen -t rsa -b 2048 -C "1336698689@qq.com"    -    ��������
cat id_rsa.pub   -   ��������
���ssh��Կ  ->  ����ssh����   -> �л���.sshĿ¼  -> git clone ssh_url  ����֤�� yes




------------------------------------------------��ʦ����
�汾���ƣ�������ƹ���
1990s - CVS / VSS - ����ģʽ
2000 - Subversion��SVN��- �ϲ�ģʽ - ���뼯Ȩ�Ͱ汾����ϵͳ - ����Ҫ�а汾���Ʒ�����
BitKeeper
2005 - Git - �ϲ�ģʽ - �ֲ�ʽ�汾����ϵͳ 

1. ��ʼ���汾�ֿ�
git init
2. �鿴״̬
git status
3. ���ļ��ŵ����������ݴ�����
git add <filename>
git add .
4. ���ļ��Ƴ�������
git rm --cached <filename>
5. �û������ָ�������
git restore --staged <filename>
6. �������������ύ���ֿ�
git config --global user.name "�û���"
git config --global user.email "����"
git commit -m '�ύ��־(ԭ��)'
7. �鿴�ύ��־
git log
git reflog
8. ���˰汾
git reset --hard HEAD^
git reset --hard �汾����

---------------------------------------------day5-----------------------------------
���� &  - �ѽ��̣�����ӵ���̨����
jobs  -   �鿴��̨������ͣ/����/����ɣ�
fg %<num>  -   ����̨��������ǰ̨����
bg %<num> -   �������ں�̨����
Ctrl+z     -          ��ǰ̨������ͣ�ŵ���̨

ps -ef / ps -aux
pgrep - ���ݽ�������������

wget   -   �����ļ�
ifconfig  -   �鿴������Ϣ
ip     -     ��ȡ��������صĸ�����Ϣ
netstat -na    -   ����״̬
	-t/-u/-a  �鿴Э��
	-l      
	-n     -ip��ַ
	-p     -����

sftp   -   ��ȫ�ļ�����
sftp root@1.2.3.4
sftp>   ls cd get(����) 
            put(�ϴ�) 
            bye

Զ�̰�ȫ�ļ�����
scp Դ�ļ� Ŀ���ļ�
scp hell.txt root@120.77.222.217:/root/abc.text

cp [] []


-------------------------------------pycharm
�����������嵥
pip freeze > requirements.txt
�����������嵥��װ�����⣺
pip install -r requirements.txt -i https://pypi.doubanio.com/simple
������汾���Ƶ��ļ����ļ��е��嵥  ->  .gitignore

--------------------------------------��װhexo
yum install -y nodejs     -   ��װnode.js
npm install -g hexo-cli     -   ��װhexo�����й���
hexo init blog      -     ��ʼ��������Ŀ
cd blog               -   ����blog�ļ�
npm install          -    ��װ��Ŀ������
hexo g               -    ͨ��markdown�ļ����ɣ�generate)ҳ��
systemctl stop nginx   -  ֹͣnginx 80�˿�
hexo s -p 80               ������������server)���в�����Ŀ


�ܽ᣺
��һ�죺FinalShell��װ������ʹ�ã�
�ڶ��죺1��vim�Ĳ���ʹ�ã� 2����������:yum-rpm-wget;3����װpythono3.0����
�����죺1����װ�ǹ�ϵ�����ݿ�redis �� 2����װGit ��3�� ��װMySQL���ݿ�
�����죺1��git����������2������git�ϴ����Ʒ�����������
�����죺1��ʣ��FinalShell�Ĳ������⣻2��pycharm��װ����¡GIT��������3����װʹ��hexo�������

---------------------------------day6--------------------------------
---------------------------------shell�ű�ʹ��
printf      - ����
read ������      -�ȴ�����
alias         -  ����
unalias     -ȡ������   
vim /etc/bashrc    -   42�и���
vim .bash_profile   -   ���õ�¼��ӭ
bash a.sh            - ִ��.sh�ű��� ��
chmod 755 a.sh   -��Ȩ��       
	./a.sh    -ִ��.sh�ű�����
----------------------------------at�ƻ���ʹ��
at 14:00+3days     -   ԤԼ3�������2��Ҫ������
	at rm -f /root/a.sh   - ��ʱ��ɾ��root�����a.sh
atq        -     �鿴ԤԼ����Ķ���
strm[���]     -     ȡ��ԤԼ[���]
----------------------------------crontab��ʱ����ִ��
crontab -e      -  ������ʱ����
	* * * * *       �� ʱ �� �� ����
	59 23 * * *

----------------------------------------���ݿ�
��ϵ�����ݿ⣺ Oracle / DB2 / MySQL / Sybase / SQLServer / SQLite / postgreSQL
������ԣ�SQL  -  �ṹ����ѯ����
	-DDL   - ���ݶ�������       create / drop / alter
	-DML  - ���ݲ�������        inster / delete / update / select    -CRUD
	-DCL   - ���ݿ�������        grant / revoke
�ǹ�ϵ�����ݿ⣺MongoDB / Redis / ElasticSearch

----------------------------------------mysql
systemctl start mysqld   -  ����mysql
netstat -ntlp  -   �鿴�˿�  netstat -ntlp | grep mysqlc
 create database school default charset utf8;   -  �������ݿ�
alter table tb_student add constraint pk_student_stuid primary key (stuid);
drop table tb_student;
insert into tb_student values (1001,'����',1,'1992-2-2','�Ĵ��ɶ�');
insert into tb_student(stuid,stuname) values (1002,'¶��˹');

SQLyog Community  (����)

-------------------------------------------------��ʦ����
���ݿ� - ���ݵļ�ɢ�أ��ֿ⣩- database
��ϵ�����ݿ� - 1970s 
Oracle / DB2 / MySQL / Sybase / SQLServer / SQLite / PostgreSQL

���ۻ�������ϵ���� + ������
���������ʽ���ö�ά������������
	- �У���¼��record��
	- �У��ֶΣ�field��- �����У�primary key��
������ԣ�SQL - �ṹ����ѯ����
	- DDL - ���ݶ������� - create / drop / alter
	- DML - ���ݲ������� - insert / delete / update / select - CRUD
	- DCL - ���ݿ������� - grant / revoke

rpm�������߰�װMySQL
rpm -ivh mysql-community-common-xxx.rpm
rpm -ivh mysql-community-libs-xxx.rpm
rpm -ivh mysql-community-client-xxx.rpm
rpm -ivh mysql-community-server-xxx.rpm

systemctl start mysqld
journalctl -xe / systemctl status mysqld
netstat -ntlp | grep mysql

mysql [-h ����IP��ַ] -u �û��� -p

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

insert into tb_student values (1001, '����', 1, '1992-2-2', '�Ĵ��ɶ�'); 
insert into tb_student (stuid, stuname) values (1002, '��Ԫ��');
insert into tb_student (stuid, stuname, stusex) values 
(1004, '�׽�', 0),
(1005, '������', 0),
(1006, '����', 1);

�ǹ�ϵ�����ݿ� - 1998 - NoSQL
MongoDB / Redis / ElasticSearch
No SQL
No, SQL
Not Only SQL 









