# Dell PowerEdge R720 系统安装
这里主要讲一些我在安装服务器的时候所碰到的一些问题及其解决方法<br>
机器到我手上的时候，就只有两台服务器，使用说明书、安装光盘什么都没有。这种情况只有先查一查资料了。查完以后发现所有的安装方法都是要通过dell服务器自带的一个[Lifrcycle Controller](http://www.dell.com/support/article/cn/zh/cndhs1/SLN287745/poweredge%E6%9C%8D%E5%8A%A1%E5%99%A8lifecycle-controller%E7%AE%80%E4%BB%8B?lang=ZH)(服务器生命周期控制器)。好吧，那就开机装系统，然而开完机器以后发现这两台机器不知道为什么都进不去LC。这就麻烦了，暂时还有光驱去刻录安装光盘。后来找到一个没有通过LC安装的大致流程。

## 一、建立raid

- 启动服务器，出现RAID Controller BOIS的时候提示你按ctrl+r，按下ctrl+r以后进入整列卡的BOIS，如果没有进入就多按几下。
- 选到raid卡，按F2选择Clear Config清除整列卡配置
- 再选到raid卡，按F2选择Create NewVD创建新的虚拟磁盘，我这边用了3块1T盘做raid5，如果有多的盘的话也可以做热备。
- 选到新建好的虚拟磁盘按F2，选择Initialzation里面的Start Init进行初始化。
- 初始化好后按Esc退出，Ctrl+Alt+Delete重启。

## 二、修改启动模式

- 开机后按F2进行BIOS设置，将启动模式改成UEFI启动，修改完成后重启机器。
- 开机后按F11进入Boot Manager进行UEFI启动,选择UEFI BootMenu插入光盘开始系统安装。

## 后记

折腾半天以后终于把两台服务器装好了，其实服务器这边只是比普通电脑多了配置阵列卡，其他部分和平时装电脑没有什么区别。LC的安装过程也主要就是这两个步骤，这边只是自己从底层配置好阵列卡和启动方式。说到LC，当我把系统装完以后，一台机器竟然神奇的进入了LC。一定是我一开始的打开方式不对_(:з」∠)_
