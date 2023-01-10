# BladeRF 2.0 Micro 更小，功能更强大

> 原文：<https://hackaday.com/2018/08/30/bladerf-2-0-micro-is-smaller-more-powerful/>

当 BladeRF 于 2013 年推出时，它是新一代软件定义无线电中最强大的一款。现在，Nuand，BladeRF 的生产商正期待着用 [BladeRF 2.0 微型](https://www.nuand.com/product/bladerf-xa4/)再次提高赌注。这个新版本有一个巨大的变化和改进，包括一个更糟糕的 FPGA 处理器，支持从 47 MHz 到 6 GHz 的接收和发送，支持 2 倍 MIMO 和令人印象深刻的 56 Mhz 带宽。它还保留了与原始 BladeRF 的向后兼容性，这意味着任何支持它的软件(大多数 SDR 包都是这样)都可以在新设备上工作。

BladeRF 2.0 Micro 的核心是 Altera Cyclone V FPGA。Nuand 正在生产两种版本的 Micro:480 美元的 xA4 使用 49 kle Cyclone V FPGA，而 720 美元的 720 XA9 是围绕 301 kle Cyclone V FPGA 构建的。xA9 的额外功能在于 FPGA 上有更多的逻辑门和元件，这意味着该卡本身可以进行更多的信号处理。这将使制造处理信号并输出结果的独立设备变得更加容易。Nuand 在 BladeRF 上演示了这一点，[创建了一个运行在卡本身上的 ADS-B 接收器](https://www.nuand.com/bladerf-vhdl-ads-b-decoder/)，将解码后的飞机数据输出到 USB 端口。xA9 可以做得比这多得多，这种可能性非常有趣。

顾名思义，这种新卡也更小，尺寸为 2.5×4 英寸，这使得它更容易与 Raspberry Pi 等设备集成，尽管它仍然比 Pi 稍大一些。

自 2013 年以来，特别提款权市场发生了很大变化，出现了大量廉价的开源特别提款权接收器和收发器，如 [LimeSDR](https://hackaday.com/2018/03/13/review-limesdr-mini-software-defined-radio-transceiver/) 和 [SDRPlay](https://hackaday.com/2015/09/25/mid-price-hardware-gets-serious-about-software-defined-radio/) 。这些设备比 BladeRF 便宜，并且提供大部分相同的功能。那么，像 BladeRF 2.0 Micro 这样更强大、更昂贵的设备在市场上还有一席之地吗？正如他们所说，这是悬而未决的。