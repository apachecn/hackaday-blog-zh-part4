# Linux Fu:愚蠢的 SSH 技巧

> 原文：<https://hackaday.com/2019/12/17/linux-fu-stupid-ssh-tricks/>

如果您通过互联网连接到远程计算机，很可能会使用某种形式的 SSH 或安全 shell。在 Linux 或 Unix 上，您将使用`ssh`命令。Windows 上类似 Linux 的环境也是如此，比如 Cygwin 或 WSL。对于本机窗口，您可能会使用 Putty。最简单的形式是，`ssh`只是一个终端程序，它使用加密连接与服务器对话。我们认为很难窃听任何人通过`ssh`与远程计算机交流。

使用`ssh`有几个技巧——有些很简单，有些你可能想不到在终端程序的领域里。您可能知道`ssh`可以安全地复制文件，并且有简单和困难的方法来设置无密码登录。

然而，您也可以通过`ssh`挂载远程文件系统(实际上，有几种方法可以做到这一点)。您可以使用`ssh`在您最喜欢的浏览器中安全地浏览网页，甚至使用它通过端口传输特定流量，甚至将其用作临时 VPN。事实上，有太多的内容需要讨论，所以这不会是最后一个谈论`ssh`的 Linux Fu。不过，设置够了，让我们开始玩把戏吧。

## 几个不错的选择

我们假设你知道基本知识:`scp`和`sftp`用于文件拷贝，`ssh-copy-id`用于设置无密码登录。(如果没有，你有十分钟时间做一个快速网络搜索。)但是`ssh`最擅长的事情之一就是操控网络。但是请记住，服务器必须有特定的选项来做一些最有趣的事情，所以如果你不控制`ssh`服务器，这些技巧可能对你不起作用。

在`ssh`命令行上有很多选项需要记住，但幸运的是你不必这样做。你甚至不需要记住你的主机名或用户名。在`~/.ssh/config file`中你可以创建一个别名。例如，假设您想要连接到家庭服务器:

```

Host homeserver
  HostName mih0me.dyndns.org
  Port 1234
  User TheAl
  IdentityFile ~/.ssh/home_id
  ForwardX11 yes
  Compression yes
  TCPKeepAlive yes

```

你可以有很多别名。只要不断重复主机行，然后跟着它与选项。您还可以向单个 Host 语句添加多个别名。随后的选项将应用于任何别名。现在，连接只是问题`ssh homeserver`并且您拥有所有正确的选项。

