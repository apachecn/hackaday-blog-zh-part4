# 在 PCB 上玩蛇！

> 原文：<https://hackaday.com/2021/04/03/playing-snake-on-a-pcb/>

当话题转向老款诺基亚手机时，唤起人们记忆的不太可能是超长的电池续航时间或凭空变出信号的能力，而是内置在普通固件中的*贪吃蛇*游戏。贪吃蛇是一个令人上瘾但极其简单的游戏，在这个游戏中，一行像素——问题中的蛇——在屏幕上导航，在不撞到墙壁或自身的情况下吃掉水果。随着游戏的进行，蛇的长度越来越长，这是一个非常困难的挑战。如果你渴望*蛇*，正如【VK5HSE】所写的，[你现在可以在 PCB 布局](https://vk5hse.blogspot.com/2021/03/how-to-play-snake-game-on-your-pcb.html)中玩它。

![](img/59381eeb18deecc965aead1134195ad5.png)问题中的软件是 [PCB-RND](http://repo.hu/projects/pcb-rnd/) ，一个跨平台开源的 PCB CAD 工具，游戏是通过用户脚本的魔力实现的。简单地[下载脚本](http://repo.hu/cgi-bin/edakrill.cgi?cmd=show&krill=igor2/script/pcb-rnd/game_snake.krill)，在你最喜欢的电路板上运行，然后你就可以走了！

我们无法想象这款软件的实际用途，但如果看到一条蛇爬进我们的几块电路板，我们也不会感到惊讶。它确实提供了一个方便的提示，提醒你 PCB CAD 工具的脚本功能的强大，这可能是我们中的许多人没有充分利用它们的潜力。

我们以前在[一个非常有用的 Eagle 导入工具](https://hackaday.com/2017/12/21/exporting-eagle-libraries-to-foss-tools/)中介绍过【VK5HSE】在 PCB-RND 的工作。