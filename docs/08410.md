# 对机器人进行逆向工程

> 原文：<https://hackaday.com/2020/11/21/reverse-engineering-a-pokewalker/>

PokeWalker 是任天堂长期寻求让儿童(可能还有一些成年人)走路和锻炼的一部分。有口袋妖怪、口袋妖怪皮卡丘、口袋妖怪 Plus、口袋妖怪皮卡丘 2、口袋妖怪迷你，当然还有口袋妖怪 Go。尽管已经问世十年了，但该设备没有 ROM 转储，关于通信协议的文档也很少。[德米特里·格林伯格]承担起了改变这一切的责任，并打开了口袋沃克。

在其核心部分，PokeWalker 只是一个带有红外端口和 96×64 灰度屏幕的计步器。它于 2009 年问世，伴随着任天堂 DS 的新口袋妖怪发行。打开设备，发现一个 64KB 的 EEPROM，一个瑞萨 H8/38606R CPU，一个博世 BMA150 加速度计和一个通用的红外收发器。CPU 特别有趣，因为除了非常罕见之外，它还混合了 8 位、16 位和 32 位以及 24 位指针。这给了它 64K 的地址空间。虽然 CPU 是可编程的，但任何尝试都会擦除板载闪存。通信协议数据包在每个数据包之前都有一个 8 位报头。报头包含一个校验和、一个命令字节、四个会话 id 字节和一个未使用的字节。奇怪的是，每个字节在广播之前都要与 0xAA 进行异或运算。

一个命令是 EEPROM 写入，它使用反向参考压缩。每个要写入的数据块被打包成 128 字节的块，尽管由于压缩，128 字节可能不会被发送。该命令理论上可以向后引用 4k 字节，但实际上只能向后引用 256 字节。正是这个命令奠定了漏洞利用的基础。通过精心制作要发送的命令，该命令可以溢出解压缩缓冲区并进入可执行代码。只有几个字节可以溢出，所以有效载荷需要精心制作。这使得攻击者能够读取系统 ROM 并通过红外端口将其广播出去。在看门狗重新启动设备之前，只能转储 22k 字节。通过改变起始地址，很容易进行多次传递。

在 ROM 从不同的通道拼接在一起之后，不同的 IR 命令被分析。特别是，发现了一个允许直接写入 RAM 的命令。这使得利用更加容易，因为您可以编写您的利用，然后覆盖事件表中的指针，然后让利用在系统自然跳转到您的利用时恢复事件表。

[Dmitry]通过编写一个 PalmOS 应用程序来从 PokeWalker 转储 ROM 并修改系统状态，从而完成了这一惊人的利用。之所以选择 PalmOS，是因为它是实现可编程 IR 收发器的一种简单而廉价的方式。总而言之，这是一篇精心撰写的精彩文章。这不是第一个[被精心设计的视频游戏配件](https://hackaday.com/2016/10/05/reverse-engineering-the-pocket-station/)，我们确信这不会是最后一个。

 [https://www.youtube.com/embed/wthwr__YJFE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wthwr__YJFE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[schme16]发送此邮件！

[专题图片:[legandarypkmn.net](https://legendarypkmn.net/2009/11/26/pokewalker-and-activity-meter-teardown/)和 [Arty2](https://twitter.com/Arty2)