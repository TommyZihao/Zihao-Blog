# 子豪兄教你在树莓派上安装OpenCV

> 本文介绍了如何在树莓派上安装分别运行在Python2和Python3的OpenCV。
>
> 运行在Python2上的OpenCV安装非常简单，几行命令即可搞定。运行在Python3上的OpenCV安装比较麻烦，需要编译安装，不用担心，本文默认你是新手小白，会一步步指导你安装。本教程经过作者亲自测试，自认为是全网最靠谱的相关教程。
>
> 原创作者：同济大学开源软件协会 [子豪兄Tommy](https://github.com/TommyZihao)  微信公众号：子豪兄的科研小屋
>
> 转载或复制请以 [原文超链接形式](https://github.com/TommyZihao/Zihao-Blog/blob/master/%E5%AD%90%E8%B1%AA%E5%85%84%E6%95%99%E4%BD%A0%E5%9C%A8%E6%A0%91%E8%8E%93%E6%B4%BE%E4%B8%8A%E5%AE%89%E8%A3%85OpenCV.md) 并注明出处 [子豪兄](https://github.com/TommyZihao)。
>
> 原文地址 http://suo.im/5gS6if  发布于2018-10-05

![](https://upload-images.jianshu.io/upload_images/13714448-71d761167d470f47.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/500)

​        OpenCV是程序员钟爱的开源计算机视觉库，拥有强大的内置函数和开源社群。OpenCV配合便携开源廉价的树莓派，可以直接读取来自树莓派摄像头PiCamera的视频，进行人脸识别、边缘检测、语义分割、自动驾驶、图像识别等各种计算机视觉开发。很多优秀开源项目，比如谷歌人工智能框架[Tensorflow](https://github.com/tensorflow/tensorflow)和人脸识别开源项目[face_recognition](https://github.com/TommyZihao/face_recognition/blob/master/README_Simplified_Chinese.md)，都需要安装OpenCV作为运行前提。不少本科生的毕业设计也要用到它。

​        网上关于在树莓派上安装OpenCV的教程很多，老外写的和中国人写的都有，但都**很不靠谱**，经过长达7个月的摸索、屡败屡战的尝试，作者终于找到了靠谱的安装流程，并总结成本文。所有过程亲测有效。

​        运行在Python2上的OpenCV安装非常简单，几行命令即可搞定。运行在Python3上的OpenCV安装比较麻烦，需要编译安装。**作者建议两个都安装**。不用担心，本文默认你是新手小白，会一步步指导你安装。本教程经过作者亲自测试，自认为是全网最靠谱的相关教程。

​        按照本教程安装好之后，你可以迅速上手用树莓派做一个[子豪兄教你用树莓派做人脸识别](https://github.com/TommyZihao/Zihao-Blog/blob/master/%E5%AD%90%E8%B1%AA%E5%85%84%E6%95%99%E4%BD%A0%E7%94%A8%E6%A0%91%E8%8E%93%E6%B4%BE%E5%81%9A%E4%BA%BA%E8%84%B8%E8%AF%86%E5%88%AB.md)。

# ![face_recognition开源项目](https://cloud.githubusercontent.com/assets/896692/24430398/36f0e3f0-13cb-11e7-8258-4d0c9ce1e419.gif)

# 安装前提

### 1.配置好树莓派的Raspbian操作系统

本教程使用的系统是2018年6月27日树莓派官方发布的Raspbian-stretch操作系统，[官方下载链接](https://www.raspberrypi.org/downloads/raspbian/)。

纯新手小白可以参考我写的这两篇文章，从拆盒子到各项配置完毕的树莓派教程。

[子豪兄树莓派系列教程01:树莓派开机教程](https://github.com/TommyZihao/Zihao-Blog/blob/master/01%E6%A0%91%E8%8E%93%E6%B4%BE%E5%BC%80%E6%9C%BA%E6%95%99%E7%A8%8B.md)

[子豪兄树莓派系列教程02:一劳永逸配置树莓派](https://github.com/TommyZihao/Zihao-Blog/blob/master/02%E4%B8%80%E5%8A%B3%E6%B0%B8%E9%80%B8%E9%85%8D%E7%BD%AE%E6%A0%91%E8%8E%93%E6%B4%BE.md)

### 2.切换到国内的apt-get下载源和pip下载源

防止下载速度过慢。

不会换源的新手小白可以参考这篇文章[一劳永逸配置树莓派](https://github.com/TommyZihao/Zihao-Blog/blob/master/02%E4%B8%80%E5%8A%B3%E6%B0%B8%E9%80%B8%E9%85%8D%E7%BD%AE%E6%A0%91%E8%8E%93%E6%B4%BE.md)。

### 3.如果你有树莓派官方的摄像头Picamera，需按如下方法正确配置

> 如果没有官方摄像头，也不影响安装

![连接树莓派摄像头Picamera](https://upload-images.jianshu.io/upload_images/13714448-4b420067401c12f1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/400)



在命令行输入以下命令，这个命令的意思是用nano编辑器打开modules这个文件：

```shell
sudo nano /etc/modules
```

在这个文件末尾添加一行

```shell
bcm2835-v4l2
```

也就是这个效果

![](https://upload-images.jianshu.io/upload_images/13714448-364a600885dd8cdf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

先按键盘上的`ctrl`+`o`，再按回车保存，再按`ctrl`+`x`退出nano编辑器回到命令行界面。

输入命令

```shell
vcgencmd get_camera
```

如果得到下面的结果，则证明摄像头连接成功

![检查摄像头是否被树莓派识别](https://upload-images.jianshu.io/upload_images/13714448-07e411efaac25994.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

可以输入命令

```shell
raspistill -o image.jpg
```

调用摄像头拍一张照片，命名为image.jpg，存储在/pi/home路径，也就是桌面左上角资源管理器一打开显示的那个路径。如果能看到摄像头上红灯亮，目录里面有照片，则进一步说明摄像头配置正确。



# 在树莓派安装运行在Python2上的OpenCV

### 1、安装

 打开树莓派的命令行界面，两个命令即可完成安装。执行第一条命令需要半个小时左右，请耐心等待。第二条命令执行只需要几秒钟。

> 子豪兄友情提示：
>
> 建议第一个命令用树莓派桌面上自带的命令行工具运行，而不要使用远程ssh连接。因为执行命令时间太长，中途如果ssh断线的话无法得知是否已经安装完毕。

```shell
sudo apt-get install libopencv-dev
sudo apt-get install python-opencv
```

# 2、在Python2上测试OpenCV

安装好之后，在命令行中输入`python`或者`python2`，回车

```python
import cv2
```

如果出现下图的结果，说明Python2环境下的OpenCV安装成功。

![python2环境中运行opencv](https://upload-images.jianshu.io/upload_images/13714448-202da54ab2900054.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

也可以输入

```python
cv2.__version__
```

查看opencv版本号

![查看python2的opencv版本](https://upload-images.jianshu.io/upload_images/13714448-f97eed06c60e3c03.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 为啥叫cv2而不叫opencv呢？这是因为OpenCV是基于C/C++开发的，有两个版本，''cv”版本的API是C语言开发的，''cv2''版本的API是基于C++语言开发的，为了保持向后兼容性所以叫"cv2"，但我们都知道cv2就是OpenCV本尊。

也可以在桌面命令行里输入以下三个命令调用树莓派摄像头，把摄像头捕捉到的画面显示在桌面上，按`ctrl`+`c`键退出。

```shell
git clone https://github.com/TommyZihao/opencvtest.git
cd opencvtest
python2 testopencv.py
```

![测试python2上的opencv：调用树莓派摄像头](https://upload-images.jianshu.io/upload_images/13714448-4558d79be1004043.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



## 在树莓派安装运行在Python3上的OpenCV

### 1、安装numpy

打开命令行界面，输入以下命令，安装Python科学计算库numpy

```shell
sudo pip3 install numpy
```

### 2、在树莓派设置中把根目录扩大到整个SD卡

命令行界面输入命令，进入树莓派配置界面。用上下键和左右键切换光标位置。

```shell
sudo raspi-config
```

![树莓派配置界面](https://upload-images.jianshu.io/upload_images/13714448-59742b839ab0c666.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### 第七行：Advanced Options

![Adcanved Options](https://upload-images.jianshu.io/upload_images/13714448-1d3bb4659426dce8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

选择Expand Filesystem，将根目录扩展到这个SD卡，充分利用SD卡的存储空间。如果不进行这一步，后续命令会出现卡死。退出设置界面，重启树莓派。

```shell
sudo reboot
```

### 3、安装OpenCV所需的库

挨个运行下面八条命令。共需要七分钟（注意倒数第三条命令中要安装四个-dev软件包）。

```shell
sudo apt-get install build-essential git cmake pkg-config -y
sudo apt-get install libjpeg8-dev -y
sudo apt-get install libtiff5-dev -y
sudo apt-get install libjasper-dev -y
sudo apt-get install libpng12-dev -y

sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev -y

sudo apt-get install libgtk2.0-dev -y
sudo apt-get install libatlas-base-dev gfortran -y
```

### 4、下载OpenCV

在命令行输入以下三条命令，下载两个压缩包到树莓派的**/home/pi/Downloads**目录下。第一个压缩包86.8MB，第二个压缩包54.5MB：

```shell
cd

wget https://github.com/Itseez/opencv/archive/3.4.0.zip

wget https://github.com/Itseez/opencv_contrib/archive/3.4.0.zip
```

>如果下载速度很慢（比如每秒几个KB）：
>
>方法1：可以在电脑浏览器中输入wget后面的链接下载压缩包，再用Fillzilla或者U盘等方法把文件传输到树莓派的**/home/pi/Downloads**目录下（一定不能错）。
>
>方法2：:可以用电脑在[百度网盘链接](https://pan.baidu.com/s/182NYJzW1nCpnQ7ftSYYuSw)下载这两个压缩包之后再用Fillzilla或者U盘等方法把文件传输到树莓派的**/home/pi/Downloads**目录下（一定不能错）。

解压这两个压缩包

```shell
cd /home/pi/Downloads
unzip opencv-3.4.0.zip
unzip opencv_contrib-3.4.0.zip
```

### 5、设置编译参数

设置编译参数

```shell
cd /home/pi/Downloads/opencv-3.4.0
mkdir build
cd build
```

设置CMAKE参数，注意，下面这是一行命令（包括最后那俩点儿），需要耐心等待十五分钟左右：

```shell
cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D INSTALL_C_EXAMPLES=ON -D INSTALL_PYTHON_EXAMPLES=ON -D OPENCV_EXTRA_MODULES_PATH=/home/pi/Downloads/opencv_contrib-3.4.0/modules -D BUILD_EXAMPLES=ON -D WITH_LIBV4L=ON PYTHON3_EXECUTABLE=/usr/bin/python3.5 PYTHON_INCLUDE_DIR=/usr/include/python3.5 PYTHON_LIBRARY=/usr/lib/arm-linux-gnueabihf/libpython3.5m.so PYTHON3_NUMPY_INCLUDE_DIRS=/home/pi/.local/lib/python3.5/site-packages/numpy/core/include ..
```

根据下图判断你是否配置成功了CMAKE。如果失败，可能是因为两个压缩包的路径没有严格按照上文的要求。如果成功，就可以开始最重要的编译了。

![CMAKE配置](https://upload-images.jianshu.io/upload_images/13714448-532012bb713dc869.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### 6、编译

最后一步，也是最重要的一步：编译

保证树莓派有至少5G的存储空间，建议本命令用树莓派桌面上的命令行工具运行，而不要使用远程ssh连接。因为执行命令时间太长，中途如果ssh断线的话无法得知是否已经安装完毕。

```shell
cd /home/pi/Downloads/opencv-3.4.0/build
make
```

![开始编译](https://upload-images.jianshu.io/upload_images/13714448-36df3d7c4c6c0db7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

编译两个小时之后，完成了40%

![编译两个小时之后](https://upload-images.jianshu.io/upload_images/13714448-e938295662efec1e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

静待五个小时的编译。注意，在此期间，树莓派要供电充足，不要运行其它任务，以免因为内存不够什么的幺蛾子报错。

![编译完成](https://upload-images.jianshu.io/upload_images/13714448-542b34f0f59da291.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

`make`命令执行完成之后，执行下面的命令，执行命令需要一分钟：

```shell
sudo make insall
```

### 7、在Python3上测试OpenCV

安装好之后，在命令行中输入`python3`，回车

```python
import cv2
```

回车

```shell
cv2.__version__
```

回车

如果出现下图的结果，说明Python3环境下的OpenCV安装成功。

![Python3的OpenCV安装完成](https://upload-images.jianshu.io/upload_images/13714448-8b4162cec9589cd6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



> 子豪兄批注：
>
> 我从2018年3月7日第一次尝试在树莓派上安装opencv，看了无数教程，历经无数次失败。有的教程要配置虚拟环境，有的要修改内存分配空间；有的教程使用树莓派四个cpu核心同时编译，每次都会报错；有的教程对新手小白极其不友好，完全不知该怎么操作。在七个月的努力成功之后，我想用我的血泪史书写本文，让每一个新手小白都能迅速上手而不是被bug卡到举目无亲。
>
> 本文会在未来继续更新和勘误，最新版以Github上的[子豪兄博客合集](https://github.com/TommyZihao/Zihao-Blog)为准
>
> 转载或复制请以 [原文超链接形式](https://github.com/TommyZihao/Zihao-Blog/blob/master/%E5%AD%90%E8%B1%AA%E5%85%84%E6%95%99%E4%BD%A0%E5%9C%A8%E6%A0%91%E8%8E%93%E6%B4%BE%E4%B8%8A%E5%AE%89%E8%A3%85OpenCV.md) 并注明出处 [子豪兄](https://github.com/TommyZihao)。
>
> 原文地址 http://suo.im/5gS6if  发布于2018-10-05
>
> 同济大学开源软件协会
>
> 重庆大学树莓派爱好者俱乐部、人工智能协会、创新实践中心



![](https://upload-images.jianshu.io/upload_images/13714448-1c1f91c8b56023a9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![微信扫码支持子豪兄制作树莓派教程](https://upload-images.jianshu.io/upload_images/13714448-4be7dc29e22207b4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/300)



## 参考文献与扩展阅读

> [【树莓派】树莓派+OpenCV3.4 + python3.5 成功以及注意细节](https://www.jianshu.com/p/3180a253fe3c)
>
> [树莓派安装Python-OpenCV](https://blog.csdn.net/u014397533/article/details/50910531)
>
>  [基于树莓派3B+Python3.5的OpenCV3.4的配置教程](https://www.cnblogs.com/Pyrokine/p/8921285.html)

![树莓派接线](https://projects-static.raspberrypi.org/projects/raspberry-pi-getting-started/13aeb423985e6bacd5d798f5f206a644b7c250a3/en/images/pi-plug-in.gif)

![欢迎加入树莓派全球开源社区](https://upload-images.jianshu.io/upload_images/13714448-9413183a2d79c2a8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![合作伙伴](https://upload-images.jianshu.io/upload_images/13714448-0a9e2bed7ab10925.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
