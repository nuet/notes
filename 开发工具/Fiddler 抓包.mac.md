Fiddler 抓包

手机和笔记本要在同一个wifi里
mac 系统内装windows10虚拟机
虚拟机上网方式使用桥接， 选择默认适配器
win10里装fiddler
虚拟机开代理按下面链接
www.cnblogs.com/mcho/p/3983053.html
  1. fiddler options->https->create https connects(勾)->
      decrypt HTTPS traffic(勾)->Ignore server certificate errors(勾)
  2. fiddler options->Extensions->Allow remote computers to connect(勾)
手机也按上面网址
手机在pa_wlan_ma上设置代理服务器10.180.145.88:8888(这个事win10的虚拟机ip)
我安装时mac系统的ip地址是10.180.145.52这个没用，
注意， 我是win10系统重启了一次， 代理才成功， 可能要重启

mac主机也能用这个做代理上网, 但是baidu没抓成功， 其他有些网站可以
虚拟机用的parallels desktop
