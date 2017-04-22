# Markdown 语言的学习

首先这是第一次接触Markdown这类轻量级的标记语言。初步学习了一下觉得这种语言能够很好的排版，解决了平时写东西时缩进、字体大小、符号等等问题。

## Markdown的准备工作

> 关于Markdown的语言工具，我直接选择[Visual Studio Code](http://code.visualstudio.com/)，至于其他的工具并没有进行尝试。目前VS Code感觉还不错，主要是VS Code的git功能还算好用，其他工具的git功能现在还不明确，以后有时间的话会去试试其他工具。

## Markdown的书写

>这边主要参考了部分老师给出的文档，并没有碰到什么太大的问题。

## Markdown上传到Github

> 之前上传代码的都是使用eclipse和IDEA的内置的插件，所以对于如何使用git命令上传文件就一头雾水。然后发现VS Code其实也是内置了git，只是相对于IDEA和eclipse稍微麻烦一点。这里我主要参考了[玄魂的 Visual Studio Code 使用Git进行版本控制](http://www.cnblogs.com/xuanhun/p/6019038.html?utm_source=tuicool&utm_medium=referral)。
- 在操作的时候发现目前VS Code发生了细微的变化：在新打开文件架后点击git按钮后出现的不是初始化GIT储存库，而是要点击右上角的git图标。
- 另外在每次push新的工程时都要去工程的根目录执行两个命令，还是有一点麻烦的。
```
git remote add origin https://github.com/xxx/xxx.git
git pull origin master
```
- 后来发现了一个VS Code的插件Git Easy，增加了VS Code中自带的git操作。可以直接在扩展中搜索安装，安装后按F1调出控制台。输入git remote 就可以直接使用命令，然后按照要求驶入名称和url就可以在VS Code中完成。
- 最后在git中选择发布就可以将文件push到Github。


## 后记

> 在查找部分资料的时候发现很多人都不太喜欢VS Code的界面，有很多关于Markdown的优化文章。以后可以尝试以下,卡里斯玛的[用VS Code打造最佳Markdown编辑器](http://www.jianshu.com/p/18876655b452)。

> 其实这篇文章写好的时候任务5的主要任务并没有完成，待会后在后面补充上简历的地址。




