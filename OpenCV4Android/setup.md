1、设置OpenCV

需要设置的内容有：

- JDK
- Cygwin
- Android SDK
- ADK
- Eclipse
- JDT
- CDT
- ADT
- OpenCV4Android

1.1 AndroidStudio下载和安装OpenCV4Android

1.1. 下载地址
[OpenCV-2.4.8-android-sdk](http://jaist.dl.sourceforge.net/project/opencvlibrary/opencv-android/2.4.8/OpenCV-2.4.8-android-sdk.zip)
1.2 解压OpenCV-2.4.8-android-sdk.zip
1.3 首先 导入sdk目录下的java目录到AndroidStudio里，并构建该模块
1.4 然后导入sample目录下的fade-detection工程，构建并运行
1.5 运行程序会报错，提示加载库失败，原因是AndroidStudio不支持NDK，所以jni的代码没有编译


