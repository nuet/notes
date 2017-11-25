

显示Mac隐藏文件的命令：defaults write com.apple.finder AppleShowAllFiles  YES
隐藏Mac隐藏文件的命令：defaults write com.apple.finder AppleShowAllFiles  NO

当前文件夹直接打开终端设置和使用
Finder->左上角点击->服务->服务偏好设置->快捷键->文件和文件夹->新建位于文件夹位置的终端窗口
Finder->右键文件夹->服务->新建位于文件夹位置的终端窗口


加密压缩
zip -e 输出文件.zip '源文件wap.doc'


电脑文件 -> 手机
adb push ~/Downloads/abc/tee.xlsx /mnt/sdcard/download/
电脑文件夹 -> 手机
adb push ~/Downloads/aaa/ /mnt/sdcard/aaa/


手机 -> 电脑
adb pull sdcard/DCIM/Camera/mp4 ~/Downloads/mp4
adb pull sdcard/aaa/mp4/ ~/Downloads/mp4
