# 你的无线电手表没有信号？自己做发射器就行了

> 原文：<https://hackaday.com/2018/09/10/no-signal-for-your-radio-controlled-watch-just-make-your-own-transmitter/>

如果你有一只无线电控制的手表，你可以赢得任何关于时间的争论。或者，至少，如果有信号的话，你可以。[Henner Zeller]住在一个接收不到 DCF77 信号的地方，而他的欧洲腕表却能接收到该信号。因此，他决定[制作自己的微型发射器](https://github.com/hzeller/txtempus)，模拟 DCF77 信号，让手表同步。

Raspberry Pi Zero W 是发射机的心脏，而[Henner]设法让它在 GPIO 引脚上产生 77500.003Hz，足够接近 DCF77 使用的 77.5kHz 载波。信号是调幅，每秒传输一比特，每分钟重复一次。第二个 GPIO 执行所需的衰减，对于只需要工作几英寸的天线来说，几圈导线就足够了。Raspberry Pi 与 NTP Stratum 1 服务器同步，这使得系统时间的精确度约为 50 毫秒。整个东西放在一个光滑的 3D 打印外壳中，为手表提供了一个晚上休息的支架；这意味着每天早上它都是同步的，随时可以运行。

[Henner]还花时间为 WWVB(美国)、MSF(英国)和 JJY(日本)执行协议。考虑到我们最近[写了关于 WWVB 被关闭的可能性](https://hackaday.com/2018/08/20/what-will-you-do-if-wwvb-goes-silent/)，这可能也无妨。在尝试之前，请务必检查您所在地区的规则。

我们以前见过 WWVB 模拟器，像 [this ATtiny45 build](https://hackaday.com/2014/03/22/build-your-own-radio-clock-transmitter/) ，但是我们喜欢这个解决方案是一个简单的命令行工具，它支持许多地理位置。