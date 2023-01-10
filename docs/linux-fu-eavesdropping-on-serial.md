# Linux 傅:窃听串口

> 原文：<https://hackaday.com/2022/09/07/linux-fu-eavesdropping-on-serial/>

在过去，如果你想窥探一个串行设备，你可能有一个串行监视器，或者，你的示波器或逻辑分析仪的附件。今天，你可以得到便宜的逻辑分析仪来完成这项工作，但是如果你想要一个纯软件的解决方案呢？最近，我需要在 USB 串行端口上做一些调试，当然，真的没有什么地方可以方便地连接监视器或逻辑分析仪。所以我开始寻找替代方案。

如果你还记得，在以前的 Linux Fu 中，我们讨论过[伪终端](https://hackaday.com/2022/05/03/linux-fu-the-infinite-serial-port/)，它看起来像串行端口，但实际上与一个软件对话。你可能会想:为什么不在串口和 pty 之间放一个监控软件呢？为什么不呢？那是一个如此好的主意，它已经被做了。当它工作的时候，它工作得很好。当然，唯一的问题是，它并不总是有效。

有问题的软件是[拦截](https://github.com/geoffmeyers/interceptty)。您可能必须从源代码构建它，但是没有任何奇怪的依赖关系。只是:

```
git clone https://github.com/geoffmeyers/interceptty.git
cd interceptty
./configure
make
sudo make install   # or however you like to install things like checkinstall, etc.
```

## 后端，前端

该软件使用后端设备和前端设备的概念。后端设备通常是普通的串行端口。前端设备是 interceptty 创建的。所以这个想法是，你把程序连接到后端，它创建前端，然后你把其他程序连接到前端。该程序将记录连接到前端的程序和后端端口之间的所有流量。

您还可以使用文件描述符、unix 套接字或 TCP 套接字作为前端或后端设备。后端也可以是正在运行的程序。还提供了两个实际端口之间的连接。您可以在该程序的手册页上找到所有选项。

输出有点笨拙，但是很容易被其他程序解析，包括附带的示例 Perl 程序。一个字符向你显示数据的方向，然后你看到一个十六进制和 ASCII 字符。

## 一个例子

可能更容易看到一个例子。我在`/dev/ttyACM0`上有一个小控制器。下面是一个命令行示例。

```
sudo interceptty /dev/ttyACM0 /dev/ttyCAP
```

这就产生了`/dev/ttyCAP`假端口。一旦程序连接上，你可以在左边看到它发送的数据，在右边看到响应(包括回应)。

```
< 0x3a (:) 
>       0x3a (:) 
< 0x78 (x) 
>       0x78 (x) 
< 0x38 (8) 
>       0x38 (8) 
< 0x79 (y) 
>       0x79 (y) 
< 0x38 (8) 
>       0x38 (8) 
< 0x69 (i) 
>       0x69 (i) 
< 0x31 (1) 
>       0x31 (1) 
< 0x30 (0) 
>       0x30 (0) 
< 0x21 (!) 
>       0x21 (!) 
< 0x0d ([CR]) 
>       0x06 ([ACK]) 
>       0x0d ([CR]) 
>       0x0a ([LF])

```

## 有问题的软件

不幸的是，并不是所有的软件都喜欢使用 pty。特别是，我想使用的主程序利用了 [Sigrok](https://hackaday.com/2018/09/14/easy-portable-serial-ports/) 串口库。这个库发出的调用不能很好地与 ptys 一起工作，这是一个已知的问题。然而，如果你使用任何普通的终端程序，如 picocom 或 [tio](https://hackaday.com/2022/07/13/tio-is-a-serial-terminal-for-us/) ，它都能正常工作。其他串行库似乎也能处理它。我想过试试 [slsnif](https://github.com/aeruder/slsnif) ，但它的工作方式是一样的，所以我怀疑它在这方面会有任何改进。

关于 Sigrok 库的另一个注意事项。内核中最近的变化已经删除了库使用的 ioctl，所以如果您使用的软件使用 libserialport，您将无法找到任何端口。在他们修复它之前，您必须自己构建库并修补 configure.ac 文件:

```
git clone git://sigrok.org/libserialport
cd libserialport
./autogen.sh
./configure
make
sudo make install
```

请确保您删除了旧版本的库，或者至少确保您的程序正在使用您的自定义库。

## 其他选项

如果你愿意，你可以试着把串口转换成网络接口，这样你就有很多监控选项了。当然，这也有类似的问题，因为不是所有的东西都理解你创建的假串口。不过，我可以报告说， [Tio](https://hackaday.com/2022/07/13/tio-is-a-serial-terminal-for-us/) 似乎表现良好，足以与这些 pty 假港口合作。

如果所有的串行软件都知道它们可能被调用来与 pty 或命名管道对话，那就好了。另一方面，你可能可以接触到恶意程序的源代码，所以如果你真的需要，你可以修复它们。