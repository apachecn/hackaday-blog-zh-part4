# 从 SPIDriver 到 I2CDriver

> 原文：<https://hackaday.com/2018/12/09/from-spidriver-to-i2cdriver/>

与微控制器和其他嵌入式系统通信需要一个通信标准。SPI 是一个很好的工具，并且被广泛使用，但是它不是唯一可用的工具。还有 I2C，与 SPI 相比，它有一些优点和缺点。然而，这两种标准的问题在于，现代计算机没有内置这两种标准。为了解决这个问题，并允许更容易地在 SPI 中进行调试，[James Bowman]在几个月前开发了 SPIDriver，现在[根据大众的需求，为 I2C 开发了一款类似的设备 I2C driver](https://www.crowdsupply.com/excamera/i2cdriver)。

与 SPIDriver 非常相似，I2C 驱动程序是一个调试工具，可以在带有 USB 接口的计算机上使用。使用 I2C 经常是一件麻烦的事情，许多事情同时进行，需要同步才能正常工作，这款设备允许用户在很短的时间内设置好 I2C 设备。首先，它有一个内置的屏幕，显示当前设备的信息，如信号线和当前流量的图形解码。它还显示一个地址空间图，内置可编程上拉电阻，可以将 I2C 流量数据发送回主机进行分析。

I2CDriver 也是完全开源的，从硬件到软件，这意味着如果您有意愿和部件，您可以从头开始构建一个，或者自己修改代码以满足您的特定需求。但是，如果您仍然坚持使用 SPI，您仍然可以找到原始的 [SPIDriver 工具](https://hackaday.com/2018/07/10/spidriver-shows-you-whats-going-on/)来帮助您调试该协议。