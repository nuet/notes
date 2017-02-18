
[使用 Charles 获取 https 的数据]
(http://blog.csdn.net/yangmeng13930719363/article/details/51645435)


[【iOS秘籍】-下载历史版本App超详细教程]
(http://www.jianshu.com/p/edfed1b1822c)(有讲解Charles抓https包配置M)
1. 菜单help->SSL Proxying->Install Charles Root Certificate->
如果没成功则->Save Charles Root Certificate->保存格式选择Binary Certificate(.cer)->
双击下载的证书->安装->双击安装好的证书->始终信任证书
2. Charles->选择Structure->右键有锁图标的https项->Enable SSL Proxying->再次访问https链接->
如果锁没有了说明可以解析了


这个快乐平安抓不了包试试
https://github.com/levyitay/AddSecurityExceptionAndroid

如果某些包抓不了, 比如快乐平安登录验证的心跳包
可以选择->"Disable SSL Proxying"  这样就能顺利的抓其他包
