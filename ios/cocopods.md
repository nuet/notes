


sudo gem install cocoapods
pod install

如果报错则执行下面三行  [!] Unable to add a source with url `https://github.com/CocoaPods/Specs.git` named `master`. You can try adding it manually in `~/.cocoapods/repos` or via `pod repo add`.
xcode-select --print-path  能看xcode的安装位置
sudo xcode-select -switch /Applications/Xcode.app
cd ~/.cocoapods/repos
git clone https://github.com/CocoaPods/Specs.git master
