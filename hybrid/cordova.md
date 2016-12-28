
参考
http://www.hangge.com/blog/cache/detail_1145.html
[Swift - 在现有的项目中添加Cordova支持1（添加Cordova核心库]
(http://www.hangge.com/blog/cache/detail_1155.html)
[iOS WebViews]
(https://cordova.apache.org/docs/en/latest/guide/platforms/ios/webview.html)

安装
sudo npm install -g cordova

更新
sudo npm update cordova -g

cordova更新完成后，还需要更新项目（比如更新ios项目）：
cordova platform update ios     这步好像出错

测试下Cordova是否安装成功
cordova -v

创建项目
cordova create hybrid com.ogoodo.hybrid HelloWorld
cd hybrid
cordova platform add ios  添加iOS平台文件
