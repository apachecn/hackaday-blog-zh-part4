# “大喊按 B”Mod 让 N64 控制器更差

> 原文：<https://hackaday.com/2018/11/25/yell-to-press-b-mod-makes-n64-controller-worse/>

可能没有理由会有人真的想要这样的一个 mod。嗯，没有好的理由。但是[威廉·奥斯曼]一直在思考用按钮以外的输入来玩一些经典游戏会是什么样子，并决定[在一个旧的 N64 控制器上制作一个负责按下 B 按钮](http://www.williamosman.com/2018/05/scream-activated-n64-controller.html)的音频传感器。当他拜访 YouTube 视频游戏爱好者时，这种“喊按 B”的模式也是向他的主人展示的独特之处。

![](img/213711f0f77d9c4bffad5c111def0dde.png)[William]承认这个构建有点像黑客的工作，但项目页面很好地记录了他的构建过程，并涵盖了与独立硬件接口所涉及的各种决策。毕竟，大多数初露头角的黑客迟早会问自己“我如何让我的小工具按下另一个东西上的按钮？”[William]最终使用一个小继电器在麦克风模块触发时关闭 B 按钮迹线之间的连接，但他指出，应该可以实现非破坏性版本的 mod。存在用 Arduino 读取 N64 控制器状态的[的例子，这可以形成“喊按 B”(或其他任何东西)而不是焊接到按钮触点的中间人方法的基础。下面嵌入了一个视频，在视频中你可以看到人们努力应对这种怪异的模式。](https://github.com/pothos/arduino-n64-controller-library)

 [https://www.youtube.com/embed/IYlt8JRpaJg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IYlt8JRpaJg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



N64 控制器对它的粉丝来说有着特殊的意义，他们准备去令人印象深刻的长度，例如[由于 3D 打印而重新设计的 N64 模拟棒](https://hackaday.com/2018/09/21/the-n64-controller-gets-brass-gears-through-3d-printing/)。N64 控制台本身已经被改装成便携的[，并配有嵌入卡带体的屏幕](https://hackaday.com/2018/10/02/a-new-take-on-building-a-portable-n64/)。就连软件也遭到了黑客攻击，正如我们在立体 3D 渲染的*[陶笛中看到的那样，虚拟现实“舞台”取代了屏幕](https://hackaday.com/2018/07/10/n64-emulated-in-vr-makes-hyrule-go-3d/)。*