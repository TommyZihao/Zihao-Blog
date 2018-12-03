>28个有趣的Linux命令行彩蛋和游戏，能让你假装成日理万机的黑客高手。这些命令可以在树莓派和Ubuntu系统上运行，有些还可以在Windows的DOS命令行中运行。
>
>[本文配套B站视频——【子豪兄的零基础树莓派教程】](https://www.bilibili.com/video/av33569265)        
>
>**看完视频后食用本文更佳**
>
>作者：张子豪（同济大学在读研究生）  
>
>关注微信公众号 **人工智能小技巧** 回复 **linux有趣命令** 即可看到本文最新版。
>
>知乎专栏：[人工智能小技巧](https://zhuanlan.zhihu.com/c_1032626015746502656)，所有文章欢迎转载！    
>
>简书专栏：[人工智能小技巧](https://www.jianshu.com/u/38cccf09b515)     
>
>Bilibili视频：[同济子豪兄](https://space.bilibili.com/1900783/#/)     
>
>张子豪写于2018-11-25     
>
>于2018-12-1发布     

![toilet命令彩色字](https://upload-images.jianshu.io/upload_images/13714448-777806bcc005bb31.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![高大上黑客仪表盘](https://upload-images.jianshu.io/upload_images/13714448-660f85e3aeb6a9bf.gif?imageMogr2/auto-orient/strip)

![hollywood命令](https://upload-images.jianshu.io/upload_images/13714448-1921727182271686.gif?imageMogr2/auto-orient/strip)

![字符串水族馆](https://upload-images.jianshu.io/upload_images/13714448-953feec6877d32ca.gif?imageMogr2/auto-orient/strip)

- [1、黑客帝国字节数据流——假装自己是黑客高手，无孔不入](#黑客帝国字节数据流假装自己是黑客高手无孔不入)

- [2、高大上仪表盘blessed-contrib——假装自己指点江山，纵横捭阖](#高大上仪表盘blessed-contrib假装自己指点江山纵横捭阖)

- [3、高大上仪表盘hollywood——假装自己日理万机，宵衣旰食](#高大上仪表盘hollywood假装自己日理万机宵衣旰食)

- [4、追逐鼠标的小猫oneko](#追逐鼠标的小猫oneko)

- [5、ASCII艺术框：box命令](#ascii艺术框box命令)

- [6、燃起字符串大火aafire](#燃起字符串大火aafire)

- [7、火车：**Strem Locomotive**](#火车strem-locomotive)

- [8、盯着鼠标看的大眼睛](#盯着鼠标看的大眼睛)

- [9、艺术字生成器toilet](#艺术字生成器toilet)

- [10、艺术字生成器figlet](#艺术字生成器figlet)

- [11、字符串视频——回归计算机的上古时代](#字符串视频回归计算机的上古时代)

- [12、输出名人名言、古诗词](#输出名人名言古诗词)

- [13、字符串水族馆：ASCIIquarium](#字符串水族馆asciiquarium)

- [14、会说话的牛](#会说话的牛)

- [15、会说话的牛2](#会说话的牛2)

- [16、日历](#日历)

- [17、yes命令](#yes命令)

- [18、分解因数](#分解因数)

- [19、screenfetch:显示系统、主题信息](#screenfetch显示系统主题信息)

- [20、linux各发行版logo图片及系统信息](#linux各发行版logo图片及系统信息)

- [21、图片转ASCII画风](#图片转ascii画风)

- [22、反转字符命令](#反转字符命令)

- [23、打字机pv命令：字幕一个个匀速显示出来](#打字机pv命令字幕一个个匀速显示出来)

- [24、从删库到跑路 sudo rm -rf /\*](#从删库到跑路-sudo-rm--rf)

- [25、播放星球大战](#播放星球大战)

- [26、让命令行说话](#让命令行说话)

- [27、随机产生人名与地址](#随机产生人名与地址)

- [28、超级牛力——包管理器的彩蛋](#超级牛力包管理器的彩蛋)

- [29、命令行游戏bastet：俄罗斯方块](#命令行游戏bastet俄罗斯方块)

- [30、命令行游戏ninvaders：太空入侵者](#命令行游戏ninvaders太空入侵者)

- [31、命令行游戏pacman4console：吃豆人](#命令行游戏pacman4console吃豆人)

- [32、命令行游戏nSnake：贪吃蛇](#命令行游戏nsnake贪吃蛇)

- [33、命令行游戏Greed：赢者通吃](#命令行游戏greed赢者通吃)

- [34、命令行游戏Air Traffic
  Controller：空中塔台控制](#命令行游戏air-traffic-controller空中塔台控制)

- [35、命令行游戏backgammon：双陆棋](#命令行游戏backgammon双陆棋)

- [36、命令行游戏moonbuggy：月球战车](#命令行游戏moonbuggy月球战车)

- [37、命令行游戏2048](#命令行游戏2048)

- [38、命令行也能联机玩网游：Tron](#命令行也能联机玩网游tron)

- [39、命令行游戏：巨洞冒险](#命令行游戏巨洞冒险)

- [40、打印圆周率后小数点若干位](#打印圆周率后小数点若干位)

- [扩展阅读与参考文献](#扩展阅读与参考文献)


# 1、黑客帝国字节数据流——假装自己是黑客高手，无孔不入

在命令行中输入以下命令安装并运行。

```shell
sudo apt-get install cmatrix
cmatrix
```

![cmatrix字节流效果](https://upload-images.jianshu.io/upload_images/13714448-92f96d6586936f3e.gif?imageMogr2/auto-orient/strip)

还可输入参数控制颜色。

```shell
cmatric -C red
```

![cmatrix红色字节流](https://upload-images.jianshu.io/upload_images/13714448-406fef5a59b0446e.gif?imageMogr2/auto-orient/strip)

按`ctrl`+`c`退出。

> 在《黑客帝国》电影里的字节流其实是该片美术指导Simon Whitley的日本妻子菜谱上的片假名。



# 2、高大上仪表盘blessed-contrib——假装自己指点江山，纵横捭阖

```shell
sudo apt-get install npm
sudo apt install nodejs-legacy
git clone https://github.com/yaronn/blessed-contrib.git
cd blessed-contrib
npm install
node ./examples/dashboard.js
```

![高大上黑客仪表盘](https://upload-images.jianshu.io/upload_images/13714448-660f85e3aeb6a9bf.gif?imageMogr2/auto-orient/strip)

> [blessed-contrib项目主页](https://github.com/yaronn/blessed-contrib)  
>
> 建议在云服务器或虚拟机上运行这个命令，在树莓派上运行可能会出问题。



# 3、高大上仪表盘hollywood——假装自己日理万机，宵衣旰食

Dustin Kirkland 利用一个长途飞行的时间，编写了这个炫酷、有趣但也没什么实际作用的软件。

Ubuntu操作系统可以直接通过以下命令安装并运行。

```shell
sudo apt install hollywood
hollywood
```

在其它Linux发行版中，可以通过以下命令安装并运行。

```shell
sudo apt-add-repository ppa:hollywood/ppa
sudo apt-get install hollywood
sudo apt-get install byobu
hollywood
```

![hollywood命令](https://upload-images.jianshu.io/upload_images/13714448-7f75cabe6d2f5560.gif?imageMogr2/auto-orient/strip)

![hollywood命令](https://upload-images.jianshu.io/upload_images/13714448-1921727182271686.gif?imageMogr2/auto-orient/strip)

> [hollywood项目主页](https://github.com/dustinkirkland/hollywood)   





# 4、追逐鼠标的小猫oneko

在桌面的命令行界面输入

```shell
sudo apt-get install oneko
oneko
```

然后输入`oneko`，即可看到效果。

按`ctrl`+`c`退出。

> 注意，本命令只能在桌面所在的命令行界面输入，在远程ssh界面会显示“oneko:Can't open display”

![oneko命令：小猫追鼠标](https://upload-images.jianshu.io/upload_images/13714448-9c07f52aa2939f25.gif?imageMogr2/auto-orient/strip)



# 5、ASCII艺术框：box命令

```shell
sudo apt-get install boxes
echo "Tongji Univerisity" | boxes
echo "Tongji Univerisity" | boxes -d dog
fortune | boxes -d cat | lolcat
```

![box命令](https://upload-images.jianshu.io/upload_images/13714448-e533a44e5f2bbe26.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)





# 6、燃起字符串大火aafire

在命令行界面输入

```shell
sudo apt-get install libaa-bin  
aafire
```

然后输入 `aafire`，即可看到效果

按`ctrl`+`c`退出。

![aafire字符串大火](https://upload-images.jianshu.io/upload_images/13714448-cb38f19a1221c7a1.gif?imageMogr2/auto-orient/strip)

# 7、火车：**Strem Locomotive**

在命令行界面输入

```shell
sudo apt-get install sl
```

然后输入 `sl`，即可看到效果。

![sl命令：字符串火车](https://upload-images.jianshu.io/upload_images/13714448-7afaccc26583811d.gif?imageMogr2/auto-orient/strip)

输入`sl-h`可以看到彩蛋（没有空格）

![字符串火车命令彩蛋](https://upload-images.jianshu.io/upload_images/13714448-eb99852eeb36aa5b.gif?imageMogr2/auto-orient/strip)

> 这个命令其实是在用户把ls命令输错成sl命令的时候准备的彩蛋。

# 8、盯着鼠标看的大眼睛

在命令行界面输入

```shell
sudo apt-get install x11-apps
```

然后输入 `xeyes`，回车，即可看到效果：一双紧盯着鼠标所在位置的大眼睛。

按`ctrl`+`c`退出。

![xeyes大眼睛命令](https://upload-images.jianshu.io/upload_images/13714448-69733edb8e3d12c9.gif?imageMogr2/auto-orient/strip)

#  9、艺术字生成器toilet

在命令行界面输入

```shell
sudo apt-get install toilet
```

然后输入下面任意一行命令，通过在命令中加-f更换字体或滤镜，你可以把命令里的`Tongji University`换成你想要转换的字符。

案例1 

```shell
toilet Tongji University
```

![toilet命令1](https://upload-images.jianshu.io/upload_images/13714448-4ab6cce86ecf5f06.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

案例2 双色字：

```shell
toilet -f mono12 -F metal Tongji University
```

![toilet命令双色字](https://upload-images.jianshu.io/upload_images/13714448-e49e74b6445a50d7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

案例3 彩色字：

```shell
toilet -f mono12 -F gay Tongji University
```

输入`man toilet`查看更多帮助，按`q`退出。

![toilet命令彩色字](https://upload-images.jianshu.io/upload_images/13714448-777806bcc005bb31.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 10、艺术字生成器figlet

在命令行界面输入

```shell
sudo apt-get install figlet
```

然后输入下面任意一行命令，通过在命令中加-f更换字体或滤镜，你可以把命令里的`Tongji University`换成你想要转换的字符。

```shell
figlet Tongji University
```

![figlet命令1](https://upload-images.jianshu.io/upload_images/13714448-205e39c52eed91a4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 11、字符串视频——回归计算机的上古时代

在命令行界面输入

```shell
sudo apt-get install bb
```

然后输入 `bb`，选择`y`加音乐，选择`8`继续，即可看到一段用字符串制作的视频，讲述了视频作者的生涯和使用Linux操作系统的历程，这段视频制作于1997年，基于AAlib平台制作。

按`ctrl`+`c`退出。

> 这段视频的音乐很带感哦~

![bb命令：字符串视频](https://upload-images.jianshu.io/upload_images/13714448-7420604404205ad9.gif?imageMogr2/auto-orient/strip)



# 12、输出名人名言、古诗词

在命令行界面输入

```shell
sudo apt-get install fortune fortune-zh
```

然后输入 `fortune`，即可看到效果。

![fortune命令](https://upload-images.jianshu.io/upload_images/13714448-345cc951023cc6d6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 可以把这个程序设置成每次开机自动启动，每次你登陆的时候就能看到一条新的名人名言或唐诗宋词了。



# 13、字符串水族馆：ASCIIquarium

第一步：安装各种依赖

```shell
sudo apt-get install libcurses-perl
cd /tmp

wget http://search.cpan.org/CPAN/authors/id/K/KB/KBAUCOM/Term-Animation-2.4.tar.gz

tar -zxvf Term-Animation-2.4.tar.gz
cd Term-Animation-2.4/

sudo perl Makefile.PL &&  make &&   make test

sudo make install
```

第二步：安装软件

```shell
cd /tmp
sudo wget https://robobunny.com/projects/asciiquarium/asciiquarium.tar.gz
```

如果显示文件下载失败，可以点击`https://robobunny.com/projects/asciiquarium/asciiquarium.tar.gz`下载压缩包，然后通过FileZilla等文件远程传输软件传输到/tmp文件夹中。

然后继续执行下列命令。

```shell
tar -zxvf asciiquarium.tar.gz
cd asciiquarium_1.1/
sudo cp asciiquarium /usr/local/bin
sudo chmod 0755 /usr/local/bin/asciiquarium
asciiquarium
```

![字符串水族馆](https://upload-images.jianshu.io/upload_images/13714448-953feec6877d32ca.gif?imageMogr2/auto-orient/strip)

> [ASCIIquarium项目主页](https://robobunny.com/projects/asciiquarium/html/?page=0)     

# 14、会说话的牛

在命令行界面输入

```shell
sudo apt-get install cowsay
```

然后输入 `cowsay “Hello Tongji Univerisity”`。

![cowsay命令](https://upload-images.jianshu.io/upload_images/13714448-91cadd9c91f009d4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

只需用 `-l`参数就能看到它能提供的所有动物。

```shell
cowsay -l
```

会输出如下人物，你可以通过`-f`参数加人物名字来更换说话人物：

```shell
# Cow files in /usr/share/cowsay/cows:
apt beavis.zen bong bud-frogs bunny calvin cheese cock cower daemon default
dragon dragon-and-cow duck elephant elephant-in-snake eyes flaming-sheep
ghostbusters gnu head-in hellokitty kiss kitty koala kosh luke-koala
mech-and-cow meow milk moofasa moose mutilated pony pony-smaller ren sheep
skeleton snowman sodomized-sheep stegosaurus stimpy suse three-eyes turkey
turtle tux unipony unipony-smaller vader vader-koala www
```

比如更换成hellokitty：

```shell
cowsay -f dragon 'Hello Tongji Univerisity'
```

![更换说话的动物](https://upload-images.jianshu.io/upload_images/13714448-dcf0c2ce485bbd5e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

也可以利用管道命令，将fortune生成的名人名言在cowsay中输出

```shell
fortune | cowsay
```

加个颜色

```shell
sudo apt install lolcat
```

利用管道命令，让彩色的恐龙大哥说彩色的唐诗：

```shell
fortune | cowsay -f stegosaurus | lolcat
```

![利用管道命令让彩色动物说话](https://upload-images.jianshu.io/upload_images/13714448-11d24b0de66c5007.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 15、会说话的牛2

> 注意，本命令只能在桌面所在的命令行界面输入，在远程ssh命令行界面输入会显示“Can't open display”

在命令行界面输入

```shell
sudo apt-get install xcowsay
```

然后输入 `xcowsay “Hello Tongji Univerisity欢迎来同济大学”`

![xcowsay说中文](https://upload-images.jianshu.io/upload_images/13714448-adab2588c11df68b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 16、日历

直接在命令行界面输入

```shell
cal 12 2018
```

即可看到2018年12月的日历。

![日历命令](https://upload-images.jianshu.io/upload_images/13714448-d8b38641704a03c0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

有趣的是，如果你输入。

```shell
cal 9 1752
```

你会发现这个月少了11天，这是因为当时大英帝国美洲殖民地的历法从凯撒历法换成了格里高利历法，凯撒历法要迟11天，所以这11天成了日历上的空白期。

[1752年9月为什么少了11天？](http://blog.sina.com.cn/s/blog_8713f2c501013md6.html)



# 17、yes命令

直接在命令行界面输入

```shell
yes Tongji University
yes Tongji University | lolcat
```

就会看到无穷无尽输出的Tongji University

按`ctrl`+`c`退出。

![yes命令](https://upload-images.jianshu.io/upload_images/13714448-cb061c5f4e9a2dcc.gif?imageMogr2/auto-orient/strip)

# 18、分解因数

在命令行界面输入

```shell
factor 60
```

即可看到60的分解质因数的结果

![factor命令：分解质因数](https://upload-images.jianshu.io/upload_images/13714448-552691f5ab69af8c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 19、screenfetch:显示系统、主题信息

```shell
sudo apt install screenfetch
screenfetch
```

在开源社区或程序员社区提问时，可以通过这条命令，直接截图，就能很清晰地描述自己的系统环境。

在Ubuntu云服务器上运行：

![在Ubuntu云服务器上运行screenfetch命令](https://upload-images.jianshu.io/upload_images/13714448-11ec8a07f22a4846.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在树莓派上运行：

![树莓派上运行screenfetch命令](https://upload-images.jianshu.io/upload_images/13714448-47504f3bebc05a58.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 20、linux各发行版logo图片及系统信息

```shell
sudo apt install linuxlogo
linux_logo
linux_logo -f -L list
sudo apt-get install neofetch
neofetch
```

在ubuntu云服务器上运行linux_logo

![在ubuntu云服务器上运行linux_logo](https://upload-images.jianshu.io/upload_images/13714448-ba7b79fa4009f951.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在树莓派上运行linux_logo

![在树莓派上运行linux_logo命令](https://upload-images.jianshu.io/upload_images/13714448-d03ff4b5604d5309.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![所有支持打印logo的linux发行版](https://upload-images.jianshu.io/upload_images/13714448-f4549aa6f834cba2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

循环打印所有支持打印的图标

```shell
for i in {1..30};do linux_logo -f -L $i;sleep 0.5;done
```

![打印所有支持的logo](https://upload-images.jianshu.io/upload_images/13714448-eca7597c796ced96.gif?imageMogr2/auto-orient/strip)

# 21、图片转ASCII画风

> 这条命令在树莓派上运行会出问题，建议在云主机或虚拟机上运行。

```shell
sudo apt-get install aview imagemagick

wget http://labfile.oss.aliyuncs.com/courses/1/Linus.png

asciiview Linus.png
```

![Linux之父：Linus的照片](https://upload-images.jianshu.io/upload_images/13714448-7db67728f6ca8b3b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

你可以把wget后面的链接换成任意图片的URL。

比如

```shell
wget http://www.shumeipai.wang/bingbingbing.jpg
asciiview bingbingbing.jpg
```

![范冰冰照片ASCII字符串处理](https://upload-images.jianshu.io/upload_images/13714448-27bab579984d63cc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 22、反转字符命令

在命令行中输入`rev`，打开rev界面，然后输入任意字符，比如

```shell
I am a student in Tongji Univerisity
```

按回车，即可看到字符反转之后的结果

按`ctrl`+`c`退出rev界面回到命令行界面。

```shell
echo "I am a student in Tongji Univerisity" | rev
```

将一句话中所有单词的顺序反转,但在单词内部字母顺序不变

```shell
echo "I am a student in Tongji University" | rev | tr ' ' '\n' | tac | tr '\n' ' '| rev
```

![rev命令](https://upload-images.jianshu.io/upload_images/13714448-1953b01188a746e4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)





# 23、打字机pv命令：字幕一个个匀速显示出来

```shell
sudo apt-get install pv
echo "Tongji Opensource" | pv -qL 10
cal | pv -qL 10
```

![pv打字机命令](https://upload-images.jianshu.io/upload_images/13714448-bc6f86e12e776681.gif?imageMogr2/auto-orient/strip)



# 24、从删库到跑路 sudo rm -rf /*

![sudo rm -rf /](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1539792611926&di=a261ba9fadfa7ba727ef2a7c724016e1&imgtype=0&src=http%3A%2F%2Fi0.hdslb.com%2Fbfs%2Farchive%2Fb6d4f8aa58841f6e8674c3bd46126e5f8ad5fc7f.jpg)

> 友情提示：千万不要轻易尝试这个命令，特别是在运行有网站服务器、数据库的Linux主机上

```shell
sudo rm -rf /*
```

- sudo：获取root管理员权限
- rm：remove，即删除
- -rf：r表示递归删除，即删除所有的子目录，f表示不需要再进行确认
- /：home目录
- *：所有文件

**也就是说，这条命令是删除这台Linux主机上的所有文件，甚至包括开机文件**

关于这条命令的一些有趣的图片：

![删库大爆炸](https://upload-images.jianshu.io/upload_images/13714448-057901398c109d38.GIF?imageMogr2/auto-orient/strip)

![从删库到跑路1](https://upload-images.jianshu.io/upload_images/13714448-9108c4583143f501.GIF?imageMogr2/auto-orient/strip)

![数据库删了肯定要跑路啊](https://upload-images.jianshu.io/upload_images/13714448-e42e61a486b7d1fd.GIF?imageMogr2/auto-orient/strip)

![从删库到跑路2](https://upload-images.jianshu.io/upload_images/13714448-77ce9a2551b16ad4.GIF?imageMogr2/auto-orient/strip)





# 25、播放星球大战

这条命令在windows上都可以运行

1、打开控制面板，找到”启动或关闭Windows功能“，然后打开Telnet客户端。

![控制面板](https://upload-images.jianshu.io/upload_images/13714448-e13443f55165768d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![打开Telnet应用](https://upload-images.jianshu.io/upload_images/13714448-98d0012f082f5cc2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



2、用管理员模式打开DOS命令行界面，输入以下命令，回车。

![进入windows命令行](https://upload-images.jianshu.io/upload_images/13714448-212d2be6bf953cea.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```shell
telnet towel.blinkenlights.nl
```

![字符串星球大战](https://upload-images.jianshu.io/upload_images/13714448-a9b65eda982e05e4.gif?imageMogr2/auto-orient/strip)

![字符串星球大战](https://upload-images.jianshu.io/upload_images/13714448-bb927898d4bd7a3a.gif?imageMogr2/auto-orient/strip)



# 26、让命令行说话

> 运行这个命令不能通过远程连接，必须通过音响

```shell
sudo apt install espeak
espeak 'Hello my dariling'
```



# 27、随机产生人名与地址

```shell
sudo apt-get install rig
rig
```

![rig命令](https://upload-images.jianshu.io/upload_images/13714448-e2b6b7c5e45ce7bc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)





#  28、超级牛力——包管理器的彩蛋

在Ubuntu和Debian上，apt-get包管理器内嵌着一个彩蛋。
如果你在命令行界面输入

```shell
apt-get help
```

在最后一行能找到

This APT has Super Cow Powers。

本APT具有超级牛力。

则说明你的系统可以运行这个菜单。

!["超级牛力"彩蛋](https://upload-images.jianshu.io/upload_images/13714448-13ff4a649e7ce51d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在命令行界面输入

```shell
apt-get moo
```

即可看到这个彩蛋。

aptitiude包管理器也有类似的彩蛋

```shell
aptitude moo
aptitude moo -vv
aptitude moo -vvv
aptitude moo -vvvv
aptitude moo -vvvvv
aptitude moo -vvvvvv
```

![apititude包管理器彩蛋](https://upload-images.jianshu.io/upload_images/13714448-f4d6aad28df0ea0d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 这个彩蛋的灵感来自于法国作家安托万·德·圣·埃克苏佩里童话小说《小王子》的第一章

![小王子插图：法国作家安托万·德·圣·埃克苏佩里童话小说](https://upload-images.jianshu.io/upload_images/13714448-b08afa0b5cc8d6bb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 29、命令行游戏bastet：俄罗斯方块

```shell
sudo apt install bastet
bastet
```

左右键控制方块移动，上键控制方块旋转。

![命令行游戏bastet：俄罗斯方块](https://upload-images.jianshu.io/upload_images/13714448-4187991a1d0416de.gif?imageMogr2/auto-orient/strip)

# 30、命令行游戏ninvaders：太空入侵者

```shell
sudo apt-get install ninvaders
ninvaders
```

按空格键发射子弹。

![命令行游戏ninvaders：太空入侵者](https://upload-images.jianshu.io/upload_images/13714448-cab4c13405bd2dd9.gif?imageMogr2/auto-orient/strip)





# 31、命令行游戏pacman4console：吃豆人

```shell
sudo apt-get install pacman4console
pacman4console
```

使用方向键控制移动。

![命令行游戏pacman4console：吃豆人](https://upload-images.jianshu.io/upload_images/13714448-29f0fdce7a5071c5.gif?imageMogr2/auto-orient/strip)

# 32、命令行游戏nSnake：贪吃蛇

```shell
sudo apt-get install nsnake
nsnake
```

使用方向键控制。

![nSnake贪吃蛇命令行小游戏](https://upload-images.jianshu.io/upload_images/13714448-57c0b9360d55d9b0.gif?imageMogr2/auto-orient/strip)

# 33、命令行游戏Greed：赢者通吃

```shell
sudo apt-get install greed
greed
```

数字表示下一步可前进的步数，游戏的目标是在咬到自己尾巴之前尽可能多走几步。

![命令行游戏Greed：赢者通吃](https://upload-images.jianshu.io/upload_images/13714448-f139804315451e0b.gif?imageMogr2/auto-orient/strip)



# 34、命令行游戏Air Traffic Controller：空中塔台控制

```shell
sudo apt-get install bsdgames
atc
```

在玩之前，你可以先输入`man atc`查看这个游戏的说明文档。游戏的目标是通过一系列命令输入，引导飞机起飞和降落，进行空中塔台调度。

![空中塔台调度游戏atc](https://upload-images.jianshu.io/upload_images/13714448-be5ab52abe3e42f1.gif?imageMogr2/auto-orient/strip)



# 35、命令行游戏backgammon：双陆棋

```shell
sudo apt-get install bsdgames
backgammon
```

这是一款1997年制作的老游戏，游戏开始的时候可以阅读相关规则介绍。

![命令行游戏双陆棋](https://upload-images.jianshu.io/upload_images/13714448-71ea0e1e0d7ba7f9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 36、命令行游戏moonbuggy：月球战车

```shell
sudo apt-get install moon-buggy
moon-buggy
```

![命令行游戏moonbuggy：月球战车](https://upload-images.jianshu.io/upload_images/13714448-d1cecec4d7ac19eb.gif?imageMogr2/auto-orient/strip)



# 37、命令行游戏2048

```shell
wget https://raw.githubusercontent.com/mevdschee/2048.c/master/2048.c
gcc -o 2048 2048.c
./2048
```

![命令行游戏2048](https://upload-images.jianshu.io/upload_images/13714448-49fff6bd836aeffd.gif?imageMogr2/auto-orient/strip)



# 38、命令行也能联机玩网游：Tron

```shell
ssh sshtron.zachlatta.com
```

使用wasd四个键控制蛇的移动，游戏的目标是既不要咬到别人也不要咬到自己，活着的时间越长分数越高。

![命令行也能联机玩网游：Tron](https://upload-images.jianshu.io/upload_images/13714448-a88c4f292ebcd0a8.gif?imageMogr2/auto-orient/strip)



# 39、命令行游戏：巨洞冒险

巨洞冒险Colossal Cave Adventure，又名 ADVENT、Clossal Cave 或 Adventure，是八十年代初到九十年代末最受欢迎的基于文字的冒险游戏。在 1976 年，一个叫 Will Crowther 的程序员开发了这款游戏的一个早期版本，之后另一位叫 Don Woods 的程序员改进了这款游戏，为它添加了许多新元素，包括计分系统以及更多的幻想角色和场景。这款游戏最初是为 PDP-10 开发的，这是一种历史悠久的大型计算机。后来，它被移植到普通家用台式电脑上，比如 IBM PC 和 Commodore 64。游戏的最初版使用 Fortran 开发，之后在八十年代初它被微软加入到 MS-DOS 1.0 当中。

游戏的主要目标是找到一个传言中藏有大量宝藏和金子的洞穴并活着离开它。这款游戏的灵感主要来源于原作者 Will Crowther 丰富的洞穴探索的经历。他曾经经常在洞穴中冒险，特别是肯塔基州的猛犸洞Mammoth Cave。因为游戏中的洞穴结构大体基于猛犸洞，你也许会注意到游戏中的场景和现实中的猛犸洞的相似之处。

```shell
sudo apt-get install python3-yaml libedit-dev
sudo pip3 install PyYAML
git clone https://gitlab.com/esr/open-adventure.git
cd open-adventure
make
make check
advent
```

![命令行游戏巨洞冒险](https://upload-images.jianshu.io/upload_images/13714448-4c3cd5e758ac0d8b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 40、打印圆周率后小数点若干位

```shell
sudo apt-get install pi
pi 50
```

打印小数点后若干位的圆周率。

![圆周率小数点后若干位](https://upload-images.jianshu.io/upload_images/13714448-5e6814eea9cdf956.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)






# 扩展阅读与参考文献

> [10个非常有趣的Linux命令](https://www.cnblogs.com/1394htw/p/6358737.html?utm_source=itdadao&utm_medium=referral)
>
> [超有趣的几个Linux命令，你都用过吗？](https://www.cnblogs.com/1394htw/p/6358737.html?utm_source=itdadao&utm_medium=referral)
>
> [Linux中管道命令的用法](https://blog.csdn.net/tq384998430/article/details/54925742)
>
> [FIGlet初识](https://aotu.io/notes/2016/11/22/figlet/)
>
> [fortune中文格言库](https://github.com/ruanyf/fortunes)
>
> [阮一峰的网络日志：fortune 命令简介](http://www.ruanyifeng.com/blog/2015/04/fortune.html)
>
> [1752年9月为什么少了11天？](http://blog.sina.com.cn/s/blog_8713f2c501013md6.html)
>
> [Linux 奇技淫巧](https://www.cnblogs.com/Nice-Boy/p/6091307.html)
>
> [十大 Linux 命令行游戏](https://zhuanlan.zhihu.com/p/33267251)      
>
> [巨洞冒险：史上最有名的经典文字冒险游戏 | Linux 中国](https://blog.csdn.net/F8qG7f9YD02Pe/article/details/78994286)         
>
> [Shell常识--基本函数和简单命令rev--总结自《Linux Shell 脚本攻略》](https://blog.csdn.net/jsjxy2009/article/details/39207595)
>
> [意想不到的有趣linux命令18个，玩得溜](https://blog.csdn.net/qq_41741971/article/details/82053290)
>
> [apt 和 apt-get的区别](https://blog.csdn.net/liudsl/article/details/79200134)
>
> [blessed-contrib项目主页](https://github.com/yaronn/blessed-contrib)  
>
> [hollywood项目主页](https://github.com/dustinkirkland/hollywood)   
>
> [启用Windows中的Telnet功能一起看DOS版星球大战](https://blog.csdn.net/crazygolf/article/details/48383869/)
>
> [树莓派官方网站](www.raspberry.org)
>
> [树莓派官方杂志MagPi（可免费下载PDF）](https://www.raspberrypi.org/magpi)
>
> [子豪兄翻译的MagPi杂志优质文章](https://github.com/TommyZihao/MagPi_Chinese)
>
> [树莓派实验室](http://shumeipai.nxez.com)
>
> [少数派](https://sspai.com/)
>
> [子豪兄的树莓派零基础教程 Github代码仓库](https://github.com/TommyZihao/ZihaoTutorialOfRaspberryPi)
>
> [子豪兄的Github首页](https://github.com/TommyZihao)
>
> 作者介绍：
>
> 张子豪，同济大学在读研究生。微信公众号、知乎专栏：**人工智能小技巧**。
>
> 自媒体**人工智能小技巧**由同济大学在读研究生张子豪于2018年11月创立。包括微信公众号、知乎专栏、简书专栏、Bilibili视频专栏等。致力于用通俗易懂的大白话帮助零基础非计算机专业的初学者快速掌握人工智能、大数据可视化、区块链、Python趣味编程、树莓派智能硬件等前沿科技知识，并手把手指导新手迅速上手开发实战项目。
>
> 微信公众号：**人工智能小技巧**   
>
> 知乎专栏：[**人工智能小技巧**](https://zhuanlan.zhihu.com/c_1032626015746502656)
>
> Bilibili视频：[同济子豪兄](https://space.bilibili.com/1900783/#/)  
>
> Github代码仓库:[TommyZihao](https://github.com/TommyZihao)      
>
> 个人主页：www.python666.org    
>
> [同济大学开源软件协会](https://mirrors.tongji.edu.cn/)     
> [同济大学微软学生俱乐部](https://baike.baidu.com/item/%E5%90%8C%E6%B5%8E%E5%BE%AE%E8%BD%AF%E6%8A%80%E6%9C%AF%E4%BF%B1%E4%B9%90%E9%83%A8/2952664)  
> [西南人工智能爱好者联盟](http://www.qingxzd.com/front/article/cms/545850)   
> 重庆大学人工智能协会
> [重庆大学树莓派爱好者俱乐部](www.maxoyed.com)      

![树莓派接线](https://projects-static.raspberrypi.org/projects/raspberry-pi-getting-started/13aeb423985e6bacd5d798f5f206a644b7c250a3/en/images/pi-plug-in.gif)

![欢迎加入树莓派全球开源社区](https://upload-images.jianshu.io/upload_images/13714448-9413183a2d79c2a8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
