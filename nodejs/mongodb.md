

下载mongodb 这个网址找地址  https://www.mongodb.com/download-center#community
curl https://fastdl.mongodb.org/osx/mongodb-osx-ssl-x86_64-3.2.7.tgz > mongodb3.2.7.tgz

tar -zxvf mongodb-osx-x86_64-2.4.6   解压

mv -n ~/Downloads/mongodb-osx-x86_64-2.4.6 ~/Applications/mongodb/  移动到想要的目录


sudo mkdir -p /data/db   创建目录

sudo chown -R  你电脑用户名 /data  设定权限

cd Applications/mongodb/bin
./mongod        启动mongoldb服务

Applications/mongodb/bin
./mongo     启动客户端

用配置文件启动
mongo —config ~/github/mongod.ncms.conf



