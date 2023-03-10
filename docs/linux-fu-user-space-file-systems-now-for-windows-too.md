# Linux Fu:用户空间文件系统——现在也适用于 Windows！

> 原文：<https://hackaday.com/2021/08/31/linux-fu-user-space-file-systems-now-for-windows-too/>

Linux 继承的 Unix 哲学的一个优点是文件系统非常模块化。这也很好，因为一个典型的系统可能需要选择像`ext4`、`reiserfs`、`btrfs`这样的文件系统，甚至像`nfs`这样的网络系统。除此之外，还有像`/sys`和`/dev`这样的假文件系统，它们帮助 Linux 让一切看起来像一个文件。缺点是构建文件系统需要改变内核，或者至少编写一个可加载的模块。这并不像听起来那么难，但是比写一个普通的程序要难一点。然后是 [FUSE](https://hackaday.com/2018/03/16/linux-fu-file-aliases-links-and-mappings/) —用户空间的文件系统。这是一个单一的文件系统模块，允许您通过编写普通代码来创建新的文件系统。

## 我最喜欢的保险丝

有几个真正有用的 FUSE 文件系统。以下是我最喜欢的一些:

*   [ssh fs](https://hackaday.com/2019/12/17/linux-fu-stupid-ssh-tricks/)–只使用 ssh 访问来挂载远程文件系统
*   [r clone](https://hackaday.com/2020/11/10/linux-fu-send-in-the-cloud-clones/)–r clone 可以访问和挂载许多远程文件系统
*   [tag assistant](http://www.tagsistant.net)–以独特的标签访问方式存储文件
*   [fuse-zip](https://linux.die.net/man/1/fuse-zip)–挂载 zip 文件
*   gitfs–用 git 挂载

还有很多[其他的](https://en.wikipedia.org/wiki/Filesystem_in_Userspace)。你可以找到与之合作的系统，例如 NTFS 和一系列云服务提供商。

## Windows 呢？

如果这是一个伟大的想法，有没有一个 Windows 的等价物？是的，有。Winfsp 看起来是在 Windows 下获得相同效果的一个很好的方法，尽管它不仅仅是即插即用地与 FUSE 兼容。有一个 FUSE 兼容性包装器，可以让您更容易地移植现有的 FUSE 代码。事实上，有两个 FUSE 包装器，一个用于 2.8 版本，另一个用于 3.2 版本。

这是一个较新的项目，但也有 [Dokan](https://github.com/dokan-dev/dokany/) 也声称他们的 API 有一个 FUSE 包装器。根据`Winfsp`提供的基准，`Winfsp`表现更好。

## 那又怎样？

如果你有一个喜欢的 FUSE 系统，它可能是开源的，如果你愿意，你可以试着把它移植到 Windows 上。如果你不使用 Windows，并且你想要写你自己的 FUSE 系统，这些系统提供你一种可能容易地把你的工作转移到 Windows 的方法。

例如，您可能有一个数据记录器，并希望将其数据公开为文件系统。这并不难做到。有一个数据结构需要填写，你不必全部填写。您提供数据结构指向的函数，这些函数读取和写入目录和文件数据等内容。这里有一个 C 中的[例子。或者试试](https://www.maastaar.net/fuse/linux/filesystem/c/2016/05/21/writing-a-simple-filesystem-using-fuse/)[一个 C++包装器](https://github.com/jachappell/Fusepp)，它能让你用更少的代码行写一个。这个例子只有四个简单的函数。