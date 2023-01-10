# 控制 MIDI

> 原文：<https://hackaday.com/2019/07/15/getting-midi-under-control/>

当 Sobolak 先生]开始他的 DIY Midi 战斗机时，他已经有了 Midi 协议的经验，因为一旦你掌握了一些东西，很自然地会在成功的基础上扩展，并建立一些更令人印象深刻、更有用、更按钮式的东西。在这方面，他一点也不罕见。更多的按钮不仅仅意味着额外的安装孔，例如，Arduino 的 I/O 将很快填满，因为电位计占据了宝贵的模拟输入，而按钮阵列接受数字输入。与 IO 扩展器使用的串行协议相比，多路复用技术是一种基于逻辑的监控或控制更多设备的方法。

复用并不在 Sobolak 先生]的技能清单中，但这是一个合适的学习时间，谁不喜欢通过改进过去的项目来获得新技能呢？所有的按钮都很容易安装，但保持电线整洁不在这个项目的范围内，所以如果你对底部的“鸟巢”感到虚弱，你可能想把目光移开，想想[一些整洁的东西](https://hackaday.com/2017/09/25/push-buttons-create-music-with-a-midi-fighter/)。不管电线多么整齐，这个系统都是有效的，你可以在休息后听一段演示。也许下方缠绕的铜是有目的的，因为它将电路板浮起来代替了外壳。

我们期待着[令人兴奋的新版本](https://hackaday.com/2012/07/15/a-replica-dj-controller-to-rule-them-all/)，在那里更多的[解决方案得到运用](https://hackaday.com/2017/09/25/push-buttons-create-music-with-a-midi-fighter/)，但有时，你必须用你现有的工具来解决问题，比如当代码不能与 [MIDI](https://hackaday.com/2017/06/30/how-to-midi-interface-your-toys/) 和 NeoPixel 库一起编译时，所以他添加了一个 Uno 来处理 led。是最优雅的吗？不。它完成任务了吗？是的，如果你不把黑板翻过来，你甚至不会知道。

 [https://www.youtube.com/embed/jJ6JKss_xAg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jJ6JKss_xAg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

