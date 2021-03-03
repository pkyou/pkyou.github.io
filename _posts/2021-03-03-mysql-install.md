# Install 

`brew install mysql`



result:

```
We've installed your MySQL database without a root password. To secure it run:
    mysql_secure_installation

MySQL is configured to only allow connections from localhost by default

To connect run:
    mysql -uroot

To have launchd start mysql now and restart at login:
  brew services start mysql
  brew services stop mysql
Or, if you don't want/need a background service you can just run:
  mysql.server start
  mysql.server stop
```

```
==> Summary
🍺  /usr/local/Cellar/mysql/8.0.23_1: 298 files, 293.1MB
==> Caveats
==> protobuf
Emacs Lisp files have been installed to:
  /usr/local/share/emacs/site-lisp/protobuf
```

## mysql_secure_installation
mysql_secure_installation

Securing the MySQL server deployment.

Connecting to MySQL using a blank password.

VALIDATE PASSWORD COMPONENT can be used to test passwords
and improve security. It checks the strength of password
and allows the users to set only those passwords which are
secure enough. Would you like to setup VALIDATE PASSWORD component?

Press y|Y for Yes, any other key for No:

## Ordors

```
mysql -u root -p  输入密码。
show databases;所有数据库列表
use mysql切换数据库
show tables; 所有表列表
describe user; 表结构 
show global variables like 'port'; 端口号
```