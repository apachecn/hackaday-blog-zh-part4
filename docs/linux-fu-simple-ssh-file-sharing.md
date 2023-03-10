# Linux Fu:简单的 SSH 文件共享

> 原文：<https://hackaday.com/2020/09/21/linux-fu-simple-ssh-file-sharing/>

如果你有不止一台 Linux 电脑，你可能会一直使用`ssh`。这是一个很棒的工具，但是我总是发现它有一点很奇怪。尽管有以`scp`和`sftp`形式的文件传输能力，但是如果不在本地机器上启动一个新程序或者从远程机器登录回本地机器，就没有办法在本地和远程主机之间来回移动文件。

最后一点是一个真正的问题，因为你经常用一个短暂的 IP 地址从防火墙或 NAT 路由器后面访问服务器，所以它无论如何都不能重新连接到你。点击 escape 字符，选择一个本地或远程文件，并通过界面传送它，所有这些都是在一个单独的`ssh`会话中完成的，这将是一件很好的事情。

我没有完全达到那个目标，但是我已经非常接近了。我将向您展示一个可以在本地机器上自动挂载远程目录的脚本。您需要在本地机器上安装`sshfs`,但是不需要在远程机器上进行修改，因为在远程机器上您可能无法安装软件。再做一点工作，如果您的客户机运行着一个`ssh`服务器，您也可以在远程机器上挂载一个本地目录。你不需要担心你的 IP 地址或端口阻塞。如果您可以登录到远程机器，那就很好。

结合起来，这让我非常接近我的目标。我可以在任何一方的 shell 中工作，也可以在另一方读取或写入文件。我只需要小心地设置它。

## 等等…那是作弊吗？

您可能会说这是欺骗，因为您实际上使用了两个`ssh`连接——一个用于文件系统挂载，另一个用于登录。确实如此。然而，如果您正确设置了`ssh`,您将只需认证一次，并且不会像两个单独的连接那样有太多的开销。

此外，该脚本隐藏了详细信息，因此从用户的角度来看，您的连接(几乎)与平常一样，并且可以正常工作。

## 关于 SSHFS

`sshfs`程序是一个用户空间文件系统(FUSE)，这意味着它是底层文件系统之上的一个用户空间层。在这种情况下，底层文件系统是一个能够执行`sftp`的`ssh`服务器。这允许您访问远程机器上的文件，就像它在本地机器上的真实文件系统上一样。如果没用过的话，还是挺好用的。

如果您为机器`myserver`设置了一个登录，您只需从本地机器运行`sshfs myserver:/home/admin ~/mounts/myserver`。

现在，远程机器上的`/home/admin`目录将出现在本地机器上的`~/mounts/myserver`处。

您可以使用一些选项。例如，允许文件系统重新连接断开的连接是很有用的。请阅读手册页了解更多信息。

因为`sshfs`使用文件的远程挂载版本，所以所有的修改都显示在远程机器上，但是一旦你关闭了`sshfs`,你在本地机器上什么也得不到。让我们解决这个问题。

## 在剧本之前

在我进入脚本之前，如果您愿意，可以在客户端上进行一些设置。我创建一个目录`~/remote`，然后为我的每台远程计算机创建一个子目录。比如`~/remote/fileserver`和`~/remote/lab`。

这个脚本名为`sshmount`，它采用与`ssh`相同的参数。为了方便起见，您应该在远程主机的`~/.ssh/config`文件中保存您的详细信息，这样您就可以使用一个简单的名称。例如，`lab`可能是这样的:

```

Host lab
Hostname lab.wd5gnr-dyn.net
Port 444
User alw
ForwardX11 yes
ForwardX11Trusted yes
TCPKeepAlive yes
Compression yes
ControlMaster auto
ControlPath ~/.ssh/master-%r@%h:%p

```

这并不是绝对必要的，但是你会得到一个很好的`~/remote/lab`目录，而不是使用起来很烦人的`~/remote/alw@lab.wd5gnr-dyn.net:444`。这些参数并没有什么神奇之处，但是`ControlMaster`和`ControlPath`确实使多重连接更加经济，这在这种情况下很重要。

