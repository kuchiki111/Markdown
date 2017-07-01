# Raspberry Pi 3使用IoT Dashboard和NOOBS 安装 windows IoT以及Raspbian 系统
主要介绍Raspberry的两个主要系统win10 IoT和Raspbian的安装方式，其中win10 IOT 使用IoT Dashboard来进行系统安装，Raspbian使用NOONS来进行安装。

## 一、使用IoT Dashboard安装win10 IOT Core
>Windows 10 IoT Core 是微软针对物联网市场的一个重要产品，与以往的Windows版本不同，是为物联网设备专门设计的，硬件也不仅仅限于x86架构，同时可以在ARM架构上运行。

### 1.准备工作
- Raspberry Pi 3
- TF卡 大于8G，CLASS 10
- TF读卡器
- Win10系统的电脑

### 2.下载安装Windows 10 IoT Core Dashboard
下载Windows 10 IoT Core Dashboard [安装文件](http://go.microsoft.com/fwlink/?LinkID=708576),下载完成后安装程序。**程序在Win10系统上才能安装**

### 3.下载Windows 10 IoT Core 镜像文件
下载Windows 10 IoT Core [镜像文件](https://go.microsoft.com/fwlink/?LinkId=846058),下载完成后运行安装文件可以得到一个flash.ffu的文件。这个就是Win10 IOT Core 的镜像文件。

### 4. 为Raspberry 安装 win10 IoT Core系统
打开安装好的Windows 10 IoT Core Dashboard
1. 选择设置新的设备
2. 设备类型选择自定义
3. 选择刚刚得到的flash.ffu文件
4. 驱动器选择插入TF卡的读卡器
5. 最后设置密码同意协议以后就可以安装了

![](http://images2015.cnblogs.com/blog/1116939/201706/1116939-20170630161442664-593416313.png)

### 5.运行Win10 IoT Core
将安装好系统的TF卡插入Raspberry，接通电源、显示器、键盘等。第一次进入系统会在WIndows界面较长时间，期间不能中断电源。最后进入系统界面以后就表示安装成功了。

## 二、使用NOOBS安装Raspbian
>Raspbian针对 Raspberry Pi 专门优化、基于 Debian 的 Raspbian OS。它面向 Raspberry Pi 硬件（armhf 处理器架构）而做了优化。

>New Out of Box Software （NOOBS）是树莓派官方发布的工具，是一种新颖的设置程序，很方便的让第一接触Linux和树莓派的玩家能更轻松的运行上树莓派。

### 1.准备工作
- Raspberry Pi 3
- TF卡 大于8G，CLASS 10
- TF读卡器

### 2.格式化TF卡
格式化TF卡，最好使用[SD Formatter 4.0 tool](https://www.sdcard.org/downloads/formatter_4/)进行格式化。

### 3.下载NOOBS
下载NOOBS[文件](https://downloads.raspberrypi.org/NOOBS_lite_latest),完成后将文件解压缩，将解压得到的所有文件拷贝到TF卡根目录。

### 4.安装Raspberry系统
将TF卡插入Raspberry，接通电源、显示器、键盘等。开机后选择需要安装的操作系统，NOOBS会自动将TF分区。这边需要从网络上下载完整的系统，所需要的时间会很长很长。

![](http://images2015.cnblogs.com/blog/1116939/201706/1116939-20170630161144399-677929583.jpg)