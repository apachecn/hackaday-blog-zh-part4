# 黑我的房子:不带 SD 卡运行树莓派

> 原文：<https://hackaday.com/2018/10/08/hack-my-house-running-raspberry-pi-without-an-sd-card/>

我们很多人都经历过 SD 卡损坏的痛苦。我怀疑闪存的写时擦除特性是问题的主要原因。不管是什么原因，一个解决方案是使用 PXE 引导树莓 Pi 3。这是说我们将通过网络启动 Raspberry Pi，而不是从 SD 卡启动的一种奇特方式。

这和黑我家有什么关系？正如我上次讨论过的，我正在使用 [Raspberry Pi 作为基础设施](https://hackaday.com/2018/09/26/hack-my-house-raspberry-pi-as-infrastructure/)，将它们构建到我家里每个房间的墙上。你不希望拖出一个梯子和螺丝刀来换出一个行为不端的 SD 卡，所以通过网络启动是一个非常好的解决方案。我知道我答应过我们会讨论布线和摄像头。请将此视为一篇附带说明的文章——我们将在下次讨论以太网和 ZoneMinder。

所以让我们深入了解一下预启动执行环境(PXE)是什么，以及如何将 PXE 与 Raspberry Pi 结合使用。

## 熟悉 Raspberry Pi 的 PXE 启动功能

![](img/56dd78ef80c3f30ca1f6551c996a640e.png)新的 Raspberry Pis 支持 PXE 启动，允许 Pi 从同一网络上的服务器加载其文件系统。我的经验是，Pi 3 型号 B+比旧版本启动更可靠。无论哪种方式，从运行 rpi-update 开始都是一个好主意。此外，您可能需要通过在 config.txt 中添加一个选项，从 SD 卡启动一次来手动启用 PXE。[官方报道](https://www.raspberrypi.org/documentation/hardware/raspberrypi/bootmodes/net_tutorial.md)是一个很好的指南，也是我第一次浏览 PXE 过程时使用的资源之一。然而，我会做一些不同的事情。

花点时间考虑一下您的网络布局。你的 Raspberry Pi 会连接到你现有的网络，还是一个新的专用网络？要使用您的主网络，您的路由器必须支持自定义 DHCP 选项。OpenWrt 路由器或类似设备有这种能力，但普通的 D-Link 或 Linksys 可能没有。

您需要在家庭网络上安装一台服务器，为 PXE Pis 提供文件系统。有多种方法，我将使用 CentOS 7。硬件可以是一个旧的桌面，一个虚拟机，甚至是另一个 Raspberry Pi。我们假设一台服务器有两个接口——一个连接到您的主网络，另一个静态 IP 为 192.168.2.1，专用于 Raspberry Pi 网络。(如果您计划使用单个网络，请跳过下面的 dnsmasq 步骤，使用服务器现有的 ip 地址，而不是 192.168.2.1。)

## 内务整理和准备

下面的代码块负责初始依赖项和防火墙设置，并启用所需的服务。在服务器上，我们需要三个主要服务:Dnsmasq 用于 DHCP，nfs-utils 用于 nfs，tftp-server 用于 tftp。Xinetd 是 tftp-server 的辅助服务，我们需要 unzip 和 wget 来下载和提取 Raspbian 磁盘映像。

安装您最喜欢的文本编辑器(我用的是 nano)和 policycoreutils 包，以便与 SELinux 一起工作。然后，允许服务通过防火墙，并设置它们在启动时自动运行。最后，在这段指令中，我们将 SELinux 设置为一个关于 TFTP 服务的更宽松的姿态。

```
sudo yum install -y dnsmasq tftp-server nfs-utils xinetd unzip wget nano policycoreutils-python
sudo firewall-cmd --permanent --add-service nfs3
sudo firewall-cmd --permanent --add-service mountd
sudo firewall-cmd --permanent --add-service rpc-bind
sudo firewall-cmd --permanent --add-service tftp
sudo firewall-cmd --permanent --add-service dhcp
sudo systemctl enable xinetd
sudo systemctl enable dnsmasq
sudo systemctl enable rpcbind
sudo systemctl enable nfs-server
sudo setsebool -P tftp_home_dir 1
```

设置目录结构和一对临时挂载点，然后下载并提取最新的 Raspbian 映像。

```
sudo mkdir /tftpboot
sudo mkdir -p /nfs/raspi1
mkdir ~/bootmnt
mkdir ~/rootmnt
wget http://director.downloads.raspberrypi.org/raspbian_liimg/raspbian_lite-2018-06-29/2018-06-27-raspbian-stretch-lite.zip
unzip 2018-06-27-raspbian-stretch-lite.zip
```

用 PXE 启动从 DHCP 选项 66 开始(不是 66 号指令，那是不同的东西)，它指向 TFTP 服务器。我们将配置 dnsmasq 来添加该选项，以及监听接口和 IP 地址范围。根据您的情况适当地更改这些值，并添加到/etc/dnsmasq.conf。

```
interface=ens9
dhcp-range=192.168.2.50,192.168.2.150,12h
dhcp-option=66,192.168.2.1
```

NFS 的配置很简单。我们通过编辑/etc/exports 来指定想要导出的目录。

```
/nfs/raspi1 *(rw,sync,no_subtree_check,no_root_squash)
```

Xinetd 代表“扩展的互联网守护进程”这个服务控制着其他几个服务，包括 TFTP。我们将在/etc/xinetd.d/tftp 中配置 xinetd 的配置文件，查找行“server_args”和“disable”。我们添加了两个“-v”标志来增加详细程度，因为我们需要查看 Raspberry Pi 在启动时正在寻找什么文件。

```
server_args = -v -v -s /tftpboot
disable = no
```

## 构建 Pi 的引导映像

Kpartx 是放在 Linux-fu 工具箱中的一个非常有价值的工具。我们将使用它来挂载这个磁盘映像中包含的分区，然后将文件系统复制到新的 PXE 根目录。Pi 首先查找 bootcode.bin，因此我们也将该文件复制到适当的位置。

```
sudo kpartx -a -v 2018-06-27-raspbian-stretch-lite.img
sudo mount /dev/mapper/loop0p2 ~/rootmnt/
sudo mount /dev/mapper/loop0p1 ~/bootmnt/
sudo cp -a ~/rootmnt/* /nfs/raspi1
sudo cp -a ~/bootmnt/* /nfs/raspi1/boot/
sudo cp -a /nfs/raspi1/boot/bootcode.bin /tftpboot/
```

我们还可以为 Pi 定制文件系统。首先，启用 ssh 访问。

```
sudo touch /nfs/raspi1/boot/ssh
```

接下来，我们将修改内核引导行，位于/nfs/raspi1/boot/cmdline.txt。这里我们通知内核，它不应该在本地磁盘上查找文件系统，而是挂载一个 nfs 共享作为其根目录。

```
dwc_otg.lpm_enable=0 console=serial0,115200 console=tty1 root=/dev/nfs nfsroot=192.168.2.1:/nfs/raspi1,udp,v3 rw ip=dhcp rootwait elevator=deadline rootfstype=nfs
```

最后，我们从 Pi 的 fstab 中删除了几行，这样它就不会试图从不存在的 SD 卡上挂载文件系统。编辑/nfs/raspi1/etc/fstab 并删除最后两行，这两行安装了`/`和`/boot`。

## 网络侦查和绑定挂载

在这一点上，我们准备看看我们的努力是否有回报。重新启动服务器，以便应用挂起的更改。(是的，手动应用它们相当容易，不需要重新启动，但是这一步也测试了断电时一切都恢复正常。)一旦恢复，在给连接到新网络的 Pi 供电的同时，观察系统日志。(Al Williams 刚刚发表了一篇关于尾巴命令多功能性的文章，值得一看。)

```
$ sudo tail -f /var/log/messages
Sep 24 11:05:15 PXE xinetd[1043]: START: tftp pid=4824 from=192.168.2.103
Sep 24 11:05:15 PXE in.tftpd[4825]: RRQ from 192.168.2.103 filename bootcode.bin
Sep 24 11:05:15 PXE in.tftpd[4825]: Client 192.168.2.103 finished bootcode.bin
Sep 24 11:05:15 PXE in.tftpd[4826]: RRQ from 192.168.2.103 filename bootsig.bin
Sep 24 11:05:15 PXE in.tftpd[4826]: Client 192.168.2.103 File not found bootsig.bin
Sep 24 11:05:15 PXE in.tftpd[4826]: sending NAK (1, File not found) to 192.168.2.103
Sep 24 11:05:15 PXE in.tftpd[4827]: RRQ from 192.168.2.103 filename 57b3548e/start.elf
```

日期会有所不同,“PXE ”(该服务器的主机名)也会不同。你正在从一个 IP 地址寻找 RRQ。如果出现了，那么一切都很好。如果没有，就该进行一些故障排除了。

您可能会注意到您的 Pi 实际上并没有启动。那是因为我们还没有完成。回头看看 TFTP 日志行，因为我们需要您的 Pi 正在寻找的文件夹名，这恰好是它的序列号。在 tftpboot 文件夹中创建该文件夹。用日志中的文件夹名称替换 57b354e。

```
sudo mkdir /tftpboot/57b3548e
```

我们需要讨论绑定挂载，以及为什么我们不只是将文件复制到这个文件夹中。Raspbian 有一个内置的程序来更新内核，通过 apt-get。PXE 转移存储在 TFTP 文件夹中的内核，而系统的其余部分作为 NFS 共享挂载。这种安排防止 Pi 更新它自己的内核。有几种方法可以解决这个问题，但是今天我们使用绑定挂载。可以把它看作是目录的硬链接。我们将在服务器的/etc/fstab 中添加一行，再次使用 Pi 的序列号作为文件夹名称。

```
/nfs/raspi1/boot /tftpboot/57b3548e none defaults,bind 0 0
```

然后使用 mount 命令激活绑定挂载。

```
sudo mount /tftpboot/57b3548e
```

现在，对 Pi 进行电源循环，它应该可以运行了！

## PXE 和圆周率的力量

Raspberry Pi 系统的头号问题是 SD 卡问题。通过网络引导可以避开这个弱点(假设您的网络和服务器都是稳定的系统)。对我来说，这是一个完美的选择，因为我计划在一个三端口电气盒中使用 Raspberry Pi，通过以太网连接并使用以太网供电。也就是说，任何有以太网连接的应用，以及需要你的 Raspberry Pi 长期可靠的应用，都是 PXE 的好选择。

我们将何去何从？下次我们将设置 Zoneminder，并最终使用这些 pi。让我们知道你还想看什么，或者这次我们错过了什么。在那之前，祝你黑客生涯愉快！