如果您还没有使用证书来设置自动登录，您也需要这样做。我们为覆盆子 P i 做了一个关于这个的帖子，但是它真的适用于任何设置。

## 剧本

这个剧本有分裂的个性。如果您通过一个到`sshunmount`的链接调用它，它将卸载与指定的远程主机相关联的目录。如果你以别的方式调用它(通常是`sshmount`)，它会做三件事:

1.  它在`~/remote`下检查与远程主机名匹配的目录(例如`lab`)。如果没有找到，它会打印一条错误信息并继续执行`ssh`。
2.  如果该目录存在，脚本将检查已挂载文件系统的列表，查看它是否已经挂载。如果是，脚本就继续执行`ssh`。
3.  如果目录没有挂载，脚本调用`sshfs`，然后继续执行`ssh`。

你可以在 [GitHub](https://github.com/wd5gnr/sshmount) 上找到脚本，不过这里是它的要点(少了一些评论)；

```

#!/bin/bash

if [ "$1" == "" ]
then
echo Usage: sshmount host [ssh_options] - Mount remote home folder on ~/remote/host and log in
echo or: sshunmount host - Remove mount from ~/remote/host
exit 1
fi

# if called as sshunmount...
if [ $(basename "$0") == sshunmount ]
then
echo Unmounting... 1&gt;&amp;2
fusermount -u "$HOME/remote/$1"
exit $?
fi

# normal call...
if [ -d "$HOME/remote/$1" ] # does directory exist?
then
if mount | grep "$HOME/remote/$1 " # already mounted?
then
echo Already mounted 1&gt;&amp;2
else
sshfs -o reconnect $1: $HOME/remote/$1 # mount
fi
else
echo No remote directory ~/remote/$1 exists 1&gt;&amp;2
fi
ssh $@ # do log in

```

这给了我们我想要的一半。当我登录到系统时，我的本地机器有一个远程文件系统的直接映射。但是将本地目录映射到远程机器有点困难。

## 逆转过程

如果您想尝试在服务器上安装一个本地目录，那么您也可以在本地机器上运行一个`ssh`服务器。当然，如果您的本地机器对主机是可见的并且是可访问的，那就无关紧要了。只需在远程机器上运行`sshfs`并从本地机器挂载一个目录。但是在许多情况下，您将没有从远程机器通过任何防火墙和路由器的可访问路径，特别是在像笔记本电脑这样不在一个地方的东西上。

尽管如此，还是有一个答案。这需要两件事。首先，您需要在调用`sshmount`时添加一个额外的参数(如果您想一直这样做，您可以编辑文件):

```

sshmount MyServer -R 5555:localhost:22

```

然后在主机上运行

```

sshfs -p 5555 localhost:/home/me ~/local

```

R 选项在远程机器上的 5555 处创建一个套接字(很明显，这个套接字在其他情况下不会被使用),并在端口 22 上将其映射回我们。假设在端口 22 上有一个`ssh`服务器，这将允许服务器通过相同的连接登录回我们的本地机器。不需要知道我们的 IP 地址或有一个开放的端口。

可以放在启动文件中的`sshfs`命令将本地的`/home/me`目录映射到远程服务器的`~/local`目录。如果你也本地登录，有几个`SSH_ environment`变量可以用来判断你是否远程启动，例如`$SSH_CLIENT`或`$SSH_TTY`。

当然，您需要更改主机、目录和端口号以适应您的环境。但是一旦设置好了，你就可以让两台机器上的文件夹互相可见。不，我没有尝试过循环挂载相同的目录。这可能会产生黑洞。

## 在外面要小心

你可能还是应该小心两个方向。例如，扫描整个文件系统的工具很容易混淆。我也希望我有一个更好的答案，当你注销最后一个会话时，干净地断开服务器的文件共享。

然而，目前来看，系统运行良好，这是一种简单的方式，无需太多工作就可以在`ssh`会话中共享文件。另一个答案可能是保持[目录同步](https://hackaday.com/2020/07/23/linux-fu-keep-in-sync/)，并使用这些目录进行传输。想要更多愚蠢的`ssh`招数？我们[得到了他们](https://hackaday.com/2019/12/17/linux-fu-stupid-ssh-tricks/)。