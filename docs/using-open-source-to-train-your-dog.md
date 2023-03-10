# 使用开源软件来训练你的狗

> 原文：<https://hackaday.com/2020/10/31/using-open-source-to-train-your-dog/>

一个[开源的犬类训练研究工具](https://openhardware.metajnl.com/articles/10.5334/joh.27/)刚刚由【Walker Arce】和【Jeffrey Stevens】在内布拉斯加大学林肯的[犬类认知和人类互动实验室](https://dogcog.unl.edu) (C-CHIL)发布。

我们没有意识到狗的训练研究技术是如此高科技。与巴甫洛夫相反，操作性条件反射给予积极的奖励，在这种情况下，是狗的款待，以加强想要的行为。传统的操作性条件反射涉及手动分配零食，并且确实存在一些使用无线遥控的设备，但是它们仍然是手动操作的，并且可能给出不一致的结果(太多或太少的零食)。没有任何现有的方法可以自动化这个过程，所以这个团队决定纠正这种情况。

他们采用了一种商业零食分配器，并为其加装了一个接口板，该接口板可以接入分配器的红外传感器，以检测料斗是否在移动以及零食是否已被实际分配。接口板连接到一个 Raspberry Pi，它是运行测试的全功能平台。在这个演示中，它连接到一个 HDMI 监视器，检测狗鼻子的触摸，以与屏幕上的事件相关联。未来的研究人员不必重新发明轮子，只需重新设计测试本身，因为[Walker]和[Jeffrey]已经在实验室的 [GitHub 库](https://github.com/unl-cchil/canine_treat_dispenser)上开源发布了所有的固件和硬件。

在下面的短视频剪辑中，观察这只狗用鼻子轻拍白点时得到的奖励。如果你仔细观察，在某一点上，狗也短暂地移动了鼠标指针。我们预测到明年，C-CHIL 的研究人员将会让这个家伙画画和玩跳棋。

 [https://www.youtube.com/embed/veKvqE5ipu4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/veKvqE5ipu4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这不是我们这个月看到的第一个动物行为黑客。看看训练鸟儿清理瓶盖的喂食器。