# MySQL
mysql安装
#### 1.官网下载MySQL
#### 2.配置初始化文件my.ini
#### 3.初始化MySQL
#### 4.安装mysql服务并启动+修改密码
#### 5.配置环境变量
#### 6.mysql 连接 Navicat


## 1. 官网下载MySQL

官网地址：https://dev.mysql.com/downloads/

选择"MySQL Community Server"下载

![image](https://user-images.githubusercontent.com/63994835/159439974-a7305c6a-f17c-4e68-9fd1-9aae8be26b71.png)

----------------------------

![image](https://user-images.githubusercontent.com/63994835/159440007-9c288ad6-3cf4-4ba5-92e1-9bf51b321068.png)

----------------------------

![image](https://user-images.githubusercontent.com/63994835/159440085-e8f0f665-5868-4b30-b474-02a8b2c4c379.png)

**下载完成后，将解压后的文件夹放到某一个文件夹，我放在D盘中（记住存放路径，后面需要用到！！）**


## 2. 配置初始化文件my.ini

在根目录下新建一个my.ini的文件，（新解压的文件没有my.ini文件，需自行创建）

![image](https://user-images.githubusercontent.com/63994835/159443554-4cc822e1-4b31-4ed6-8b4b-b59b8d974d52.png)

之后复制下面这个代码放在文件下，以下代码除安装目录和数据的存放目录（改成你刚才解压后的文件存放的位置）需修改，其余不用修改

[mysqld]
# 设置3306端口
port=3306
# 设置mysql的安装目录   ----------是你的文件路径-------------
basedir=D:\mysql\mysql-8.0.28-winx64
# 设置mysql数据库的数据的存放目录  ---------是你的文件路径data文件夹自行创建
datadir=D:\mysql\mysql-8.0.28-winx64\data
# 允许最大连接数
max_connections=200
# 允许连接失败的次数。
max_connect_errors=10
# 服务端使用的字符集默认为utf8mb4
character-set-server=utf8mb4
# 创建新表时将使用的默认存储引擎
default-storage-engine=INNODB
# 默认使用“mysql_native_password”插件认证
#mysql_native_password
default_authentication_plugin=mysql_native_password
[mysql]
# 设置mysql客户端默认字符集
default-character-set=utf8mb4
[client]
# 设置mysql客户端连接服务端时默认使用的端口
port=3306
default-character-set=utf8mb4

## 3.初始化MySQL

按住 win+r 键, 输入cmd, 进入终端界面

![image](https://user-images.githubusercontent.com/63994835/159444055-898677cd-542b-4767-9f87-53b3125e0848.png)

----------------------------

输入 cd D:\mysql\mysql-8.0.28-winx64\bin 进入bin目录，

![image](https://user-images.githubusercontent.com/63994835/159452830-530db3e8-4af0-4715-89cd-d01434b91bb9.png)

----------------------------

输入命令： mysqld --initialize --console

![image](https://user-images.githubusercontent.com/63994835/159453083-69402062-9d7d-44e5-acbd-7a03fdb4188f.png)

----------------------------

复制最后一行root@localhost后的密码，这个密码是进入数据库的初始密码（一定要保存好！）P!tk(6+;#Ol#

![image](https://user-images.githubusercontent.com/63994835/159453226-8d6fa9ad-794c-4866-94e1-88f47b2c1416.png)

## 4.安装mysql服务并启动+修改密码

安装mysql服务，输入命令：mysqld --install mysql

![image](https://user-images.githubusercontent.com/63994835/159453410-79c1ae5d-d595-437b-860b-4aa2a1ca1c02.png)

----------------------------

启动mysql服务，输入命令：net start mysql

![image](https://user-images.githubusercontent.com/63994835/159454058-0f4a4195-540c-45f0-a94c-2e93ab6e3678.png)

----------------------------

若启动mysql服务器失败，显示：'net’ 不是内部命令或外部命令，也不是可运行的程序或批处理文件，解决方案如下：

我的电脑-->属性-->高级-->环境变量 Path的变量值新加: %SystemRoot%\system32（以“；”隔开即可）

----------------------------

开始连接mysql, 输入命令：mysql -uroot -p

![image](https://user-images.githubusercontent.com/63994835/159454612-ceb1b030-a5f2-4aeb-a4d0-5f4f1b7cb07e.png)

----------------------------

输入刚才保存的密码，密码不会显示，大家输入后直接点击回车即可

![image](https://user-images.githubusercontent.com/63994835/159454698-b2610e33-8d9f-4f74-9ccf-72fca7dd9507.png)


