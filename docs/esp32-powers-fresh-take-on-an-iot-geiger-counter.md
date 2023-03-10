# ESP32 为物联网盖革计数器带来新动力

> 原文：<https://hackaday.com/2022/07/07/esp32-powers-fresh-take-on-an-iot-geiger-counter/>

多年来，我们报道了许多旨在检测高辐射水平的项目，其中相当一部分已经以某种方式连接到互联网。但由于它们通常是围绕苏联时代的 SBM-20 盖革-米勒管建造的，这些设备通常遵循相当保守的设计。随着欧洲目前的形势加剧了对潜在辐射暴露的担忧，[g3gg0]认为这是一个很好的时机，因为任何人都可以重新考虑使用更多现代组件的互联网连接盖革计数器的想法。

现在要明确的是，即使这种现代化的方法仍然使用相同的 SBM-20 管。关于如何与他们一起工作的信息是如此之多，以至于你几乎将自己置于不利的地位，去选择其他的东西作为你设计的基础。简单来说，经典是很难出错的。

[![](img/67021b9dcac32c9918317aa964a85891.png)](https://hackaday.com/wp-content/uploads/2022/07/esp32geiger_detail.jpg)

An unfortunate bug was discovered in the HV circuit.

也就是说，[g3gg0]很早就决定在设计中使用尽可能多的 SMD 元件，[这与](https://hackaday.com/2020/08/26/this-geiger-counter-has-few-parts/)[我们见过的许多 SBM-20 计数器](https://nora.codes/post/arduino-geiger-counter-dosimeter/)有很大的不同。这意味着要想出一种新的高压电源，能够为显像管提供必要的 400 V 电压，从事情的发展来看，这需要几次尝试才能完成。最终的结果可能是我们见过的最小和最干净的电路板来安装这种特殊的电子管。

为了进行这场表演，[g3gg0]选择了 ESP32-PICO-D4。你当然不需要如此强大的微控制器来读取来自 SBM-20 管的脉冲并通过 MQTT 发布它们，但公平地说，该芯片还有许多其他职责。它处理 WS2812 RGB LEDs，这些 led 在检测到颗粒时会熄灭，运行(显然是可选的)2.9 英寸 WaveShare 电子纸显示器，还从 BME280 环境传感器和 CCS811 VOC 传感器中提取数据，所以它一直很忙。

尽管这个建筑令人印象深刻，但我们确实讨厌它被建造。从某些世界领导人对其核武库实力发表漫不经心的评论，到鲁莽地试图占领[切尔诺贝利核电站](https://hackaday.com/2021/05/14/increased-neutron-levels-at-chernobyl-4-how-dangerous-is-corium/)，现在拥有一个可靠的盖革计数器并不是一个不合理的预防措施。为了每个人的利益，让我们希望这个特别的建筑上的花哨的 RGB LEDs 尽可能保持黑暗。

 [https://www.youtube.com/embed/kAV-d_5LLHw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kAV-d_5LLHw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

