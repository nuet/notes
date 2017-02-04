
[MAC上卸载Jenkins的方法]
(http://blog.csdn.net/wirelessqa/article/details/17915517)

教程  http://www.jianshu.com/p/c0955ff67c91
    1. Subversion Plug-in 装这个插件
    2. Gradle plugin： Android专用
    3. Xcode integration：iOS专用
    4. GitHub plugin


教程  http://blog.csdn.net/potato512/article/details/52289136
教程  http://www.jianshu.com/p/41ecb06ae95f
    这个讲得很详细, 权限怎么改都有说明

Mac 安装 Jenkins 有两种方法

方法一：
  从官方下载最新版本：http://mirrors.jenkins-ci.org/osx/latest
  点击安装。
  卸载(注意复制带单引号)
  '/Library/Application Support/Jenkins/Uninstall.command'


方法二（推荐）：
使用 homebrew 安装
  brew search jenkins
  jenkins
  brew install jenkins

安装jekins需要先装jdk  http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

下面地方能找到jekins初始化密码
/var/log/jenkins/jenkins.log 中搜索关键字“installation”
