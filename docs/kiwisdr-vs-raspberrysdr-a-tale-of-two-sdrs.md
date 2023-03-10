# kiwi SDR Vs RaspberrySDR——两个 SDR 的故事

> 原文：<https://hackaday.com/2020/09/30/kiwisdr-vs-raspberrysdr-a-tale-of-two-sdrs/>

一旦你远离通常的软件定义无线电(SDR)加密狗，你只有几个选择，除非你想放弃一些严重的现金。一种常见的爱好级 SDR 是 KiwiSDR。这种流行的设备运行 Linux，可以接收高达 30 兆赫。该平台使用专用模数转换器、FPGA 和 BeagleBone 计算机。成功当然会滋生模仿者，尤其是当你有一个像 Kiwi 这样的开源设计时，你会发现类似的设备可能有不同的最终目标。这就是树莓博士的由来。这是一个与 KiwiSDR 非常相似的单元，但它使用了树莓 Pi，还有一些其他的不同之处。有什么不同？[KA7OEI] [在最近的博客文章](https://ka7oei.blogspot.com/2020/09/comparing-kiwisdr-and-raspberrysdr.html)中告诉我们。

除了计算机的明显差异和它所需要的一切，RaspberrySDR 具有更高的 A/D 速度(125 MHz 对 66 MHz)和 16 位分辨率，而不是 Kiwi 的 14 位。这两者相结合，使 Raspberry 具有更宽的接收范围(高达 60 MHz ),并且在理论上，在动态范围和失真方面具有更好的性能。

[KA7OEI]测量了两款设备的一些关键参数，并得出了一些令人惊讶的结论。几维鸟似乎在其截止频率附近增强信号，以补偿系统中的损耗。树莓——使用改编的软件——看起来好像做了同样的把戏，但它是在几维鸟的截止频率附近做的，该频率较低。当然，也许一个软件补丁可以解决这个问题。

还有镜像拒绝和前端过载的测试。测试揭示了信号强度测量的一些问题和 RaspberrySDR 的一些其他问题。然而，最大的问题是，16 位模数转换器似乎没有更好的性能。没有适当的设计，在一个问题上投入更多的精力并不总是有帮助的，这似乎是一个很好的例子。

最后，树莓看起来像是猕猴桃的廉价克隆，有一些好处，但也有一些缺点。这篇博客文章还涉及了一些开源问题，Kiwi 现在表示，他们的部分代码将来只会是二进制的，并且很难找到树莓的所有文件。如果你想买一个，你可能不会找到“raspberrysdr”这个名字，但[KA7OEI]建议搜索“新的 16 位 62M 实时带宽网络共享 sdr 接收器”，这确实会找到一些结果。

当然，你总是可以使用一个 Pi 和一个更传统的加密狗，这就足够了。如果你想让一个 Pi 只是传输，你可以用[比电线](https://hackaday.com/2015/11/04/rpitx-turns-rasberry-pi-into-versatile-radio-transmitter/)多一点，虽然质量可能不完美。