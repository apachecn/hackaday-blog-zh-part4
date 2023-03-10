# 面向物联网应用的低成本电流探针

> 原文：<https://hackaday.com/2020/07/27/a-low-cost-current-probe-for-iot-applications/>

当谈到物联网时，许多设备使用电池、太阳能或其他有限的电力来源。这意味着低功耗是成功的关键。然而，这些电路消耗的电流通常相对较小，难以测量，其中大量瞬态电流来自其 RF 电路。为了有效地测量这些低电流消耗， [[Refik Hadzialic]建造了一个便宜但精确的电流探头。](https://www.lab4iot.com/2020/07/24/a-low-cost-current-measuring-technique-for-iot-devices-diy/)

该探头由一个仅 0.1ω的低值电阻组成，充当与所需负载串联的分流电阻。通过测量这个已知电阻上的压降，可以计算出电路的电流消耗。

然而，对于低电流消耗，电压降非常小，因此需要一些放大。[Refik]很好地解释了他的选择过程，深入到所涉及的数学中，以获得恰到好处的增益和部分选择。选择德州仪器(ti)的 INA128P 仪表放大器是因为它具有良好的共模抑制比(CMRR)和增益带宽。

最终电路表现良好，与流行的 [uCurrent Gold](https://www.eevblog.com/product/ucurrentgold/) 测量工具相媲美。虽然功能较少，但[Refik]的电路似乎在噪声方面表现更好，这可能是由于 TI 器件的 CMRR 额定值较高。这是一个很好的例子，说明了 DIY 方法如何能够在简单地购买现成的东西之外获得坚实的结果。

电流感应是你工具箱中的一项关键技能，甚至可以帮助解决洗衣纠纷。休息后的视频。

 [https://www.youtube.com/embed/VQXPpeowj9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VQXPpeowj9o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

