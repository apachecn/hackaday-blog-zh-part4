# 您的固件中包含更多固件

> 原文：<https://hackaday.com/2020/10/01/even-more-firmware-in-your-firmware/>

有许多方法可以在现场更新嵌入式系统。图像可以一次一张在空中飞行，通过运动鞋传播，或者搭上其他传递数据的便车。好吧，也许这有点夸张，但是肯定有很多方法可以将这些更新字节放入目标系统。这些字节是如何组装的，组装的工具是什么？这是我需要解决的问题。

[回想一下，我的系统](https://hackaday.com/2020/09/15/putting-the-firmware-in-your-firmware/)并不是一个特别新颖的系统(见下面的框图)。只是几台电脑通过串行总线互相询问更新。我选择将有效负载固件映像捆绑到用于执行更新过程的中间微控制器的二进制文件中。额外的限制是，三个固件映像(一个载体和两个有效载荷)的混合需要在编译后很长时间内在具有单独工具链的不同系统上进行。最终有两个选项符合要求。

![](img/749df76f6cacac004e54b7c53488cbf7.png)

The system thirsty for an update

# 编辑精灵

使用链接器将二进制文件粘在一起的方法不止一种——这毕竟是它的工作。典型的编译工具链使用`ld`将目标文件串在一起，但是也有其他链接器附近的工具可以方便地处理正确类型的二进制文件。这种将固件映像捆绑在一起的方法将关注 GCC 中的一个新工具`objcopy`。

滥用这个比喻，`objcopy`有点像用于对象文件操作的实用工具。它的功能范围很广，但是我们这里需要的具体东西是`--update-section`参数，它允许我们用另一个目标文件替换一个目标文件中的命名部分。那么我们如何得到那部分呢？这就是名为“链接器脚本”的配置文件发挥作用的地方。

关于链接器脚本用法的详细讨论超出了这里的范围，但是现在让我们把它总结为链接器的一个脚本！一个完整的可执行文件由[许多不同的部分](https://en.wikipedia.org/wiki/Object_file#Segmentation)组成，链接器脚本描述了它们应该去哪里以及如何引用它们。例如，在微控制器中，存储要执行的代码的[文本部分](https://en.wikipedia.org/wiki/Code_segment)通常放在闪存中微控制器开始执行的地址。链接器脚本描述了数据应该进入的区域，以及它应该位于闪存中的位置。我们可以使用相同的机制将固件有效负载注入到我们的映像中。

我的第一步是描述两个新的部分，每个新的固件映像一个部分。下面的部分显示了中间微控制器的[数据段](https://en.wikipedia.org/wiki/Data_segment)，以及我在它下面添加的两个有效载荷段。

```
/* Initialized data sections into "RAM" Ram type memory */
.data : 
{
  . = ALIGN(4);
  _sdata = .; /* create a global symbol at data start */
  *(.data) /* .data sections */
  *(.data*) /* .data* sections */

  . = ALIGN(4);
  _edata = .; /* define a global symbol at data end */

} >RAM AT> FLASH
/* Below this point are the sections I added */
.payload1 :
{
  . = ALIGN(4);
  BYTE(0x0);
  payload1End = .;
} >FLASH

.payload2 :
{
  . = ALIGN(4);
  BYTE(0x0);
  payload2End = .;
} >FLASH
```

这有点神秘，但应该清楚的是，`payload1`和`payload2`都是要放在 flash 中的特殊描述的部分。有了这些定义，链接器将负责确保符号被定义，部分足够大，并且它们不会与其他任何东西重叠。它们将以相同的顺序相对于它们的邻居浮动，保持这两个部分在 flash 的末尾，而`*end`符号在它们各自部分的末尾。

为了在运行时访问这些部分，我们可以在 C 源代码中将命名符号`payload1/payload1End`和`payload2/payload2End`称为`extern`符号，但是它们在编译后的二进制文件中也是可见的。为此，我们需要使用链接器生成的可执行链接文件(ELF)作为最终输出。在我的例子中，这是默认输出，并从 ELF 转换为二进制以闪存到微控制器。根据您的平台，情况可能是这样，也可能不是这样。

ELF 文件包含运行程序所需的一切，包括链接器在链接时拥有的所有元数据和符号，而二进制文件可能会将这些去掉。如果它们存在，那么像`objcopy`这样的工具可以引用它们。此时，注入固件只需要一个格式良好的命令。将有问题的 bin 有效负载转换成一个目标文件，然后使用`objcopy`将其注入到最终的二进制文件中，如下所示

```
borgel$ objcopy --update-section .payload1=payload1.bin combined-firmware.elf
```

使用与链接器相同的技巧来使所有东西都合适，并根据需要移动我们的符号来标记有问题的部分。现在，正在运行的固件可以通过减去起始和结束符号的地址来获得大小，并在起始地址开始时引用有效载荷内存。轻松点。

那么，为什么这不是我注入有效载荷固件的最终方法呢？它需要一个知道如何处理目标架构的 elf 的`objcopy`副本。在我的用例中，我没有合适的工具链来使用它，所以我转移到下一个方法。

# 1337 年 H4X:二进制编辑

如果没有更聪明的方法，二进制文件只是一个可以编辑的文件。这并不特别优雅，但是如果不是普遍适用的话，直接修改二进制文件也没什么，只要您知道文件的细节。

让我们从将多个二进制文件连接在一起开始。这被证明是非常简单的；把它们连接起来！该命令看起来像

```
borgel$ cat payload1.bin payload2.bin >> combined-firmware.bin
```

就这么简单！我需要将合并后的文件放入中间的微控制器，这同样简单。微控制器的闪存工具会很高兴地将组合固件写入设备，将有效载荷文件放在正确的地址。但是正在运行的固件如何知道去哪里提取有效载荷呢？它怎么知道它们有多大？为此，我们需要回到我们的朋友链接器。

请记住，我们必须处理的文件是最终的二进制图像，没有前面方法中的任何嵌入元数据。即使有，这个过程也需要在手头没有处理器专用工具链的情况下工作。那怎么办呢？在编辑 ELF 时，我们使用了链接器脚本来描述 flash 中的一个新部分。我们可以在这里使用相同的技巧来创建一个特殊的“固件结束”部分和符号。只要链接器脚本将它定位为要写入闪存的映像的最后一个元素，它将保证随着固件的其余部分在开发过程中增长和收缩而浮动并始终停留在末尾。

现在我们有了一个固件结束标志，这个难题就可以解决了。为了简单起见，在这一节中，我选择放置 8 个神奇的字节(作为两个`uint32_t`)来描述要跟随的图像的大小。将来，如果我需要更多的灵活性，我可以把一个文件放在一个 JSON 对象中，一些[序列化的 msgpack](https://hackaday.com/2020/06/10/the-ceedy-world-of-message-serialization/) ，或者其他任何东西。最终的图像看起来像

```
[main firmware][8 byte size file][payload 1][payload 2]
```

但是如果没有附加有效载荷会发生什么呢？中级微控制器需要一种方法来判断在闪存的荒野中是否有任何要搜索的东西。擦除的闪存可能会工作(它应该总是读取为 0xFF)，但如果闪存映像缩小，并且我不幸处于擦除边界，则那里可能会有看起来有效的垃圾数据，而不是 0x ff 的新字段。为了避免这种情况，我再次求助于链接器。

链接器脚本允许定义硬编码的字节或字节模式来填充一个区域。所以我在固件结束标志后的区域*中添加了两个 4 字节的校验值。在运行时，固件从固件偏移量的末尾加载有效载荷固件大小，并将它们与检查值进行比较。如果它们匹配，则假定不存在有效载荷。链接器脚本中定义的部分如下所示*

```
.endmatter :
{
  . = ALIGN(4);
  endmatterStart = .;
  LONG(0xDEADC0DE); /* Payload 1 size */
  LONG(0xDEADBEEF); /* Payload 2 size */
} >FLASH
```

当固件被捆绑在一起，我截断了主要的固件文件，并删除了最后 8 个字节，以消除这一部分。然后，我创建一个包含两个有效载荷大小的文件，并将其连接到。链接器保证最后 8 个字节*总是*校验值(可以用`hexdump`确认)。此时，该命令如下所示

```
borgel$ truncate -s -8 combined-firmware.bin
borgel$ cat size.bin payload1.bin payload2.bin >> combined-firmware.bin
```

拼图的最后一块是构建 8 字节大小的文件。我想将大小作为原始字节值(不是 ASCII)嵌入，以强制它们成为恒定的大小。为此，我们必须一路回到旅程的起点，再次找到`xxd`。以前我使用`xxd`将二进制文件转换成十六进制文件(以 C 源代码的形式)，但是这个工具也可以反向工作，将十六进制文件转换成二进制文件。这并不太挑剔，所以我们只需要给它要转换的“十六进制文件”的起始地址，然后是它产生二进制输出文件应该消耗的字节序列。看起来像是

```
borgel$ printf '0: %08x %08x' `stat -c %s payload1.bin` \
  `stat -c %s payload2.bin` | xxd -r -p - >lenfile.bin
```

并给出了一个包含我们所期望的内容的文件:

```
borgel$ stat -c %s payload1.bin
922
borgel$ stat -c %s payload2.bin
176
borgel$ hexdump lenfile.bin
0000000 00 00 03 9a 00 00 00 b0
0000008
```

够了几乎是虎头蛇尾的是，最终的命令序列只是三个 shell 命令

```
borgel$ truncate -s -8 combined-firmware.bin
borgel$ printf '0: %08x %08x' `stat -c %s payload1.bin` \
  `stat -c %s payload2.bin` | xxd -r -p - >lenfile.bin
cat size.bin payload1.bin payload2.bin >> combined-firmware.bin
```

# 管理的位缓冲区

我们走吧！编辑二进制文件的另外两种方法。在这些选项和[所描述的前两个选项](https://hackaday.com/2020/09/15/putting-the-firmware-in-your-firmware/)之间，应该涵盖了大多数用例。这些技术中的大多数应该很好地服务于任何需要组合的资产；想想在没有外部存储器的系统中添加音效或图像。

希望你现在觉得自己有能力切割和掷骰子来获得二进制有效载荷的胜利，不管几何形状如何。

感谢 2016 年【Christian Stigen Larsen】发表的这篇优秀文章[“在可执行文件中嵌入二进制数据”，其中包含了这些想法的核心。如果你对另外一两个选择感兴趣，它提供了一些其他选择的极好的总结。](https://csl.name/post/embedding-binary-data/)