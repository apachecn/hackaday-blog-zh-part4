# 由实际穿孔控制的黑客穿孔

> 原文：<https://hackaday.com/2021/11/10/hacked-punch-out-controlled-with-actual-punches/>

除了玩喷气滑旱冰和挥舞闪电之外，伊恩·查纳斯(Ian Charnas)一直在黑客攻击复古电子游戏，这种方式稍微安全一些。经过大量的努力工作，伊恩已经设法在 NES 拳击游戏“出拳”中加入姿势估计来控制角色他那样做肯定不会受伤吧？不，但是因为伤害那些可怜的受苦的角色是不公平的，而他自己没有受到任何伤害，他增加了电击反馈来给游戏更多一点，咳咳，*重拳*。看，玩电子游戏会受伤的！

从 [Google MoveNet](https://www.tensorflow.org/hub/tutorials/movenet) 开始，这是一个预烤的骨骼跟踪模型，可以在使用 TensorFlowJS 的浏览器中运行，他为通常用游戏控制器执行的各种拳击动作定义了一些简单的启发。接下来，他需要得到游戏。作为一个全面的好人，[伊恩]购买了游戏卡带的原始副本以获得许可，然后使用 RetroUSB 的 [USB 副本](https://www.retrousb.com/product_info.php?products_id=36)，为下一步倾倒出游戏二进制文件。

为了在同一台机器上运行游戏和姿态模型，选择了 NES 硬件的仿真，由 [FCEUX](https://fceux.com/web/home.html) 负责。这简化了游戏的控制，因为在最初的 NES 上运行它需要更多的工作。通过使用 [emscripten](https://emscripten.org/) ，FCEUX 被交叉编译成 WebAssembly，因此游戏和控制端都属于 JavaScript 领域。老实说，在玩了一会儿游戏后，[Ian]发现它太快了，无法用姿势控制来玩，而不是更快的按键，所以需要一些游戏黑客。仿真让这变得容易多了。

[伊恩]花了大约两个月的时间来分解游戏二进制文件，并找出围绕角色的游戏逻辑，以便让他们慢下来，使其可以玩，但他做到了。你可以当评委，既然他买了一堆弹夹解锁了更多的许可证副本，[你也可以玩一下](https://reallifepunchout.com/)。只是不要加上电击的部分，没有人需要从一个两英寸高的明亮的橙色迈克泰森管理电击疗法！

 [https://www.youtube.com/embed/07JibJJVNp8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/07JibJJVNp8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

