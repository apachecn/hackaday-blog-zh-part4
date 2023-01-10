# 鱿鱼游戏的最后期限工程

> 原文：<https://hackaday.com/2022/04/14/engineering-on-a-deadline-for-squid-game/>

如果你问我们一个在期限内设计和建造的史诗故事，我们会想到的最后一个地方是一个视频。然而，我们在这里，在很大程度上感谢[的史诗般的技能之一【威廉奥斯曼】](https://www.youtube.com/watch?v=hdt18p-VMmQ)。

当一个 YouTube 名人让你处理一个不可能完成的项目时，你会怎么做？如果你是威廉，你会说“好的”，然后再考虑细节。在这种情况下，它是著名的 YouTuber [Jimmy Donaldson]，又名 *MrBeast* ，他正在计划他自己版本的*乌贼游戏*。在这个版本中，没有人死亡，但一些玩家确实带着大量现金离开。

前提很简单——用动作感应炮塔“杀死”人，就像节目里的那个。问题是这部剧拥有电影魔法的所有工具——多重拍摄、视频剪辑，应有尽有。[威廉]的任务是处理一个现场活动，有 456 个真实的人，没有重做。哦，整个事情必须在 3 周内准备好。

[![](img/e3e369cf54e922e0d2cd4262ab2bd019.png)](https://hackaday.com/wp-content/uploads/2022/04/beastgame_detail.jpg) 杀戮也必须相当明显——我们说的是到处喷射的模拟血液。所以[威廉]决定制造他自己版本的血炮——好莱坞几十年来一直用这种装置来模拟枪伤。气动系统的初期工作被证明是不切实际的。这时，他戴上了经理的帽子——雇人帮他解决问题。你可能会认出他们中的几个——[【艾伦·潘】出场](https://hackaday.com/2015/10/14/thors-hammer-build-recognizes-its-masters-hand/)，还有[化学天才【奈尔德】](https://hackaday.com/2020/08/04/nilered-makes-superconductors/)。甚至[【the backyardscientist】也出现](https://hackaday.com/2017/10/26/thermite-creates-a-sword/)。

视频记录了[威廉]的旅程，在截止日期前制作并交付了 500 份电路板。因此，没有太多关于系统内部工作的细节。一对 AA 电池馈入升压转换器，为 ESP-WROOM-02 模块内的 ESP8266 供电。ESP 驱动几个 led 和一个 MOSFET。MOSFET 连接到展览的明星-一个 [MGJ 火线引爆器](https://electricmatch.com/pyrotechnics/see/6/5/mjg-firewire-initiator)-想象它是一个类固醇模型火箭点火器。始作俑者藏在一袋 YouTube 友好的黄色“血液”后面。当系统被命令杀人时，引爆者打开袋子，血喷得到处都是。

为一个设备这样做并不坏，但我们遵循的是*乌贼游戏*规则——这意味着 456 个竞争者。此外，还有 100 部 iPhones 为员工安装了定制的 kill 应用程序。再加上一台中央服务器，你就有 557 台设备在 2.4 GHz 和 5.8 GHz 上近距离测试。我们是否提到过[William]从未使用过多的设备进行过测试？

想知道会发生什么吗？看看下面的视频吧！

 [https://www.youtube.com/embed/hdt18p-VMmQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hdt18p-VMmQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

