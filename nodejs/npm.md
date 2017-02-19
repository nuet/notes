npm 命令记录

npm install update

查看第一级包
npm ls --depth=0
    后面带了extraneous  卸载掉就好了
    项目的package.json中没有添加报extraneous错误的模块信息

npm i <name>@<tag>   安装指定版

npm i <name>@latest  安装最新版

npm i －force 强制拉取远程资源

npm outdated 检查包是否已经过时

npm view module name engines 查看包依赖的node版本

npm upgrade -g npm  升级NPM,有些兼容性可以通过升级解决

npm uninstall gulp
npm install gulp

安装cnpm
 npm install -g cnpm --registry=https://registry.npm.taobao.org

// 查看某个包的版本, 可以看服务器上的
npm show extract-text-webpack-plugin versions
