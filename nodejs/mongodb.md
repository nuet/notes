
[官网安装教程]
(https://docs.mongodb.com/manual/tutorial/install-mongodb-on-os-x/#install-mongodb-community-edition-manually)

curl -O https://fastdl.mongodb.org/osx/mongodb-osx-x86_64-3.2.10.tgz  下载
tar -zxvf mongodb-osx-x86_64-3.2.10.tgz  解压
mkdir -p mongodb   新建目录
cp -R -n mongodb-osx-x86_64-3.2.10/ mongodb  复制

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

启动mongodb服务 mac(解压了就可以直接使用 dbpath指定数据存储的位置)
sudo ~/db/mongodb3.2.7/bin/mongod --dbpath ~/db/data/ncms
