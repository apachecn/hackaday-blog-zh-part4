# SWO:一枚纹章，也可以叫别的名字

> 原文：<https://hackaday.com/2022/05/25/swo-an-arm-printf-by-any-other-name/>

我会坦白。虽然`printf`风格的调试名声不好，但我发现自己有时会求助于它。当然，`printf`很贵，而且会带来很多代码，但是如果你有空间和时间在调试的时候使用它，你可以在完成之前删除它。但是，如果你没有输出设备，或者你把它用于其他用途，该怎么办呢？如果您使用的是最现代的 ARM 芯片，您还有另一个选择——一个专用的输出通道，用于多种用途，包括调试输出。我决定在运行 mbed 的 Blackpill 上尝试一下，发现这并不像你想象的那么简单。但是这是可能的，当你读完了，你也能做到。

我是用 STM32 专用的 ST-LINK 硬件写的。如果您使用其他 JTAG 设备，如 BlackMagic probe，您可能已经为您设置好了。

## 你有什么

我将从最终结果开始，然后谈论软件，这样当您达到硬件要求时，您将会表现良好并受到激励。剧透:你现有的硬件可能需要快速修改才能工作，尽管如果你愿意，你可以买现成的。

下面是一个非常简单的测试程序:

```

SWO_Channel debugport;  // requires #include "SWO.h"
int main() 
  {
  unsigned count=0;
  debugport.printf("\r\nHello World from SWO\r\n");
  debugport.printf("CPU SystemCoreClock is %d Hz\r\n", SystemCoreClock);

  while (1) 
    {
    led = !led; // flip LED if output is true
    ThisThread::sleep_for(rate); // sleepy time
    if (count % 10) debugport.putc('*'); else debugport.printf("%d\r\n",count); 
    count++;
    }
}

```

这里没什么难以想象的。您可以使用`putc`或`printf`写入调试输出。正如您在图中看到的，您得到了一个显示所有输出的漂亮窗口。实际上有 32 个输出通道，但通道 0 是为调试输出保留的。在这种情况下，我选择了所有，因为它是唯一从设备中出来的东西。

## 你需要什么

