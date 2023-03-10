# Linux Fu:简单的虚拟机

> 原文：<https://hackaday.com/2022/11/01/linux-fu-easy-vms/>

不久前，我们还在考虑从命令行轻松创建 Docker 容器，这样您就可以轻松地构建一个虚拟开发环境。如果你能为虚拟机做同样的事情，那不是很好吗？你可以。使用 Ubuntu 制造商 Canonical 的 [Multipass](https://multipass.run) ，你可以在 Linux、Mac 或 Windows 下轻松启动虚拟机。诚然，大多数虚拟机都是 Ubuntu 的变体，但是还有一些额外的镜像可用，您可以创建自己的镜像。

一旦你安装了它，启动一个新的 Ubuntu 实例是很简单的。如果您有一个设置配置，您甚至可以使用 YAML 文件设置预定义的设置。

## 装置

该过程因平台而异，但在 Ubuntu 上，安装 Multipass 非常简单:

```
sudo snap install multipass
```

您应该确保您所在的计算机支持虚拟机。`/proc/cpuinfo`文件应该有一个`vmx`或者`svm`标志(实际上是几个；每个内核一个)。

## 目录

您可以通过运行以下命令来查看所有可用的图像:

```
multipass find
```

当然，大多数图像都是 Ubuntu 版本，尽管也有一些其他设备，如 anbox 和 nextcloud。

假设您想在 Ubuntu bionic (18.04)实例中进行一些测试。您可以通过发出以下命令来启动默认实例:

```
multipass launch bionic
```

然而，您通常希望有更多的控制，因为默认情况下是一个 CPU 内核、1gb 的 RAM 和 5G 的磁盘存储。假设您想要 4 个 CPU、6G 内存和 10G 磁盘。您还可以为虚拟机提供一个名称:

```
multipass launch -c 4 -m 6G -d 10G -n hackaday-vm bionic
```

## 逃亡中

一旦您有了一组虚拟机，您可能想要了解它们的运行情况:

```
multipass list
```

你可以用开始和停止来控制它们。您也可以删除机器。

```
multipass stop hackaday-vm
multipass start hackday-vm
multipass stop hackaday-vm
multipass delete hackaday-vm
```

## 接近

那你用它做什么？默认情况下，机器通过只能从主机访问的专用网络启动。如果你需要的话，有很多方法可以路由流量。

但是，很多时候你只是想给新机加个壳。这很简单:

```
multipass shell hackaday-vm
```

如果您想要共享数据，可以将主机文件夹装载到虚拟机中:

```
multipass mount ~/hackaday hackaday-vm
```

如果您忘记了所有的事情，您可以询问特定的机器:

```
multipass info hackaday-vm

Name:           hackaday-vm 
State:          Running 
IPv4:           10.134.147.131 
Release:        Ubuntu 18.04.6 LTS 
Image hash:     5269cad5bc26 (Ubuntu 18.04 LTS) 
Load:           0.78 0.41 0.16 
Disk usage:     1.2G out of 9.5G 
Memory usage:   143.2M out of 5.8G 
Mounts:         /home/alw/hackaday => /home/alw/hackaday 
                   UID map: 0:default 
                   GID map: 0:default

```

真的就这么简单。还有其他[命令](https://multipass.run/docs/multipass-cli-commands)可用于在机器上运行程序或建立网络。在你的系统托盘中也有一个 GUI，但是如果你不是作为你自己的用户运行虚拟机，那对你来说就没什么用了。

## 配置

如果你总是需要设置一些东西，你可以自动设置。您创建一个 yaml 文件(称为[云初始化文件](https://cloudinit.readthedocs.io/en/latest/topics/tutorial.html))并设置用户、包、ssh 密钥等等。注意，该标准允许多种格式，但是显然 Multipass 只支持 YAML。

你可以做的另一件事是使用 Packer 来打包你自己的新图像。这有点复杂，但是您可以[阅读文档来了解如何](https://multipass.run/docs/building-multipass-images-with-packer)。

你是否曾经建立了一个开发环境，然后几年后发现它因为更新而崩溃了？有了虚拟机，这种事情再也不会发生了。您可以归档整个环境。在生产环境中，当您需要回到构建代码的确切方式来解决问题时，这可能很重要。这对于安全关键软件来说也是非常重要的，有时你需要能够产生完全相同的可执行文件，并证明你能做到。虚拟机使这变得更加容易，Multipass 是一种创建和使用至少某些类型的虚拟机的简单方法。它可以在多个平台上运行，这本身也是一个很大的特点。