当然，如果你正在使用 Putty，你的[选项](https://www.ssh.com/ssh/putty/putty-manuals/0.68/Chapter4.html)将主要在主机配置文件和选项屏幕的`ssh`面板上。你可能没有太多的选择，但有一些你可以尝试。

## 坚持不懈

一组非常好的选项包括设置主控制文件。例如:

```

ControlMaster auto
ControlPath ~/.ssh/master-%r@%h:%p

```

这使得同一个主机的多个会话共享一个 TCP 套接字。因为建立一个安全套接字需要一些时间，所以如果您在两台主机之间保持几个会话，这可以加快速度。您可以使用配置文件中的`Host *`行为所有主机设置它。您可以将它用于您可能有的任何全局选项。

另一方面，如果你通过多个连接传输大量数据，开启`ControlMaster`可能不是一个好主意。您可以添加`-S none`来覆盖全局设置。

另一件要注意的事情是，如果您试图在所有其他连接关闭之前退出，您的第一个`ssh`会话可能会挂起。有些人在登录到他们经常连接的主机时故意运行一个隐藏的`ssh`会话来避免这个问题。然而，更好的方法是将`ControlPersist`设置为是。这将导致原始会话无限期地转到后台。如果你想要一点宽限期，你可以设置`ControlPersist`为 180 这样的数字。如果三分钟内没有连接，这将导致后台会话结束。

这种方法的另一个缺点是，您可能会得到孤立的主文件。在`rc.local`中，我有下面一行:

```

/bin/rm /home/*/.ssh/master-* || true >/dev/null

```

使用 Putty，您可以单击 SSH 选项面板中的“如果可能，共享 SSH 连接”按钮。

## 配置

在配置文件中有很多[配置选项](http://man7.org/linux/man-pages/man5/ssh_config.5.html)可以使用。例如，`BatchMode`让你告诉`ssh`这个连接是无人值守的，所以不要麻烦提示用户输入密码或其他任何东西。当然，这并不是说它会让你进来。这只是意味着如果你没有设置无密码登录，它将会失败。

还有一些其他有趣的项目。例如，您可以在连接上运行本地或远程命令。您还可以向远程主机发送一个环境变量，甚至只设置一个。例如，假设您希望在工作站和服务器上始终保持 LS_COLORS 相同，但是您经常更改它们，并且不想使用相同的配置文件。您可以将它添加到主机的配置文件条目中:

```

SendEnv LS_COLORS

```

当然，服务器必须配置为接受这一点。Putty 可以处理从其设置中的 Data 选项卡设置环境变量。

在网络端，如果希望服务器和客户机在空闲期间测试它们的连接，可以将`TCPKeepAlive`指定为 yes。这是一把双刃剑。如果连接是空闲的，你不会被断开。但是，如果网络在适当的时候中断了一小段时间，你可能会断开连接，而如果你坚持使用默认设置，就不会断开连接。甚至有一种方法可以在机器之间打开第三层或第二层隧道——这是未来 Linux Fu 的一个主题。

## 遵照你的命令

不要忘记`ssh`可以执行一个命令，并将其输出发送给你。作为一个实际的例子，我偶尔会刷新我的 3D 打印机固件。打印机连接到一个 Raspberry Pi，但我在我的主机上做固件构建。在很长一段时间里，我将我的文件复制到 Pi(使用`scp`)，然后登录到 Pi 运行我写的一个名为`flash`的脚本。该脚本禁用 Reptier 服务器软件，刷新打印机控制板上的 Atmel 芯片，然后重新打开服务器。

这是在我的主计算机上运行的脚本。注意`ssh`命令。一个关闭服务器。一个`scp`命令复制新的固件。然后另一个`ssh`刷新并重命名服务器。当然，还有许多其他方法可以做到这一点。但是别忘了`ssh`可以运行一个远程命令然后返回。

```

#!/bin/bash
if [ -z "$1" ]
then
  echo Usage: flash hexfile [remote_name]
  echo If omitted, remote_name will have date attached
  exit 1
fi
ONAME="$2"
EXTRA=$(date "+%Y%m%d.%H%M")
if [ -z "$2" ]
then
  ONAME="$1-$EXTRA.hex"
fi
IP=192.168.1.110
  echo Stop Server
  ssh -l pi $IP "sudo systemctl stop RepetierServer"
  echo Copy...
  scp "$1" "pi@$IP:a8fw/$ONAME"
  echo Flashing...
ssh pi@$IP "cd a8fw; ./flash $ONAME"
echo Restart
ssh "pi@$IP" "sudo systemctl start RepetierServer"
echo Done
exit 0

```

如果您想要一个对黑客更友好的示例，可以考虑使用相同的方法在本地运行 Wireshark 并分析远程数据包捕获:

```

ssh root@someserver 'tcpdump -c 1000 -nn -w - not port 22' | wireshark -k -i -

```

如果你愿意，你可以用`tshark,`做同样的把戏。

## 速度测试

什么才能知道你的`ssh`连接有多快？确保您已经安装了`pv`,然后试试这个:

```

yes | pv | ssh remote_host "cat >/dev/null"

```

[![](img/aadf9dafeb90b2c14812adb511c5d2f1.png)](https://hackaday.com/wp-content/uploads/2019/10/speed.png)

相当酷！

如果你有好的速度——或者即使你没有——你可以尝试使用`sshfs`挂载一个远程文件系统。这是一个 FUSE 文件系统——也就是说，一个作为常规用户程序存在的文件系统，而不是内核的一部分。除了`ssh`服务器和标准工具之外，在远程端没有任何东西，您可以让任何您可以连接的主机看起来像一个本地文件系统。

## 但是等等…

您可以使用`ssh`做更多的事情，稍后我会介绍更多。但是现在，希望你找到了至少一个你可以使用的`ssh`技巧，如果不是新的，至少可以提醒你。