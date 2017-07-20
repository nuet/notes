
[官方文档]
(http://cordova.apache.org/docs/en/latest/guide/cli/index.html)

安装
sudo npm install -g cordova

更新
sudo npm update cordova -g

创建项目
cordova create MyH5App

增加ios平台
cd MyH5App
cordova platform add ios
cordova platform add android

构建android:
cordova build android
构建ios:
cordova build ios
  项目目录下，有个platforms文件夹，找到对应的平台，打开项目，运行。

模拟器测试：
cordova emulate android

手机测试：
cordova run android


[打包ios]
(http://www.tuicool.com/articles/numEBrM)
