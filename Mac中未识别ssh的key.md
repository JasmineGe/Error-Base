场景：Mac中.ssh文件中替换了公钥与私钥之后，`git pull`时仍然显示没有权限

解决办法：`ssh-add id_rsa`

作用：把指定的私钥添加到ssh-agent所管理的一个session当中, id_rsa是私钥的文件名

可能出现如下error：
>@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0644 for 'id_rsa' are too open.
It is required that your private key files are NOT accessible by others.
This private key will be ignored.

解决办法：`chmod 400 id_rsa`，显示如下即表示设置成功

>Identity added: id_rsa (id_rsa)

## chmod语法 ##

chmod [对谁操作][操作符][赋予的权限]文件名

操作对象
* u 用户user，文件或目录的所有者
* g 用户组group，文件或目录所属的用户组
* o 其他用户other
* a 所有用户all

操作符
* 添加权限 +
* 减少权限 -
* 直接给定一个权限 =

权限
* r(二进制100  十进制4)
* w(二进制010  十进制2)
* x(二进制001  十进制1)

<font color=#FF6347 size=3>chmod可以用数字来表示权限</font>

例如：`chmod 400 id_rsa`中的400，分别表示User、Group及Other的权限

`chmod 400 id_rsa`可改写为`chmod u=r id_rsa`

`chmod 777 id_rsa`可改写为`chmod ugo=rwx id_rsa`或者`chmod a=rwx id_rsa`