

参考: http://my.oschina.net/bianweiall/blog/369655
能运行成功2016/2/19
3. cordova安装

cnpm install -g cordova

创建应用:
教程API:http://cordova.apache.org/docs/zh/edge/guide_cli_index.md.html
cd E:\Program Files\html\cordova
cordova create hello com.example.hello HelloWorld

添加平台:
cd hello
cordova platform add android

构建:
cordova build android

模拟器测试：
cordova emulate android

手机测试：
cordova run android
