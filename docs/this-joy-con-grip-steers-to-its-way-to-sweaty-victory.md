# 这种喜悦-Con 握转向它的方式，以汗水的胜利

> 原文：<https://hackaday.com/2021/02/08/this-joy-con-grip-steers-to-its-way-to-sweaty-victory/>

在 Hackaday，我们总是乐于看到黑客将我们最喜爱的童年游戏机改造成新的有趣的东西。在这种情况下，以制造商从未想过的方式将新的和不寻常的控制方法与旧设备相结合的 mod 并不罕见。[Mike Choi]用 Labo Fit Adventure Kit 构建的是一个罕见的黑客技术，它将全新的控制方案与现代控制台相结合:实际上没有修改任何硬件。

![](img/d1f280db5dc33f3b75363583b9aeb074.png)

Face button pusher in blue

简而言之，Labo Fit Adventure Kit 允许玩家在任天堂 Switch 上玩马里奥赛车，方法是骑固定的健身车，用轮子转向，挤压轮子来使用物品。Fit 套件结合了任天堂为任天堂 Switch 制作的优秀纸板制作套件 Labo 的主题，以及现有的用于不相关的任天堂游戏 [Ring Fit Adventure](https://ringfitadventure.nintendo.com/) 的 Ring-Con 配件，加上一系列定制硬件，将所有这些结合在一起。该硬件感应静止自行车上的节奏，观察用户挤压手持车轮控制器，并将这些输入转化为控制器上的按钮按压来玩游戏。

![](img/a8068ce4cad390ffc363236138132727.png)

Shoulder button pusher in green

这个项目最吸引人的部分是 TAPBO 模块，它可以使 Joy-Con 控制器适应远程输入。该模块包括电子器件、致动器和一个巧妙的机械设计，使其可以安装在环形控制台上，代替未经修改的 Joy-Con。有一个青少年分线板，它也有一个 XBee 模块，可以远程接收输入并驱动一对伺服系统。整个模块在视频中从 4:42 开始[详细描述。](https://youtu.be/UN6iYyGgqmA?t=282)

在机械方面，TAPBO 依靠一对凸轮驱动的臂，将旋转伺服运动转化为线性动作来按压肩部或面部按钮。该模块通过添加的灵活电阻直接测量 Ring-Con 的弯曲度，并通过 Zigbee 从固定自行车中嵌入的另一个模块接收节奏信息。当这些输入超过设定的阈值时，它们驱动伺服系统按下适当的控制器按钮来加速或使用物品。

我们非常重视这个项目的技术方面，但这大大低估了[Mike]制作的文档的精美和易懂程度。它包括一个定制包装的 TAPBO Amiibo，等等。检查完整的视频，以获得该项目的完整范围。

 [https://www.youtube.com/embed/UN6iYyGgqmA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UN6iYyGgqmA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

