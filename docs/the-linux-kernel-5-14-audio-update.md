# Linux 内核 5.14 音频更新

> 原文：<https://hackaday.com/2021/07/13/the-linux-kernel-5-14-audio-update/>

您可能还记得几周前我们运行的 Pipewire 覆盖率，以及用 Pipewire 修复 Firewire 设备支持的 TODO 项目。事实证明，这对于内核黑客来说也是一个重要的特性，因为 Alsa 的变化刚刚被纳入 5.14 内核，并且包括了所需的 Firewire 音频作品。向[Marcan]大声疾呼，感谢他指出了这个变更集。是的，这和[Hector Martin]是一样的，那个把 Linux 带到 M1 的黑客，他也发现了 M1racles。我们以前报道过他的一些作品。

事实证明，一些 Firewire 音频设备希望传输流中的定时信息与流中包含的音频的正确回放时间相匹配。一个天真的驱动程序最终将声音数据包发送到 Firewire 设备，该设备希望在数据包到达之前播放声音数据包。难怪这些设备不能正常工作。我运行的是 5.14 开发内核，到目前为止，我的 Focusrite Saffire Pro40 运行得非常好，而以前的内核很快就将其音频变成了一片混乱。

对于 Pipewire 用户来说，还有另一个值得注意的修正，[减少了 USB 音频设备的延迟](https://lore.kernel.org/alsa-devel/20210601162457.4877-6-tiwai@suse.de/)。这个结果不太正确，导致 Torvald 机器的内核挂起。它已经被恢复，直到问题可以被纠正，但希望这个将登陆 5.14。(编辑:补丁清理完毕，[已拉 5.14](http://lkml.iu.edu/hypermail/linux/kernel/2107.1/00919.html) 。 [Via Phoronix](https://www.phoronix.com/scan.php?page=news_item&px=USB-Low-Latency-5.14-Try-2) 。)如果您想看到更多内核开发更新，请告诉我们！