# 用树莓派搭建FM广播，播放音乐和实时语音

在树莓派的命令行界面运行以下八条命令

```shell
mkdir fm
cd fm
sudo git clone https://github.com/markondej/fm_transmitter
sudo apt-get install mpg123
sudo apt-get install gcc g++ make
cd fm_transmitter
sudo make
sudo apt-get install sox
```



运行以下命令，即可在调频100.6MHz频道广播自带的星球大战主题曲：

```shell
sox star_wars.wav -r 22050 -c 1 -b 16 -t wav - | sudo ./fm_transmitter -f 100.6 -
```

按`ctrl`+`c`结束广播。
>也可以把这条命令中的100.6改成其它数字，即可在新频道上广播。
>
>也可以将其它wav格式的文件放到/fm/fm_transmitter文件夹中，替换命令中的star_wars.wav文件
>



插上USB声卡，在USB声卡的麦克风孔里插入麦克风，运行以下命令，在即可在调频100.6MHz频道广播实时语音，你也可以把这条命令中的100.6改成其它数字，那样就会在新频道上广播：

```shell
arecord -D plughw:1,0 -c1 -d 0 -r 22050 -f S16_LE | sudo ./fm_transmitter -f 100.6 -
```

按`ctrl`+`c`结束广播。



扩展玩法：

用移动电源给树莓派供电，设置开机免密码自动登录和自动运行广播脚本，将整个系统装在书包里，即可实现走到哪里，广播开到哪里（旅游景点、重要会场讲话、窃听器、位置信标）



