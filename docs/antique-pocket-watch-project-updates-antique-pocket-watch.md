# 古董怀表项目更新古董怀表

> 原文：<https://hackaday.com/2019/12/08/antique-pocket-watch-project-updates-antique-pocket-watch/>

在 Hackaday，我们对钟表有点着迷。也许是与你穿在身上的某样东西有着深刻的个人联系，或者是对终极可靠性的需求。也许这只是对时间本身概念的迷恋。无论是哪种情况，我们似乎并不孤独，因为我们的虚拟世界里有源源不断的与时间相关的项目。为了这篇文章，我们挖掘了 2009 年【波林·磅博士】的 [LED 怀表 1.0(讽刺的是，通过](https://web.archive.org/web/20160322025932/http://www.eng.yale.edu/pep5/pocket_watch.html)[去年关于手表](https://hackaday.com/2018/07/05/leds-make-an-analog-wristwatch/)的帖子！).对我们来说幸运的是，互联网档案馆从互联网垃圾箱中拯救了这个传家宝，这样我们就可以欣赏 Pounds 博士]作品中的工艺。

![](img/bfaa6f7ac85604433101b8e5b3862cf7.png)

Check out the wonderful, spiral routing!

我的天，我们已经走了多远；这个项目发布十年后，黑客可能会选择 3d 打印一个新的可穿戴设备的外壳，但在 2009 年，这将是一个完整的项目！Pounds 博士]选择使用古董[埃尔金怀表](https://en.wikipedia.org/wiki/Elgin_National_Watch_Company)的外壳。即使透过模糊不清的演示视频，我们也能想象出因频繁使用而磨损的外壳有多柔软。选择这个特殊的单元是因为它的直径为 50 毫米，为 44 毫米的双面 PCBA 留下了足够的空间，该双面有 133 个 0603 led(60 秒，60 分钟，12 小时)，PIC 16F946，一个 [ERM](https://www.precisionmicrodrives.com/vibration-motors/eccentric-rotating-mass-vibration-motors-erms/) ，和一个 110mAh LiPo。但真正让 LED Pocketwatch 1.0 与众不同的是用户界面。

ERM 直接安装在机箱后部，以便更好地向外界传导振动。为了最大限度地保证真实性，它会在第二秒闪烁，给人一种电子表像原来一样机械地滴答作响的感觉。最初的怀表设计有一个封闭的盖子，当按下表柄时，盖子就会打开。Pounds 博士]将一个按钮和编码器与杆的末端(在 PCBA 上)集成在一起，因此该设备可以意识到这种相互作用；当盖子打开时，它会唤醒设备，在 led 上显示时间。真正令人难以置信的是，他还集成了一个微型旋转编码器，所以当按下阀杆时，你可以旋转它来设置时间。这一切都非常优雅地集成在一起，并立即可用。

![](img/e1c1dad11231f306fd61a28f8601be2a.png)

在这一点上，我们想链接到来源，详细的图纸，或 CAD 文件，但不幸的是，我们没有找到任何。如果这给了你灵感，看看我们过去发布的一些[其他](https://hackaday.com/2016/09/15/hackaday-prize-entry-neopixel-pocket-watch/) [怀表](https://hackaday.com/2012/11/30/led-pocket-watch-2/)。如果你对 LED Pocketwatch 1.0 的现场演示感兴趣，请在休息后查看原始视频。

 [https://www.youtube.com/embed/lex53AY7Fmo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lex53AY7Fmo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

