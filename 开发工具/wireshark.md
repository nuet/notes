
参考 https://wiki.wireshark.org/CaptureFilters


过滤目标地址
ip.dst==192.168.101.8
过滤源地址
ip.src==1.1.1.1

过滤目标端口
tcp.port==80

过滤源端口
tcp.srcport==80

过滤协议
http

如过滤get包
http.request.method=="GET"

过滤post包
http.request.method=="POST"

ip.src==192.168.101.8 and http

http.host==z-stg2.pa18.com
http.host contains pa18.com


host z-stg2.pa18.com
