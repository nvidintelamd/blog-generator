---
title: MAC 终端命令行下用 sublime、vscode、atom 打开文件或目录
date: 2018-07-30 14:50:58
tags: MAC命令行
---
[转帖来自于这里](https://www.cnblogs.com/hongrunhui/p/5928833.html)
要知道，有时候一些小技巧，能极大的加大我们的工作效率。

在 MAC 下开发，用的最多的还是终端，我的终端环境是 iterm2+ohmyzsh；步入正题前先给大家介绍几个小技巧：

第一个：

打开 findle, 然后找到我的项目目录，然后我用安装好的 Go2shell 打开当前目录的终端。如下：

![](https://images2015.cnblogs.com/blog/726124/201610/726124-20161003093555785-1735168450.png)

说实话，很方便，总比先打开终端然后一步一步 cd 进去好多了。相信很多人都知道这个东西，不知道的自己搜名字去下载把。

第二个：

相信大家都会打开不止一个终端窗口，大家是不是这样做的：command+T 或者 comman+D, 前者是打开新窗口，就跟浏览器打开新标签一样，后者则是在当前窗口打开一个分屏窗口。

我们说说前面那个 comman+T, 打开心串口又会回到~ 根目录，然后又得不断 cd 进入到指定目录，其实 iterm2 有设置的：

打开 iterm2 终端，然后点左上角的 iterm2->Prefrences:

![](https://images2015.cnblogs.com/blog/726124/201610/726124-20161003095541692-1249420842.png)

然后只要把红框里那个选项勾上就行了。然后你在一个终端窗口 command+t 新建出来的窗口的目录就是当前目录了。

第三个：

在终端下怎么在 findle 中打开当前目录，这个只要输入 open . 就行了，记住，有一点。

好了，接下来步入正题：

1、在终端随便一个目录输入

<pre>cd</pre>

对，就一个 cd.

2、ls -al

![](https://images2015.cnblogs.com/blog/726124/201610/726124-20161003100116723-867735840.png)

然后看看当前目录有没有这个文件：

![](https://images2015.cnblogs.com/blog/726124/201610/726124-20161003100201489-1767376996.png)

这个是 zsh 的配置文件，我们就是要在这里配置：

3、

<pre>sudo nano .zshrc</pre>

在文件末尾加上：

<pre>alias atom='/Applications/Atom.app/Contents/MacOS/Atom'
alias subl='/Applications/SublimeText.app/Contents/SharedSupport/bin/subl'
alias code='/Applications/Visual\ Studio\ Code.app/Contents/Resources/app/bin/code'</pre>

 command+x 再输入 y, 保存。重启 iterm2.

![](https://images2015.cnblogs.com/blog/726124/201610/726124-20161003100436020-1360522937.png)

注意，上面的路径是我自己应用的路径，你们的可能会有变化。怎么找到路径：

![](https://images2015.cnblogs.com/blog/726124/201610/726124-20161003100649614-728418839.png)

然后

![](https://images2015.cnblogs.com/blog/726124/201610/726124-20161003100817410-141155794.png)

打开包内容后一直找到可以执行的文件（就是可以打开应用的文件），具体可以参考我的 zshrc 的设置。然后把当前路径复制到. zshrc 中用 alias 设置，alias 就是设置别名，有空格就用 \ 转义。

就这样，大功告成。然后看效果：

![](https://images2015.cnblogs.com/blog/726124/201610/726124-20161003101247973-1786489287.png)

![](https://images2015.cnblogs.com/blog/726124/201610/726124-20161003103418192-1554191494.png)

![](https://images2015.cnblogs.com/blog/726124/201610/726124-20161003103504817-74483477.png)

OK 了。赶紧试试吧。真的很方便。不懂欢迎评论问我。
