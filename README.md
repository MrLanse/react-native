# react-native
react-native开发遇到的一些问题

1.初始化react-native项目 build失败
  最新0.45版本 build failed
  切换到0.44版本 build success 但是报错 ——Dev——is not define
  删除目录内的隐藏文件 .babelrc
  删除后可以正常build

2.mac上配置好环境后 rect-native run-android失败
  报错：
  Could not install the app on the device, read the error above for details.
  Make sure you have an Android emulator running or a device connected and have
  set up your Android development environment:
  https://facebook.github.io/react-native/docs/android-setup.html
  解决办法：
   //1.在app的根目录下运行
   chmod 755 android/gradlew
   //2.然后再运行就正常了
   react-native run-android
   
    Mac安装android studio后卡在building gradle project info的解决方法。
    1.找到.gradle目录，一般在/User/<用户名>/下；需要执行defaults write com.apple.finder AppleShowAllFiles Yes && killall Finder命令显示隐藏的文件即可看到.gradle文件夹
    2.进入.gradle/wrapper/dists/gradle-3.3-all/55gk2rcmfc6p2dg9u9ohc3hw9文件夹下，删除.part文件
    3.去gradle网站下载对应的cradle-3.3-all.zi文件，下载完成后不解压放入55gk2rcmfc6p2dg9u9ohc3hw9文件夹下
    4.重新打开android studio问题已经解决Mac安装android studio后卡在building gradle project info的解决方法
