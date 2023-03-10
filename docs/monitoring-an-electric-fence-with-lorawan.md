# 用 LoRaWAN 监控电网

> 原文：<https://hackaday.com/2019/08/28/monitoring-an-electric-fence-with-lorawan/>

确保防止牛羊走失的电围栏仍然正常工作似乎是一项相当艰巨的任务，尤其是当这个围栏距离一个人的家相当远时，检查它非常耗时。在[kiu]的一个朋友因为一些绵羊越狱而被警察打了几次电话后，显而易见的技术解决方案是用 LoFence 物联网启用围栏。

这个解决方案非常简单，非常优雅。为了给家里打电话提供状态数据，该系统使用了[微芯片 RN2483 IC](https://www.microchip.com/wwwproducts/en/RN2483) ，它几乎可以处理 [LoRaWAN](https://en.wikipedia.org/wiki/LoRa#LoRaWAN) 的所有方面，因此人们只需将数据发送到它的串行接口进行传输。因为这个系统使用[物联网](https://www.thethingsnetwork.org/) (TTN)，所以没有因低数据速率而产生的服务成本。这是容易的部分，除了必须增加一个 [LoRaWAN 网关](https://www.thethingsnetwork.org/forum/t/ttig-the-things-indoor-gateway/22049)来增强有电栅栏的区域的信号。

覆盖这一侧后，其余部分包括 AVR ATmega328p MCU、电阻分压器和运算放大器(TLV9062)以及一些无源器件。由此产生的电路测量电压，主要是为了检测栅栏是否仍然形成完整的电路。侵入给栅栏提供能量的小盒子可能是一种可能的升级，但至少这是一种相当简单的测量方式。毕竟，电栅栏在有电压的情况下工作得最好。

在 LoRaWAN 网络的另一端，数据由一个服务解析和分析，以便可以显示在 Grafana 仪表板上，确保只需一瞥就足以看到围栏的当前状态，以及是否需要在凌晨 1 点冒雨冲出去修理它。