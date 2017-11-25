
[react-app-rewired]
(https://github.com/timarney/react-app-rewired)(不想eject可以用此方案)

[create-react-app慢的解决方法]
(http://blog.csdn.net/eagyne/article/details/53780653)(方案是用淘宝代理)

[修改create-react-app支持多入口]
(http://imshuai.com/create-react-app-multiple-entry-points/)

[基于create-react-app的打包后文件路径问题]
(https://segmentfault.com/q/1010000009672497)(相对路径配置)

```shell
// create-react-app 安装eslint不eject好像不行
npm run eject

npm install -g install-peerdeps
install-peerdeps --dev eslint-config-airbnb
[参考](https://www.npmjs.com/package/eslint-config-airbnb)

```
