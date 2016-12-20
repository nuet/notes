nvm

注意 nvm install 6.2.2 不要带v不然不行

帮助: https://github.com/creationix/nvm/blob/master/README.markdown
1.
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.32.1/install.sh | bash
2.新建文件
touch ~/.bash_profile
3.下面内容放入.bash_profile 最底下
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh" # This loads nvm

避免每次用nvm use 设定版本
nvm alias default stable

用国内地址安装
NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node nvm install 4.4.7

nvm ls - 查看本地安装的版本
nvm ls-remote - 查看所有可以安装的版本
nvm use $version - 使用指定版本
nvm default $version - 指定默认版本