[![](img/cacec2f5ab25e4b4e351819605c4e282.png)](https://hackaday.com/wp-content/uploads/2022/05/swv.png)

ST’s STM32CubeProgrammer can display SWO data.

首先，你需要一个兼容的 ARM 芯片。并非所有的 ARM 芯片都支持 ITM(集成跟踪宏单元)，但这正是你所需要的。设备上会有一个标记为 SWO 的 pin 码(可能还有其他东西)。由于我使用的是带 STM32F411CE 的 Blackpill，我们知道它应该可以工作，输出引脚为 PB3。

您还需要一个带有 SWO pin 的 ST-Link 加密狗。不幸的是，看起来像你通常得到的 USB 存储设备的廉价产品没有 SWO 针。然而，你可以很容易地破解它们。“完整的”ST-Link V2 有销带出来，但通常要贵得多。然而，如果你去通常的中国商店购物，你通常可以找到一个合理的价格。我付了不到 10 美元。

当然，您还需要某种工具来读取输出。一个普通的终端是做不到的，但是 ST 的 STM32CubeProgrammer 可以轻松读取数据。当然，还有其他选择。许多 ide 和调试器可以读取 SWO 输出。还有一些[开源工具](https://github.com/stlink-org/stlink)，但是 Ubuntu 包太老了，发布包没用。不过，从零开始建造确实有效。

## 软件设置

自从我使用 Mbed 以来，我做的第一件事就是寻找一个库。我没有失望。该库是 CMSIS 中 ITM 函数的一个薄薄的包装，所以如果你没有使用 Mbed，只要看看这些函数，你就能弄明白了。如果你喜欢 STM32Duino，[看看类似的东西](https://github.com/koendv/SerialWireOutput)。

一旦我将它添加到项目中，我必须解决一个小问题。这可能无关紧要，但是有一个实例，其中一个数组被分配给一个文件名，然后被不正确地删除了。注意下面代码中的`delete`:

```

bool SWO_Channel::claim (FILE *stream) {
  if ( FileBase::getName() == NULL) {
  error("claim requires a name to be given in the instantiator of the SWO instance!\r\n");
  }

//Add '/' before name:
  char *path = new char[strlen(FileBase::getName()) + 2];
  sprintf(path, "/%s", FileBase::getName());

  if (freopen(path, "w", stream) == NULL) {
// Failed, should not happen
  return false;
}

  delete [] path;   //  fixed

//No buffering
  setvbuf(stream, NULL, _IONBF, 32);
  return true;
}

```

一旦完成，你就可以走了。你只需要一些硬件。

## 硬件设置

如果您有“正常”的 ST 加密狗，就像下图中的白色加密狗，那么设置就是正常的设置。将电源、接地和两个调试引脚连接到 Blackpill 的背面连接器，然后从 SWO 连接到设备的 B4 引脚。

[![](img/1ec118fe624ddfb376f568d134a92486.png)](https://hackaday.com/wp-content/uploads/2022/05/stlink.png)

如果你有一个像紫色的廉价克隆体坐在白色设备旁边，你将需要做一些手术来取出一个额外的 pin。

加载一个程序，做一些简单的 SWO 输出，然后启动一切。您可能需要升级 ST-Link 的固件，STM32CubeProgrammer 软件也可以做到这一点。

用编程器连接硬件时，发现白色加密狗在 4000 kHz 时连接不可靠，只好选择 1800 kHz。那可能只是那个装置或者我的杂乱的线路。你可以在相邻的截图中看到我使用的连接信息。请按“连接”开始。

[![](img/b26746d15ca82ac989c89ed65d12dc61.png)](https://hackaday.com/wp-content/uploads/2022/05/settings.png) 当您选择 SWV 项目时，您需要为此设置设置 96 MHz 的时钟。据推测，如果你运行在不同的频率，你会知道你的设置正确的值。当您按下 Start 时，您应该会看到程序的输出。

唯一要记住的是，你的软件将会争夺加密狗，除非它已经在“共享”模式下工作。在我的情况下，Mbed Studio 似乎并不关心这个设置，所以如果你想让它重新编程芯片，你必须断开连接。当然，你可以使用程序员做任何事情。这完全取决于您的工具和设置。

当然，一旦你做了一次，就很容易在未来的项目中复制。你的程序中只有一根额外的线和两个额外的文件。

## 更进一步

不过，你可以更进一步。首先，有丰富多彩的输出。如果您的调试字符串包含#RED#、#GRN#或#ORG#，则该行的其余字符将以该颜色显示(红色、绿色或橙色)。当然，假设观众明白这一点，并且你打开了电视。例如，用红色显示重要信息是很方便的。

然而，有这么多额外的频道我们没有使用，这是一种浪费。例如，为什么不在通道 0 上显示进度消息，在通道 1 上显示详细的调试信息呢？你可以从第五频道的外部设备获取大量信息。当然，你可以在这一行写一个前缀，然后把数据取出来，但是这样更有趣。

我重写了现有 SWO 类的一小部分，由于可选参数，它仍然工作。唯一的区别是您可以向构造函数添加一个通道号，这样就有可能创建多个调试流:

```

SWO_Channel debugport;
SWO_Channel dbg2("second",1);

```

代码改动很少，但我会将整个项目放在 [GitHub](https://github.com/wd5gnr/mbed-swo) 上。

如果你不知道，我喜欢使用 STM32 和 Mbed。当然，你可以通过回避 Mbed 获得更好的性能，但好的一面是[你可以](https://hackaday.com/2020/11/17/bare-metal-stm32-from-power-up-to-hello-world/)。奇怪的是，通过一个端口将数据推送到[几个通道](https://hackaday.com/2022/05/03/linux-fu-the-infinite-serial-port/)是我以前以完全不同的方式做过的事情。