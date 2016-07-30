

https://segmentfault.com/a/1190000005126759



# Install the `electron` command globally
npm install electron-prebuilt -g

# Install as a development dependency
npm install electron-prebuilt --save-dev

运行
./node_modules/.bin/electron .

asar打包压缩源码
npm install -g asar

切换到含有你项目文件夹的父级文件夹
asar pack your-app/ app.asar

http://blog.csdn.net/yanzi1225627/article/details/51168904
打包工具
npm install -g electron-packager
electron-packager <sourcedir> <appname> --platform=<platform> --arch=<arch> --version=<version>

mac打包命令
electron-packager ./ --platform=mas --arch=x64
electron-packager ./ --platform=mas --arch=x64 --version=0.37.5  指定版本

windows打包
electron-packager ./ demo --platform=win32 --arch=x64 --version=0.37.6
