# 这种升级的电动车轮玩具足够强大，需要牵引力控制

> 原文：<https://hackaday.com/2019/06/23/this-upgraded-power-wheels-toy-is-powerful-enough-to-need-traction-control/>

除了最富有的父亲，兰博基尼 Aventador 超出了所有人的预算，但[CodeMakesItGo]为他的小儿子准备了一份礼物。这是一辆兰博基尼 Aventador，但只有 6V 动力轮的版本。因此，即使对于一个年轻人来说，它的性能也很出色，所以他决定给它升级 12V。这被证明有足够的咕噜声导致那些硬塑料车轮打滑，所以进一步的升级是[一个具有节点 MCU 的牵引力控制系统](https://hackaday.io/project/166169-traction-control-lamborghini-power-wheel)。没有其他孩子有这样的交通工具！

Power Racing 系列的退伍军人或 Hacky Racers 可能希望看到中国电机控制器的组合，但他使用了一组继电器进行简单的开关控制。牵引力控制系统有一对 3D 打印的传感器轮，它们作用于相应的一对光耦合器，向 NodeMCU 提供反馈。尝试了一系列不同的驱动器选项，最终发现 H 桥板最为可靠。

广告下方的视频展示了硬件，并详细介绍了软件。NodeMCU 的 WiFi 用于为移动中的系统提供一些可调整性。牵引力控制系统会稍微降低起步速度，但会让驾驶员更容易控制机器。他看起来对他的玩具很满意！

长期读者会知道[这不是我们向你展示的第一次动力轮升级](https://hackaday.com/2016/11/14/power-wheels-rescued-restored-and-enhanced/)。

 [https://www.youtube.com/embed/sQc1SC60owo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sQc1SC60owo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

