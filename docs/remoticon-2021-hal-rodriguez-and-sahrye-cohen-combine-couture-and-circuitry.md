# REMOTICON 2021 // Hal Rodriguez 和 Sahrye Cohen 将时装和电路结合在一起

> 原文：<https://hackaday.com/2022/03/31/remoticon-2021-hal-rodriguez-and-sahrye-cohen-combine-couture-and-circuitry/>

Amped Atelier 的[Hal Rodriguez]和[Sahrye Cohen]专注于创造具有相当高标准的交互式可穿戴服装。每件衣服都必须漂亮，并且要么可以由穿着者通过一组传感器来控制，要么甚至可以由观众通过蓝牙来控制。在他们过去的创作中，有一件衣服前面有颜色传感器和 3D 打印的刻度，可以改变颜色，还有一件为舞蹈演员设计的飘逸的裤装，使用加速度计根据她的动作制作灯光图案。

Conductive Melody 是一种可穿戴乐器，是[Sahrye]和[Hal]的 Remoticon 2021 演讲的焦点，是为在卡尔加里举行的为期多天的蒸汽聚会 Beakerhead Festival 上的演示而创作的。[Sahrye]和[Hal]真的联手合作了，因为[Sahrye]完全是关于电子和服装的，而[Hal]对合成器和电子音乐感兴趣。休息之后你可以在视频中看到演示。

礼服的形式受到了古典乐器和服装类型的启发，这些乐器和服装反过来又受到了启发，比如为竖琴演奏者和钢琴家设计的宽大长袖。因此[哈尔]和[萨拉伊]设计了一件从中臂和上臂垂下的单个大袖连衣裙。袖子上覆盖着激光切割的导电织物花饰，看起来像是对竖琴琴弦的巴洛克式诠释。通过触摸这些轨迹中的一个来演奏一个音符，礼服前面的灯将与音乐同步移动。

[![](img/b07b783ad5bcf2eb6c0bc35aae3a774e.png)](https://hackaday.com/wp-content/uploads/2022/03/Sahrye-Cohen-Hal-Rodriguez-Conductive-Melody-muslin.png)【SAH rye】以服装的大致线条草图开始了《导电旋律》的服装部分，然后画了一张更具细节的最终图。然后她做了一个平纹细布，这是一个服装制作项目的试验版，用薄棉布来帮助想象最终结果。一旦对合身感到满意，[Sahrye]就用上好的布料制作出最终的礼服。我们指的是真正好的面料——这里指的是丝绸。因为正如[Sahrye]所说，如果你打算一次性成功，为什么不尽可能做得好一点呢？我们完全可以支持。

[![](img/bd4591e6b1e6aaf90ff71f06c67d8440.png)](https://hackaday.com/wp-content/uploads/2022/03/Sahrye-Cohen-Hal-Rodriguez-Conductive-Melody-LEDs.png)【SAH rye】说她总是在想一件可穿戴的东西将如何穿戴，以及它将如何清洗或以其他方式护理。紧身胸衣的亮片和半透明部分很好地隐藏了 led 和它们的线路，同时仍然让穿着者感到舒适。

袖子里有一个 MPRP121 电容式触摸传感器和一个 Arduino，Arduino 控制发光二极管，并将信号发送到藏在裙子背面褶边中的树莓 Pi。

Pi 正在运行[钢琴精灵](https://magenta.tensorflow.org/pianogenie)，它可以实时将八个输入变成一架 88 键钢琴。当没有人玩袖子时，灯光有一个柔和的黄色和白色的待机模式，与音乐模式中更乐观的彩虹相比，这种模式慢慢淡入淡出。

我们喜欢看到可穿戴的项目——尤其是如此奇特的创意！—但我们知道他们有多挑剔。在[Sahrye]和[Hal]的经验教训中:不要让你的导电织物痕迹太薄，银导电材料可能会失去不可挽回的光泽。我们只是希望他们不必浪费太多的导电织物或漂亮的蓝色丝绸来发现这一点。

 [https://www.youtube.com/embed/UVHOFXT1_UQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UVHOFXT1_UQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

