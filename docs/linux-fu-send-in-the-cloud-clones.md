# Linux Fu:发送(云)克隆

> 原文：<https://hackaday.com/2020/11/10/linux-fu-send-in-the-cloud-clones/>

将数据存储在“云中”——即使它是你自己的服务器——非常流行。但是许多云解决方案要求你使用网页浏览器笨拙地访问你的文件。有一天，操作系统将像任何其他文件系统一样包含通用云存储。但是通过使用两个工具， [rclone](https://github.com/rclone/rclone) 和`sshfs`，你几乎可以用一点点一次性的设置来完成这个任务。有一些限制，但是，一般来说，它工作得很好。

这是一个和计算机一样古老的故事。有新的东西。使用它是奇特的，需要特殊的技术。然后它就变成了操作系统的另一部分。如果你追溯得够远，程序员必须从磁带、鼓或磁盘等海量存储中提取特定的记录，并对数据进行解块。现在你只需打开一个文件或一个数据库。相机、打印机、音频甚至网络曾经是特殊的设备，现在却变得很普通。例如，如果您使用 Windows，OneDrive 会得到很好的支持。但是，如果您使用另一种服务，您可能有也可能没有一个简单的选项，只将您的文件作为一级文件系统来访问。

`rclone`计划是云存储服务的瑞士军刀。尽管名不副实，但它并不需要将本地文件存储同步到远程服务，尽管它可以做到这一点。该程序与令人眼花缭乱的云存储提供商合作，它可以进行简单的操作，如列出和复制文件。如你所料，它也可以同步。但是，它也有一个实验性的 FUSE 文件系统，允许您挂载远程服务——并获得不同程度的成功。

## 支持什么？

如果你不喜欢使用谷歌或亚马逊这样的人，你可以托管自己的云。在这种情况下，您可以使用`sshfs`来挂载一个使用`ssh`的文件，尽管`rclone`也可以这样做。也有像 OwnCloud 和 NextCloud 这样可以自己托管的云服务。运行 Raspberry Pi 的 Docker 可以在几分钟内轻松完成其中一个，rclone 也可以处理这些。

该项目声称支持 [33 种类型的系统](https://rclone.org/overview/)，虽然其中一些是服务于本地文件的，但无论如何，至少有 30 种。像谷歌、Box、Dropbox 和亚马逊这样的大玩家都在那里。Google Drive 和 Google Photos 有不同的版本。有些协议是通用的，如 SFTP、HTTP 和 WebDAV，因此它们可以与多个提供者一起工作。还有一些不太为人所知的名字，比如 Tardigrade、Mega 和 Hubric。

当然，每个系统都有自己的特质。有些文件系统区分大小写，有些则不区分。有的支持修改时间记录，有的不支持。有些是只读的，有些不支持重复文件。您可以挂载大多数文件系统，也有元系统可以显示来自多个远程设备的文件(例如，Google Drive 和 Dropbox 一起)，还有其他特殊的系统可以缓存另一个远程设备或拆分大文件。

## 它是如何工作的？

当您设置`rclone`时，您使用该程序来配置一个或多个遥控器。程序将设置存储在~/中。尽管您很少需要编辑该文件。相反，你运行`rclone config`。

从那里你可以看到任何你已经拥有的遥控器并编辑它们，或者你可以定义新的。每个后端提供者都有稍微不同的设置，但是您通常必须提供某种登录凭证。在许多情况下，该程序会启动一个 Web 浏览器来验证您的身份，或者允许您授予`rclone`访问该服务的权限。

一旦你有了遥控器，你就可以用`rclone`来使用它。假设您有一个 Google Drive，并且您制作了一个名为 HaDFiles 的遥控器:它指向那个驱动器。您可以使用如下命令:

```
rclone ls HaDFiles:
rclone ls HaDFiles:/pending_files    # directory name, not file wildcard!
rclone copy ~/myfile.txt HaDFiles:/notes/myfile.txt
rclone copy HaDFiles:/notes/myfile.txt ~/myfile.txt
rclone sync ~/schedule HaDFiles:/schedules
```

复制更像是同步。文件从一个路径复制到另一个路径。您不能复制目录。换句话说，考虑这个命令:

```
rclone copy /A/B/C/d.txt remote:/X/Y/Z
```

这会将`d.txt`从`/A/B/C`复制到`/X/Y/Z`。If 不会复制另一端已经存在的文件，除非它的哈希值与新文件不同，这表明文件已更改。还有一个移动命令，以及`delete`、`mkdir`、`rmdir`和所有其他你会想到的东西。`sync`命令更新目的地以匹配源，而不是相反。

然而，我们感兴趣的是 mount 命令。从表面上看，这很简单:

```
rclone mount remote:/ /some_local_mount_point
```

## 警告

不过，还是有一些问题。首先，一些文件系统的性能很差，如果您的连接速度很慢，甚至会更差。如果您有像文件索引程序(例如，`baloo`)或遍历整个文件系统的备份程序这样的工具，这就特别糟糕。最好的办法是从那些程序中排除这些挂载点。

访问远程文件系统可能效率低下，因此`rclone`将在短时间内缓存文件属性。如果文件在远程端发生了更改，您可能会得到陈旧的数据，这对您的数据可能是不利的。它还缓存目录，所以如果您对多个用户使用它，请务必阅读文档。

默认情况下，您也不能随机写入文件。这使得一些程序如文字处理器无法工作。您可以给`--vfs-cache-mode`传递一个参数，让`rclone`在本地缓存文件，这可能会有所帮助。然而，没有免费的午餐。如果你将缓存模式设置为满，所有的文件操作都可以进行，但是你冒着`rclone`不能将整个文件转移到远程的风险，这同样不利于你的数据完整性。

## 问题

如果你不介意手动设置的话，真的就是这么简单。运行一个`mount`命令，大概指定一个缓存模式，就大功告成了。然而，我一直想挂载云，这导致了一些问题。

你可以将`rclone`设置成作为`systemd`服务运行，但这对我来说不太好。只是把我的命令放在我的登录配置文件中似乎效果更好。但是有两个问题。首先，每次运行登录 shell 时调用它是很浪费的，即使挂载已经在那里了。其次，有时网络连接会断开，挂载的目录处于某种僵尸状态。你不能重新安装，但你也不能得到任何文件。

## 剧本

我的问题的答案？创建一个简单的脚本。

```
#!/bin/bash 
# error checking 
if [ $# != 2 ] 
then 
cat <<EOF 
   Usage rclonemount volume mount_point 
EOF 
exit 1 
fi 

if ! which rclone >/dev/null # check we have rclone
then 
   echo Can\'t find rclone, exiting. 
   exit 3 
fi 

if [ ! -d "$2" ] 
then 
   echo Mount point $2 does not exist. 
   exit 2 
fi 

VOL="$1" 
DIR="$2" 

# Check if getting something out of the dir fails 
# if so, maybe a stale mount so try to unmount 
if ! ls "$DIR/." >/dev/null 
then 
   fusermount -u "$DIR" 
fi 
# See if directory appears to be mounted. If so, we are done 
if grep "$DIR" /etc/mtab >/dev/null 
then 
   echo $VOL Mounted 
else # if not, mount it 
   echo Mounting $VOL 
   rclone mount --vfs-cache-mode full "$VOL"/ "$DIR" & # run in background
fi
exit 0  # we tried
```

在我的 shell 启动中，我简单地为每个遥控器调用一次这个脚本，并将它们安装到类似于`~/cloud/googledrive`或`~/cloud/dropbox`的东西上。当然，您也可以将该脚本作为`systemd`的用户服务来运行。

有一个警告。有一天，你的一个遥控器将无法安装。您必须记住，您可能需要再次运行配置来重新授权到远程服务的连接，或者更改密码(如果您最近更改了密码)。错误消息不会清楚地说明这一点。

您可以使用相同的通用脚本，用`sshfs`代替`rclone`，并且`rclone`也可以通过 SSH 挂载。选择你的毒药。

## 心不在焉

我有自己的 WebDAV 服务器，让它看起来像是我所有机器上的一个目录真的很方便。我承认我也喜欢将 Google 相册映射到我的文件系统。`rclone`的范围令人印象深刻，它似乎已经跟上了远程服务似乎每隔几个月就做出的各种变化，这些变化经常破坏类似的工具。总的来说，这是一个很好的工具。

我没有试过，但显然`rclone`也可以在其他平台上工作，包括 BSD、MacOS，甚至 Windows，在这些平台上，它看起来像是安装了一个驱动器号。让我们知道！