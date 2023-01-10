# 在树莓派上玩你最喜欢的诺基亚游戏

> 原文：<https://hackaday.com/2021/05/11/play-your-favorite-nokia-game-on-the-raspberry-pi-pico/>

在许多人的记忆中，从 90 年代末到 21 世纪初，Snake 就生活在诺基亚的手机上。然而，这个游戏已经存在了很长时间，并且将会继续存在下去。这至少部分归功于[像【哈里·威古纳】这样的人通过在新平台上实现它来保持它的活力。](https://hackaday.io/project/179669-harifun-203-pico-snake)

[Hari]着手用 MicroPython 为 Raspberry Pi Pico 编写 *Snake* 。硬件方面的事情很简单——五个按钮连接到微型电脑，以及一个 128×64 I2C 有机发光二极管屏幕来显示游戏。在软件方面，[哈里]把船推了出来，决定他的*蛇*版本必须让玩家角色像真的一样滑行。这需要一点努力才能做好，尤其是在不同方向的拐角处。然而，坚持不懈得到了回报，[哈里]完成了工作。

GitHub 上为那些想在家修补的人提供了代码。这是一个整洁的作品，虽然不是我们见过的游戏出现的最奇怪的地方—[我们之前确实见过它在 PCB 布线软件中运行，这要感谢一些漂亮的脚本](https://hackaday.com/2021/04/03/playing-snake-on-a-pcb/)。休息后的视频。

 [https://www.youtube.com/embed/5r_6mbYlLVo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5r_6mbYlLVo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

