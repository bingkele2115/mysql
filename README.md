# mysql
方法一：
MySQL提供跳过访问控制的命令行参数，通过在命令行以此命令启动MySQL服务器：
safe_mysqld --skip-grant-tables&
即可跳过MySQL的访问控制，任何人都可以在控制台以管理员的身份进入MySQL数据库。
需要注意的是在修改完密码以后要把MySQL服务器停掉重新启动才会生效
方法二：
可以进行如下的步骤重新设置MySQL的root密码：
1．首先确认服务器出于安全的状态，也就是没有人能够任意地连接MySQL数据库。
因为在重新设置MySQL的root密码的期间，MySQL数据库完全出于没有密码保护的
状态下，其他的用户也可以任意地登录和修改MySQL的信息。可以采用将MySQL对
外的端口封闭，并且停止Apache以及所有的用户进程的方法实现服务器的准安全
状态。最安全的状态是到服务器的Console上面操作，并且拔掉网线。
