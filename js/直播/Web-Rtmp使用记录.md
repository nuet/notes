
git clone https://github.com/yingDev/Web-Rtmp.git
cd Web-Rtmp
git submodule update --init --recursive
npm install
npm install webpack@2.2.1 -D

修改./Web-Retmp/test.js 修改成如下行
var player = new WebRtmpPlayer('ws://127.0.0.1:1999', 'live', 'BXlYmS28E8', 'rtmp://test.my.com/live');

node_modules/.bin/webpack --config ./webpack.config.js

命令行执行
./websockify/websockify.py 1999 test.my.com:1935

复制index.template.html一个index.html去掉一个模板参数

运行index.html就可以看到视频了
