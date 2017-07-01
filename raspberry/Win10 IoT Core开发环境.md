# Windows 10 IoT Core开发环境
Windows 10 IoT Core开发语言主要使用C#，所以我们选择Visual Studio 2017作为主要开发环境。

## 一、确认操作系统
微软要求Windows 10 IoT Core的程序和开发环境只能在Windows 10上才能够开发和运行，所以开发之前请务必将你的操作系统升级到win 10。~~不要尝试在win7开发。~~

## 二、下载Visual Studio 2017
进入[Visual Studio](https://www.visualstudio.com/zh-hans/)官网，选择Visual Studio Community下载[安装文件](https://www.visualstudio.com/zh-hans/thank-you-downloading-visual-studio/?sku=Community&rel=15)。运行安装文件选择Visual Studio所需要的组件，主要有以下组件，其他组件根据自己需求进行添加。

![](http://images2015.cnblogs.com/blog/1116939/201706/1116939-20170630172121664-273701936.png)
组件选择完成后安装，等所有组件下载并安装完成后启动Visual Studio。

## 三、开发环境配置
打开Visual Studio后选择工具>扩展和更新

![](http://images2015.cnblogs.com/blog/1116939/201706/1116939-20170630180152618-407006656.png)
在联机中搜索iot后安装扩展组件。

![](http://images2015.cnblogs.com/blog/1116939/201706/1116939-20170630180346977-2014023558.png)

## 四、创建Win10 IoT程序
- 创建一个新的解决方案，模板选择空白应用（通用 Windowa）

![](http://images2015.cnblogs.com/blog/1116939/201706/1116939-20170630180740758-1070133032.png)

- 右键引用选择添加引用

![](http://images2015.cnblogs.com/blog/1116939/201706/1116939-20170630181302774-1171369059.png)

- 选择引用

![](http://images2015.cnblogs.com/blog/1116939/201707/1116939-20170701115144789-693314480.png)

这样以后就可以在程序中添加raspberry的引用
~~~
using Windows.Devices.Gpio;

GpioController gpio = GpioController.GetDefault();
GpioPin pin = = gpio.OpenPin(5);
pin.SetDriveMode(GpioPinDriveMode.Output);

pin.Write(GpioPinValue.Low);
pin.Write(GpioPinValue.High);
~~~

## 五、调试程序
程序完成后我们往往需要进行调试，raspberry的程序和win10程序都是相通的，在没有引脚接口的的程序完全可以在本地计算机进行调试，对于需要引脚的调试程序需要调用远程计算机进行调试。

- 右键项目，属性选择调试。平台选择ARM，目标选择远程计算机。身份验证选择通用，点击查找以后如果raspberry和计算机在同一局域网内，就可以找到在线的树莓派。调试以后就会把整个程序打包发送到树莓派上进行调试

![](http://images2015.cnblogs.com/blog/1116939/201707/1116939-20170701123307086-1706296358.png)