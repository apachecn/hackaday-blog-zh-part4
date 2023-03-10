# 拆卸:吊索适配器

> 原文：<https://hackaday.com/2021/09/29/teardown-sling-adapter/>

消费电子领域总是处于不断变化的状态，但这一点在娱乐设备领域表现得最为明显。在短短几十年的时间里，我们从 24 英寸 CRT 上的粒状 VHS 磁带到 70 英寸 LED 面板上的 4K 蓝光，到头来却把大部分观看时间花在了观看智能手机上的流媒体内容上。也没有放缓的迹象。事实上，他们可以说是在加速。当然，你几年前买的 4K 电视可能有 HDR，但它有 HDMI 2.1 和杜比视界吗？

因此，毫不奇怪，易贝到处都是过时的视听设备，只需花上几分钱就能买到。以我们今天看到的 SB700-100 吊索适配器为例。[这款设备在 2010 年发布时的零售价为 99 美元](https://www.ecoustics.com/products/dish-network-sling-adapter-tv/)，它让 Dish Network 用户能够将保存在 DVR 上的内容流式传输到智能手机或平板电脑上。在网飞推出他们的 Android 应用之前，能够通过互联网在移动设备上观看完整的电视节目和电影是一个巧妙的技巧。但是今天，它几乎和 HD-DVD 驱动器一样有用，这就是为什么你只需花 5 美元就可以买到一台。

[![](img/d1671a76854b9201fbfa5ebd7b4df32a.png)](https://hackaday.com/wp-content/uploads/2021/09/slingadapter_dvr.jpg) 当然，这只是一笔交易，如果你真的能用这款设备做点什么的话。当代评论似乎对这个东西实际上是如何工作的非常谨慎，只是简单地解释说，将它插入你的碟中，DVR 赋予了机顶盒迄今为止闻所未闻的功能。他们向读者保证，表演非常精彩，如果他们决定一头扎进这个勇敢的新世界，你最喜欢的电视节目和电影最终可以在浴室里欣赏，那 99 美元是值得的。

现在，在它发布十多年后，我们将打开 SB700-100 吊索适配器，看看我们能否弄清楚这项不寻常的技术实际上是如何工作的。它扔办公室最新一集的日子可能结束了，但也许这只老狗还能学到一些新技巧。

## 深红色的谜

可以肯定的是，吊索适配器是一个非常不寻常的设备。它没有控制器，没有显示器，它与外界的唯一联系是永久连接在设备后部的短 USB 引线。然而，尽管它看起来很简单，但它的散热金属外壳暗示着它的梅洛引擎盖下有相当大的原始能量。即使在今天，这种设备看起来也令人印象深刻的高科技，这可能解释了为什么前十年的评论者对它如此着迷。如果吊索适配器现在看起来像某种先进技术，想象一下他们在 2010 年对它的看法。

[![](img/6155af085ca459d8c6131e882bb0f053.png)](https://hackaday.com/wp-content/uploads/2021/09/slingadapter_open.jpg)

打开设备后，我们看到的是热化合物的健康应用，这证实了金属网格外壳本质上是一个巨大的散热器。随着四个螺丝的拆除，70 毫米 x 80 毫米的 PCB 可以从机箱中取出，令人惊讶的是，USB 引线可以从原来是一个母 Mini-B 插孔中断开。就拆卸而言，[肯定不会比这个](https://hackaday.com/2021/08/17/teardown-3d-printed-space-shuttle-lamp/)更容易。但是当然，我们仍然要弄清楚这个板子是做什么的。

在我走得更远并可能损坏某些东西之前，我决定将该板插入计算机以查看会发生什么是明智的。[我们在之前的拆卸](https://hackaday.com/2020/06/22/teardown-wonder-bible/)中发现了意想不到的 USB 功能，但尽管如此，我承认我还是被`lsusb`的输出震惊了。

[![](img/e5c02bc5ba3f2a54492d67febfa324a9.png)](https://hackaday.com/wp-content/uploads/2021/09/slingadapter_lsusb.png)

令人难以置信的是，吊索适配器立即被识别为 [Cypress CY7C68013 EZ-USB FX2 开发套件](https://www.cypress.com/documentation/development-kitsboards/cy3681-ez-usb-fx2-development-kit)。EZ-USB FX2 将一个[英特尔 8051 微控制器与一个高速 USB 2.0 接口](https://www.cypress.com/products/ez-usb-fx2lp)配对，该接口旨在促进批量传输，并具有在运行中重新获取自身的能力。稍加挖掘就会发现，芯片的固件通常是从主机系统下载，并在上电时复制到 RAM 中，然后执行代码，并根据新应用的需要重新调整 USB 参数。

似乎偶然地或以其他方式，Sling 适配器的默认状态是将其自身作为开发板进行广告，直到 Dish DVR 提供了固件映像。我的第一个想法是，设备[可能是作为一种安全加密狗](https://hackaday.com/2017/12/19/drm-workarounds-save-arcade-cabinet/)运行的，DVR 会上传一些代码给它，然后等待它执行后是否得到适当的响应。但是如果它只是计算一些校验和的话，这个设备就不会产生很明显是为其设计的那种热量；显然有一些严重的数字运算正在进行。

## 片上 H.264

在用棉签和异丙醇度过一段美好时光后，我们有了答案。在厚厚的热化合物层下面隐藏着一个 Magnum DX6225-LHG00-A3，[旨在将 MPEG-2 视频转码为较低分辨率的 H.264 流](https://www.digitaltvnews.net/?p=14052)，适合在早期的智能手机和平板电脑上播放。它旁边的两个相同的芯片显然是外部内存，但我一直有一些麻烦，以确定它们。我的最佳猜测是，他们是美光 8 MB 的 MT47R64M16 的一些替代品牌，但即使是 2010 年，16 MB 的内存似乎相当低。

[![](img/8fb5ef149b5b02e79e83b644a0aea5c4.png)](https://hackaday.com/wp-content/uploads/2021/09/slingadapter_magnum.jpg)

结合 EZ-USB FX2 的批量传输功能，事情开始变得有意义了。Dish DVR 通过 USB 将存储在其硬盘上的 MPEG-2 视频推送到 DX6225，在 dx 6225 中，视频被实时转换为移动友好格式，并被发送回机顶盒，最终通过网络进行分发。

这是一个我们今天仍在使用的概念，尽管工作负载有很大不同。Coral USB 加速器和英特尔神经计算棒本质上是对 Sling 适配器的现代回答；处理机器学习的计算工作量的插件模块，以便主机系统可以专注于后勤和用户界面。这有助于性能受限的“边缘”平台，如 Raspberry Pi 处理高帧率计算机视觉等任务，早在 2010 年，它就允许 Dish 用户在手机上播放视频，而不会使 DVR 陷入困境。

## 新的行军命令

我知道你在想什么。如果 Sling 适配器的 USB 端真的是基于 Cypress CY7C68013 EZ-USB FX2 开发套件，那是不是意味着你可以花 5 美元买一个这样的东西，然后将新代码加载到它的 8051 MCU 中？至少到目前为止，答案似乎是肯定的。但和往常一样，细节决定成败。

[在编译开源 cyusb linux 套件](https://github.com/Ho-Ro/cyusb_linux)之后，我成功地连接到 EZ-USB FX2，并将其中一个演示固件映像上传到 RAM 中。在重编 Sling 适配器之后，在计算机上运行的程序能够与固件建立环回连接。虽然我还没有亲自测试过，但你应该可以使用 Cypress 的官方(也是相对现代的) [EZ-USB FX3 软件开发工具包开始编写自己的固件，因为它向后兼容 FX2。](https://www.cypress.com/documentation/software-and-drivers/ez-usb-fx3-software-development-kit)

[![](img/933f4737f2d258284b60e98d10d39f44.png)](https://hackaday.com/wp-content/uploads/2021/09/slingadapter_programming.png)

Note the changed product ID and device description after firmware upload.

现在是坏消息。还记得我说过吊索适配器没有任何控制或显示吗？不幸的是，这并没有使它成为一个非常令人兴奋的实验平台。当然，你可以让它运行你自己的代码，但这是一台为非常特定的目的而建造的机器，所以代码实际上能做的不多。虽然如果你设法为这些东西创建一个定制的固件，做一些有趣的事情，[我们当然很乐意听到它](https://hackaday.com/submit-a-tip/)。