
参考
[React Native 集成到原生项目(iOS)]
(http://www.jianshu.com/p/3dc9d70a790f)

[]
(http://www.jacpy.com/2016/09/06/react-native-ios-integrated.html)(按照这篇配置成功)
(tvOS库要删掉,否则编译不成功)

[ReactNative集成到已有工程中-IOS]
(https://segmentfault.com/a/1190000004253916)[Linking Libraries]
(http://facebook.github.io/react-native/docs/linking-libraries-ios.html)(官方教程rn集成到ios)[链接原生库]
(http://reactnative.cn/docs/0.39/linking-libraries-ios.html#content)(不错)


npm install -g yarn
npm install -g react-native-cli
react-native init awesomeProject
cd awesomeProject
react-native start
react-native run-ios
react-native run-android

gem install  cocoa pods
//权限不够则运行下面一句
sudo gem install cocoapods


Build Phases->Linking Binary With Libaries->
删掉:Pods_MySwiftProject.xcworkspace


[react-native-swipeout]
(https://github.com/dancormier/react-native-swipeout/tree/master/example/ios/swipeoutExample.xcodeproj)
