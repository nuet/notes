
将文件拉到本地
svn checkout path(服务器上的目录) --username=mj --password=123

svn add filename
svn add *.js
svn add *

svn commit -m 提交消息

同步服务器上的文件
svn update
svn update filename


linux/mac svn 切换用记
1. 临时切换
在所有命令下强制加上--username 和--password选项。
例如：svn up --username zhangsan --password 123456
2.永久切换(这个要在finder里才看得到)
删除目录 ~/.subversion/auth/  下的所有文件。下一次操作svn时会提示你重新输入用户名和密码的。换成你想用的就可以了。然后系统默认会记录下来的。
