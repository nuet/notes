


sudo gem install cocoapods
pod install


# 这个能解决, 原因装了react-native, 可能对设置有修改
RPC failed; curl 56 SSLRead() return error -9806.00 KiB/s
解决 参考:  http://stackoverflow.com/questions/39434447/unable-to-setup-pods-error-rpc-failed-curl-56-sslread-return-error-9806?rq=1
brew remove git
brew remove curl
brew install openssl
brew install --with-openssl curl
brew install --with-brewed-curl --with-brewed-openssl git
参考:
网上面说的好多都解决不了实质问题 其实是git的问题 我电脑最近安装过react-native 配置过的东西有可能对git的文件有重写和覆盖,然后继续配置brew的openssl就可以了http://stackoverflow.com/questions/39434447/unable-to-setup-pods-error-rpc-failed-curl-56-sslread-return-error-9806 

如果报错则执行下面三行  [!] Unable to add a source with url `https://github.com/CocoaPods/Specs.git` named `master`. You can try adding it manually in `~/.cocoapods/repos` or via `pod repo add`.
xcode-select --print-path  能看xcode的安装位置
sudo xcode-select -switch /Applications/Xcode.app
sudo xcode-select -switch /Applications/Xcode.app/Contents/Developers  
cd ~/.cocoapods/repos
git clone https://github.com/CocoaPods/Specs.git master

// 上面报错用下面方式解决了
cd ~/.cocoapods/repos
/Applications/Xcode.app/Contents/Developer/usr/bin/git clone https://github.com/CocoaPods/Specs.git master


sudo xcode-select -switch 后面当前xcode路径
pod update --no-repo-update
pod install --verbose --no-repo-update


gem sources --remove https://rubygems.org/
gem sources -l
gem sources -a https://gems.ruby-china.org/


You might also want to try sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer.

Does /Applications/Xcode.app/Contents/Developer/usr/bin/git exist for you? If not, I'd suspect a broken Xcode installation might be the problem.




https://github.com/CocoaPods/Specs.git/': SSLRead() return error -9806
