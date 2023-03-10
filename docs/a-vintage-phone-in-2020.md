# 2020 年的老式手机

> 原文：<https://hackaday.com/2020/01/14/a-vintage-phone-in-2020/>

当我们在 2020 年打电话时，最有可能的是通过蜂窝或基于 IP 的连接使用智能手机，而不是通过一对铜线连接到交换机的传统工具。随着我们不可阻挡地走向一个无线世界，在这个世界中，电话线只作为宽带互联网的载体，人们很容易忘记过去一百多年来导致现在的电话技术。

[![The iconic British telephone of the 1960s and 1970s, the GPO model 746\. Mine is from 1971.](img/1d3e9421a9f55eba3e9cacb58464b46d.png)](https://hackaday.com/wp-content/uploads/2019/12/GPO746-on-desk.jpg)

The iconic British telephone of the 1960s and 1970s, the GPO model 746\. Mine is from 1971\. (That isn’t my phone number)

从某种意义上说，你的电话墙上插座没有忘记。如果你喜欢旧手机，你仍然可以拥有一部，想象自己在一部 20 世纪 50 年代的电影中，一边说话，一边将手机线绕在手指上。

随着我们无情地前进，值得考虑我们还能这样做多久。如果一切顺利，我将在几周内收到一个新的光纤连接。沿着一片玻璃，将会出现我目前所能梦想的更快的互联网，我希望我们的电话提供商放在它末端的盒子将有一个电话插座，它只是一个专用 VOIP 客户端的前端。毫无疑问，它适用于我的数字电话答录机，但它还适用于一台 50 年前的老式电话吗？如果我不得不侵入这部旧手机，我最好现在就弄清楚，以防我不得不把它连接到其他东西上以保持它的通信。

## 电话是如何工作的？

[![A grotesquely simplified schematic of a dial phone. In this diagram SW2 is open and SW3 is closed, so the handset is off the cradle but the dial is not in use..](img/88209f39c6f440df8fb0c11a62f08ff1.png)](https://hackaday.com/wp-content/uploads/2019/12/simple-phone-schematic-1.jpg)

A grotesquely simplified schematic of a dial phone. In this diagram SW2 is open and SW3 is closed, so the handset is off the cradle but the dial is not in use.

起源于 20 世纪初的无源器件的伟大之处在于其原理相对容易理解。像我的 GPO 746 这样的手机包含许多智能电路，可以提供更好的音频，并保护它免受线路故障、过压和其他事故的影响。但是它最基本的操作可以用类似我们所描绘的简化示意图来解释。

左边是听筒，一个碳麦克风和一个耳机串联在一起。当听筒离开支架时，SW3 闭合，因为线路上有一个 DC 电压，所以有电流流过听筒。线路上的任何音频都可以在耳机中听到，任何对碳麦克风的讲话都会改变电流，并产生音频信号作为回报。

[![A telephone dial, front and rear. Daderot [CC0]](img/26e7b5681dbd60ecf5d79a13eb79ad0f.png)](https://hackaday.com/wp-content/uploads/2019/12/1024px-Automatic_Electric_821C_rotary_dial_-_Telephone_Museum_-_Waltham_Massachusetts_-_DSC08171.jpg) 

一个电话，前后拨号。可以看到两组弹簧触点，左边一组用于脉冲拨号，右边一组用于接通电话听筒上的低电阻。调速器斜对着机械装置，驱动它的齿轮也用来操作左手触点。当听筒放在支架上时，SW3 被打开，没有 DC 电流通路，但是通过电容器 C1，有一个交流通路到铃 B1。因此，交换机可以通过在 DC 稳定电压之上发送交流电压来响铃。

SW1 和 SW2 是拨号盘中的联系人，由于低于某一年龄的[人可能不熟悉拨号盘电话](https://www.youtube.com/watch?v=8HyyAlcoUXo)已经成为一个病毒式的迷因，所以有必要为他们解释一下拨号盘的操作。在放开之前，用户将弹簧加载的盘旋转到代表所需数字的点。它以一个调节器设定的恒定速率返回，当它这样做时，它闭合一组这里标记为 SW2 的触点，以在手机上接通低电阻，并通过齿轮传递它的其他触点 SW1。其作用是中断线路电流，[产生一系列由所拨号码](https://en.wikipedia.org/wiki/File:Rotary_Dial,_Dialing_Back_with_LEDs.ogv)设定的脉冲，这些脉冲最初用于机械交换，每个脉冲使开关设备前进一步。

这种电路的一个有趣的副作用是，有些电话可以通过快速按下支架来模拟拨号。在一些付费电话上，这提供了一种绕过硬币盒电路的方法，硬币盒电路使拨号无效。(我记得我大学的一些学生因为这样做而惹上麻烦。)谁需要 2600 Hz 的音调来欺骗电信公司！

## 插座的另一面

了解了电话之后，我们如何模拟一条电话线来连接它呢？为了找到答案，我带着 GPO 746 在黑客空间呆了一个晚上。

[![My basic fake phone line simulator, which should serve as a template for something a little more useful.](img/a2e34d124c64f31689adb42ce64a7375.png)](https://hackaday.com/wp-content/uploads/2019/12/simple-phoneline-schematic.jpg)

My basic fake phone line simulator, which should serve as a template for something a little more useful.

网上搜索会告诉你，电话线携带一个稳定的 DC 电压和一个间歇的交流电压来操作电铃。进一步研究发现，这些电压都可以是 50 伏，DC 电流不应该超过 50 毫安。因此，一个好的起点是将台式电源设置为 50 V，用一个 1kω电阻来限制电流，并模拟几英里电话电缆的电阻。有了电阻器，对线路的任何改变都只能产生 50 mA 的电流，因此降低了损坏的可能性。将它连接到 746，麦克风拾取的声音可以在耳机中听到，如果我愿意，我可以在 1kω电阻后检索音频。

[![Experimenting with driving a dial phone on the bench.](img/7ca81e37b9a8b26b9d3540ce1edd84e9.png)](https://hackaday.com/wp-content/uploads/2019/12/gpo746-on-bench.jpg)

Experimenting with driving a dial phone on the bench.

类似地，将听筒放在支架上，我可以施加交流电压并响铃。我的交流变压器略低于 50 V，但它确实可以在更小的体积下工作。我仍然缺乏任何感应拨号或支架的手段，为此我需要感应 50 毫安 DC 电流的存在或不存在。当年真正的 GPO 交换机将通过与线路串联的继电器来实现这一点，所以我使用了一个小型继电器。在这一点上，我了解到继电器在其闭合和释放电流上有一个滞后曲线，所以它不像我希望的那样可靠或快速。我开始明白为什么电信电路使用簧片继电器。将来我将不得不使用电流感应电阻和晶体管来完成这项工作。

为了让这个项目真正发挥作用，我必须注意我的两个 50 V 电源，可能需要一点升压转换器和振荡器来产生我的交流响铃驱动，然后我需要对微控制器进行编程，以处理挂机和摘机，以及将脉冲流解码为数字。我可能还必须注意我的音频源和来自麦克风的音频之间的相位关系，因为在某些情况下，反馈可能会成为一个问题。一旦我掌握了这些东西，我将能够制造一个位于标准英国电信主插座后面的单元，并提供与我选择的任何东西的连接，无论是 GSM 模块还是单板计算机上的 SIP 客户端。这样，在未来的几十年里，我仍然可以使用我的 GPO 746 拨号电话。