> 微软Custom Vision提供了成熟开源的计算机视觉开发框架，你只需要上传十张训练图片，即可一键训练图像分类模型（比如识别不同的水果、花卉、地标、人脸）。不需要具备任何深度学习算法知识，小学生都能快速上手。Custom Vision提供了API接口，你还可以将模型部署在网站、手机移动端、微信小程序中。
>
> 作者：张子豪（同济大学微软学生俱乐部）  
>
> 微信公众号：人工智能小技巧   
>
> [本文配套B站视频：用微软Custom Version识别水果—不用写代码，三分钟做一个人工智能小应用](https://www.bilibili.com/video/av35093833)        
>
> 发布于2018-11-8  

[TOC]

# 美剧《硅谷》中的热狗识别app

在美剧《硅谷》中，程序员Jian-Yang开发了一款识别图片中物体是不是热狗的app，虽然听名字就知道，功能十分鸡肋弱智，但由于搭上了人工智能和虚拟现实的快车，这个app迅速获得了硅谷风投公司的青睐并大捞一笔。这部剧深刻讽刺了人工智能浪潮下的经济泡沫以及硅谷投资人的盲目冲动。难怪十九大报告中提出要将”人工智能与实体经济深度融合“。

其实，你也可以用不到三分钟时间轻松开发一款类似的应用，也许下一个硅谷弄潮儿就是你！

![热狗识别app](https://upload-images.jianshu.io/upload_images/13714448-da713087881404a6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![Not Hotdog](https://upload-images.jianshu.io/upload_images/13714448-904960a8b5e3f189.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 微软开源机器视觉开发平台Custom Vision

微软Custom Vision提供了成熟开源的计算机视觉开发框架，你只需要上传十张训练图片，即可一键生成图像分类app。你不需要具备任何深度学习、图像处理的算法知识，小学生都能快速上手。Custom Vision提供了API接口，你还可以将模型部署在网站、手机移动端、微信小程序中。

[本文配套B站视频：用微软Custom Version识别水果—不用写代码，三分钟做一个人工智能小应用](https://www.bilibili.com/video/av35093833)        

关注微信公众号 **人工智能小技巧** 回复 **苹果** 即可看到这个视频。

![Custom Vision](https://upload-images.jianshu.io/upload_images/13714448-772791bb655b9428.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 第一步：新建模型项目

[Custom Vision官网](https://www.customvision.ai/)  

点击进入后免费注册微软账号，即可新建模型项目。

![工作流程](https://upload-images.jianshu.io/upload_images/13714448-816b5556330f33ff.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![新建项目](https://upload-images.jianshu.io/upload_images/13714448-120511366ca16c93.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 第二步：上传训练图片并打标签

![上传图片并打标签](https://upload-images.jianshu.io/upload_images/13714448-d422bdabe7f36d41.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

> 注意事项：
>
> 1、不能只上传一个标签的图片，否则模型无法通过**交叉验证**的方式对照学习。也就是说，不能只上传苹果的图片，而是至少上传苹果和香蕉两种水果的图片并分别打标签。
>
> 2、上传的训练图片要包含对象整体，而非局部。
>
> 3、上传不同背景、角度、大小的照片。
>
> 4、每个标签上传十几张图片就够了。



# 第三步：训练模型

## 点击右上角绿色的"Train"按钮

![训练模型](https://upload-images.jianshu.io/upload_images/13714448-b9ed2f5683eb1cf0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

等待几秒钟之后，模型就训练完成了。

## 模型评估参数

窗口中显示的Precision和Recall是用于评价我们训练的分类模型分类效果的两个参数。

Precision：被预测为苹果的结果中有多少真实就是苹果。

Recall：真实为苹果的样本中有多少被预测正确了。

> 简单来说，Precision就是宁可放过不可杀错，Recall就是宁可杀错不可放过。

在机器学习领域，通常使用F-measure参数将这两个参数综合起来。

![Precision与Recall](https://upload-images.jianshu.io/upload_images/13714448-a746e7d6eee8c1e1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



Precision和Recall随着分类阈值的变化而此消彼长（举例说明），使用Precision-recall曲线，来显示出分类器在Precision与Recall之间的权衡。 

打个比方，如果有个人号称是地震预测的专家，如果他每天都说第二天不会发生大地震，那么他有相当大的概率能够预测成功，也就是说Precision很大。但我们不能说这就是一个好的模型，因为当地震真来临的时候他能够预测成功的概率是0，也就是Recall很低。综合起来的F-measure也很低，所以这是一个失败的分类器。

再打个比方，医疗诊断用的试剂有假阳性和假阴性，假阳性指的是一个正常人被测出有癌症，假阴性指的是一个癌症病人测出来没有癌症，这和Precision和Recall的道理也是一样的。



# 第四步：测试模型

点击右上角的Quick Test，进入测试界面，既可以上传图片文件，也可以上传图片的URL地址，模型就能正确识别出图片属于哪一类标签。

![快速测试](https://upload-images.jianshu.io/upload_images/13714448-9ab81bb7eaf5f279.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![快速测试](https://upload-images.jianshu.io/upload_images/13714448-b9e025dd858b0a20.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 第五步：扩展开发—使用API编写Python脚本程序

Custom Vision提供了API接口，你可以将训练模型部署在网站、手机移动端、微信小程序中，从而开发自己的用户界面，并大批量识别图片。

在Performance栏中，选择Prediction URL，打开API界面。

![Predicton URL](https://upload-images.jianshu.io/upload_images/13714448-d182a50ce283db80.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![API](https://upload-images.jianshu.io/upload_images/13714448-b337ce4b350de5df.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)利用Python的requests库，构造post请求，Python脚本代码如下：

将body栏里的Url链接更换成你要识别的图片链接。

```python
# 同济大学张子豪于2018年11月2日编写 
# 微信公众号：人工智能小技巧
import requests

def getHTMLText(url):
    try:
        headers = \
        {
            "Prediction-Key": "7e1469b8051b45329814ef7f2275a3ff",
            "Content-Type": "application/json",
        }
        body = \
        {
            "Url": "https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=684871772,3282663100&fm=27&gp=0.jpg",
        }
    # Set Prediction-Key Header to : 7e1469b8051b45329814ef7f2275a3ff
    # Set Content-Type Header to : application/json
    # Set Body to : {"Url": "https://example.com/image.png"}
        r = requests.post(url,timeout=30,headers=headers,json=body)
        r.raise_for_status()  #如果状态不是200，引发HTTPError异常
        r.encoding = r.apparent_encoding
        return r.text
    except:
        return '产生异常'

if __name__ == "__main__":
    url = "https://southcentralus.api.cognitive.microsoft.com/customvision/v2.0/Prediction/7c9b4755-271f-4d32-82c5-3c93ba34df8b/url?iterationId=c4927c90-b28a-4c22-9957-3e0b4f2ce99e"
    print(getHTMLText(url))


```

例如，用下列[测试图片](https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=684871772,3282663100&fm=27&gp=0.jpg)做测试，运行Python脚本，结果如下：是香蕉的概率为100%。通过这个程序，你可以将这个图像分类模型部署在自己的云服务器上，搭建自己的网站、手机APP、微信小程序，向用户提供图像分类服务。

![测试图片](https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=684871772,3282663100&fm=27&gp=0.jpg)

![运行结果](https://upload-images.jianshu.io/upload_images/13714448-658936bcb78acfd0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 微软开源人工智能工具和深度学习框架

[微软开源人工智能工具和深度学习框架介绍](https://blog.csdn.net/qq_41822781/article/details/83688944)   

关注微信公众号 **人工智能小技巧** 回复 **微软** 即可看到这篇文章。

本文介绍了微软在人工智能领域的领先成果、产品线，开源人工智能框架和工具。读者可以运用这些工具快速开发机器视觉、语音处理、视频检索等丰富的人工智能应用。  

![微软AI产品](https://upload-images.jianshu.io/upload_images/13714448-445ebd0ec569e7b0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![微软Cognitive Service](https://upload-images.jianshu.io/upload_images/13714448-5b8943f26c2eafe0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![微软开源人工智能框架CNTK](https://upload-images.jianshu.io/upload_images/13714448-0bcf0b72ba37157e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 同济大学微软学生俱乐部

![同济大学微软学生俱乐部](https://upload-images.jianshu.io/upload_images/13714448-9fba99721363735c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 参考文献与扩展阅读

> [Custom Vision](https://www.customvision.ai/)
>
> [【YOLO学习】召回率（Recall），精确率（Precision），平均正确率（Average_precision(AP) ），交除并（Intersection-over-Union（IoU））](https://blog.csdn.net/hysteric314/article/details/54093734)
>
> [用Microsoft Custom Vision技术识别点东西吧](http://www.sohu.com/a/227641551_181341)
>
> [学堂在线慕课：微软人工智能-深度学习框架和工具](http://www.xuetangx.com/courses/course-v1:MicrosoftX+Microsoft106+2017_T2/pdfbook/0/)    
>
> [用Microsoft Custom Vision技术识别点东西吧](http://www.sohu.com/a/227641551_181341)  
>
> [科普文：大白话讲解卷积神经网络工作原理](https://github.com/TommyZihao/Zihao-Blog/blob/master/%E5%A4%A7%E7%99%BD%E8%AF%9D%E8%AE%B2%E8%A7%A3%E5%8D%B7%E7%A7%AF%E7%A5%9E%E7%BB%8F%E7%BD%91%E7%BB%9C%E5%B7%A5%E4%BD%9C%E5%8E%9F%E7%90%86.md)  
>
> [B站视频：不用写代码，三分钟做一个人工智能小应用](https://www.bilibili.com/video/av35093833)  
>
> [视频：三分钟走进卷积神经网络](https://www.bilibili.com/video/av35094580)  
>
> [视频：大白话讲解卷积神经网络工作原理](https://www.bilibili.com/video/av35087157)  
>
> [微软亚洲研究院](https://www.msra.cn/)   
>
> [微软亚洲研究院20年20人](https://baijiahao.baidu.com/s?id=1616265160012096539&wfr=spider&for=pc)  
>
> 作者介绍：
>
> 张子豪，同济大学在读研究生。微信公众号**人工智能小技巧**运营者。致力于用人类能听懂的语言向大众科普人工智能前沿科技。目前正在制作《说人话的人工智能视频教程》、《零基础入门树莓派趣味编程》等视频教程。西南地区人工智能爱好者高校联盟联合创始人，重庆大学人工智能协会联合创始人。充满好奇的终身学习者、崇尚自由的开源社区贡献者、乐于向零基础分享经验的引路人、口才还不错的程序员。
>
> 说人话的零基础深度学习、数据科学视频教程、树莓派趣味开发视频教程等你来看！
>
> 微信公众号：**人工智能小技巧**   
>
> Github代码仓库:TommyZihao   
>
> 个人主页：www.python666.org    
>
> [同济大学开源软件协会](https://mirrors.tongji.edu.cn/)     
> 同济大学微软学生俱乐部    
> 西南人工智能爱好者联盟   
> 重庆大学人工智能协会      
