
[spy-debugger]
(https://github.com/wuchangming/spy-debugger)
(微信调试，各种WebView样式调试)(可以尝试调试APP里的网页看看)

## 用chrome调试ios
[使用Chrome DevTool调试iOS设备的webView]
(http://www.jianshu.com/p/19c18c924f91)
[github]
(https://github.com/google/ios-webkit-debug-proxy)
```sh
以下命令行执行  用chrome调试ios
brew update
brew reinstall --HEAD libimobiledevice
brew reinstall -s ios-webkit-debug-proxy
ios_webkit_debug_proxy -f chrome-devtools://devtools/bundled/inspector.html
浏览器执行
http://localhost:9222/  
或者 http://localhost:9221/  
如果没有出来， 邮件url复制链接地址， 新标签打开url可以调试了
```
