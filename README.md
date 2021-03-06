# Pixiv

> 关于我，欢迎关注：
>
> 个人博客：[mrcai.space](https://mrcai.space)
> 
> Github 主页：[MrCaiDev](https://github.com/MrCaiDev)
>
> 个人邮箱：1014305148@qq.com
>
> 工作邮箱：yuwangcai@std.uestc.edu.cn

## 项目介绍

通过镜像网站[pixivel.moe](https://pixivel.moe/)对Pixiv的图片进行爬取和下载。无需梯子，异步下载。

目前已实现四项爬取功能：

- 按<插画ID>下载图片
- 按<画师ID>下载图片
- 按<排行榜>下载图片
- 按<标签+人气值>下载图片

## 使用方法

该程序在终端运行，用户输入指令来下载插画。具体指令说明如下：

### help

查看某一功能的使用帮助。

**指令格式**

`>>> help [功能(选填)]`

**例1**

查看整个程序的帮助：

`>>> help`

**例2**

查看功能“按<插画ID>下载图片”的帮助：

`>>> help id`

### quit

用户执行完所有指令后，退出程序。

**指令格式**

`>>> quit`

### id

按插画ID查找插画并下载。

**指令格式**

`>>> id [插画ID]`

**例**

下载[84026087]这幅插画：

`>>> id 84026087`

### member

按画师ID查找画师，并下载画师最新的若干幅插画。

程序会在下载开始前告诉您这位画师的名字，以便确认TA是否是您要找的画师。

**指令格式**

`>>> member [画师ID] [插画数量]`

**例**

下载画师[1980643]的最新[3]幅插画：

`>>> member 1980643 3`

### rank

从排行榜上，下载最热门的若干幅插画。

如果您没有指定排行模式，程序会默认为您从**日榜**下载。
如果您没有指定下载多少幅，程序会默认为您下载该排行榜前**30**幅插画。

排行模式见下表：

| 参数     | 排行模式 |
| -------- | -------- |
| day      | 日榜     |
| week     | 周榜     |
| month    | 月榜     |
| male     | 男性日榜 |
| female   | 女性日榜 |
| original | 原创榜   |
| rookie   | 新人榜   |
| manga    | 漫画日榜 |

**指令格式**

`>>> rank [排行模式(选填)] [插画数量(选填)]`

**例1**

默认下载[日榜]前[30]幅插画：

`>>> rank`

**例2**

下载[周榜]前[10]幅插画：

`>>> rank week 10`

### tag

搜索带有指定标签的，人气高于指定值的，最新的若干幅插画。

标签随便写多少个都可以，但能不能搜出结果就得看Pixiv的算法了。
如果您没有指定最低人气值，程序会为您全部下载。(即指定人气值默认为0。)

**指令格式**

`>>> tag [标签] [插画数量] [人气值(选填)]`

**例1**

下载带有[miku]标签的最新[10]幅插画：

`>>> tag miku 10`

**例2**

下载同时带有[VOCALOID]和[miku]标签的前[10]幅插画，并且人气高于[10000]：

`>>> tag VOCALOID miku 10 10000`

## 注意事项

如果您在程序运行过程中误删了输出文件夹，本程序虽然可以重新创建，但似乎会影响本地写入图片数据的速度，所以尽量还是不要进行这样的误操作......

其他bug暂时未发现。
