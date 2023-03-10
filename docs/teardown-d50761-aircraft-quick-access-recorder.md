# 拆卸:D50761 飞机快速存取记录器

> 原文：<https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/>

每个人都听说过“黑匣子”。它的官方名称是飞行数据记录器(FDR)，是商用飞机上的必备设备。FDR 有助于调查事故或坠机，并专门设计为在飞机被摧毁时幸存。对所谓“黑匣子”的搜寻往往在一架商用飞机失联后主导新闻周期；因为找到它对确定事故的真正原因几乎肯定是必要的。你可能*还没有*听说过的是一个快速访问记录器(QAR)。

[![](img/c4150af4d48f710271526151a59b00b4.png)](https://hackaday.com/wp-content/uploads/2018/09/qar_plate.jpg) 虽然 FDR 最为人所知，但它并不是唯一一种用于航空的记录设备。QAR 可以被认为是罗斯福的非紧急替代方案。虽然从 FDR 中检索数据通常意味着最坏的情况已经发生，但 QAR 是专门设计来方便轻松和定期访问飞行数据以进行研究和维护的。它的数据存储在可移动介质上，由于 QAR 预计不会在飞机失事后幸存，它没有进行物理加固。事实上，现代飞机经常使用消费级技术，如紧凑型闪存卡和 USB 闪存驱动器作为 QAR 中的存储介质。

通过易贝的奇迹，我最近获得了一个老式彭妮&贾尔斯 D50761 快速访问录音机。这是从现已停业的图卢兹国际航空公司的一架飞机上取出的。让我们打开这个相对模糊的设备，看看航空公司信任的硬件中有什么可以帮助确保他们价值数百万美元的飞机在最佳状态下运行。

## 它仍然像坦克一样

[![](img/eb54315852896b5373c4861d05f08725.png)](https://hackaday.com/wp-content/uploads/2018/09/qar_front.jpg) 快速访问记录器可能不会在坠机中幸存，但它仍然是安装在更昂贵的飞机上的一个昂贵的硬件，所以这东西仍然像坦克一样建造。表壳本身最好被描述为一个金属鞋盒:底部和侧面都被熟练地焊接在一起，形成一个连续的金属片，只有顶部的“盖子”可以通过松开周边的 12 个固定螺钉来拆除。

QAR 的前面有一个手柄和一些锁片，所以它看起来像是要滑入某种类型的电子机架，而不是永久安装。在底部有一个电源 LED，但在正常操作期间，其他所有东西都被一个锁定的门覆盖。门的下面是一个用于存储设备数据的磁带的插槽，标记为忙碌和就绪的状态 led，以及一个弹出按钮。有趣的是，弹出按钮是电子的，而不是连接到一个物理机制，但它确实有助于解释为什么 QAR 到达我的驱动器内卡住了磁带。

## 盒式数据

我没费多大劲就从 QAR 上取下了带子，但不幸的是，它没有给我们提供太多的信息。标签上说它是在 12 月 10 日被放入 QAR 的，但是没有说是哪一年。似乎最右边的字段是飞机的注册码:TFELM。搜索结果显示，一架波音 737-300 在 2000 年初仍在飞行，所以*可能是我们的捐赠鸟。*

[![](img/a51844e8a0af6863532080644da1d11b.png)](https://hackaday.com/wp-content/uploads/2018/09/qar_tape.jpg)

这盘磁带本身是一个 3M 的 QIC 数据盒式磁带，从轨道的数量和大致的年份来看，我认为它是一个 DC300XL，可以容纳高达 20 MB 的数据。虽然现在已经过时，但值得注意的是，与现代 QARs 非常相似，D50761 确实使用了当代消费级存储介质。

## 控制板是一个盒子里的逆向计算机

在 D50761 的盖子下面，我们看到了 20 世纪 80 年代工程的华丽展示。三块独立的电路板使用铝制支架堆叠在一起，并用 64 引脚带状电缆互连。有帮助的是，它甚至说每个人在 PCB 丝网印刷上做对了什么。

[![](img/de9d7d401450ca6ea6396ce21a089ec1.png)](https://hackaday.com/wp-content/uploads/2018/09/qar_boards.jpg)

堆栈中的第一层是“接口 PCB”。该板通过三个黑色连接器接受来自飞机上各种传感器和系统的输入，这些输入通过一组电阻，最终到达负责解码信号的各种 IC。其中包括摩托罗拉 LM139J 比较器以及国家半导体 UA9638RM 和飞兆 UA9637ARM，它们都是 RS-422 线路驱动器。然后，来自这些 IC 的信号通过电路板传输到 Z8420AB6 并行 I/O 控制器和 Z8470AB6 UART，它们通过带状电缆将其输出发送到堆叠中的下一个电路板。

 [![qar_interface1](img/81ed8d00925d05561d26a38c8adb0c60.png "qar_interface1")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_interface1/)  [![qar_interface2](img/389a021960c8aec341aadec7464093a7.png "qar_interface2")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_interface2/) 

中间的板是“CPU PCB”，它是系统的 4 MHz Z8400AB6 CPU、Z8410AB6 DMA 控制器和 10 个 HM-6514 芯片的所在地，共 5 KB 的 SRAM。该板还有三个紫外 EPROM 芯片，其中包含计算机的软件。有趣的是，与其他电路板不同,“CPU PCB”除了通过带状电缆之外，与系统的其他部分没有任何连接。

 [![qar_cpu3](img/4eff195a416b6d217461957ce4a078aa.png "qar_cpu3")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_cpu3/)  [![qar_cpu2](img/3157c548075807a19a1053d61275a7cc.png "qar_cpu2")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_cpu2/)  [![qar_cpu1](img/b04c29a4ae311940d339e73d42b4c29f.png "qar_cpu1")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_cpu1/) 

最后，我们有“格式化 PCB”，它通过带状电缆从 Z80 计算机获取数据，并将其写入磁带机。这是唯一一个连接到磁带机本身的板，包含两个以上的 Z8420AB6 并行 I/O 控制器和一个大阵列的摩托罗拉 SN54LS04J hex 反相器。

 [![qar_format2](img/58feac0989696ed837fb608dd86489a3.png "qar_format2")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_format2/)  [![qar_format1](img/e63d3ba8a722bbcd79c36cf179587237.png "qar_format1")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_format1/) 

在这个设备内部发现了一个本质上完整的逆向计算机，这让我想起了我们之前看过的 AH-64A 阿帕奇数据输入面板。虽然在这种情况下，我很惊讶地看到缺乏保形涂层，甚至在振动保护的方式。显然，军用硬件将按照尽可能高的标准建造，但考虑到这种设备是为商用客机设计的，控制电子设备似乎仍然很普通。

## 磁带机是一项了不起的工程

尽管控制部分令人着迷，但磁带机无疑是这场表演的明星。几乎占据了 D50761 内部的所有可用空间，这是一个巨大的设备，尤其是对现代人来说。它的构建也与控制部分大相径庭，因为这里我们看到的不仅是更密集的 PCB 布局，还有其它电路板没有的保形涂层和振动考虑。

从表面上看，这两个组件的制造方式如此不同，但仍封装在同一设备中，这似乎很奇怪，但这可能是 Penny & Giles 将磁带机本身设计成更高的规格，以便可以出售给军方。当它被出售用于民用飞机时，它将简单地与较低等级的控制电子设备配对。

 [![qar_drive1](img/8d638948c3de62cee0c14e7a2d4426b7.png "qar_drive1")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_drive1/)  [![qar_drive2](img/699051d56cad9a3688e14d9b1e6d6ba0.png "qar_drive2")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_drive2/)  [![qar_drive3](img/64a3a8d769a04ab3449c980c8e79c7a8.png "qar_drive3")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_drive3/) 

无论如何，磁带机是一项了不起的工程。称为“驱动和控制 PCB”和“读/写 PCB”的两块板安装在驱动器背面的铰链上，因此您只需卸下前面的两个螺钉，将它们向下折叠，以便于操作。遗憾的是，在今天，真正考虑到测试和维修而设计的电子产品如此罕见。

 [![Hinged PCB](img/759ef3bc34f20bc01f593ec3d6021ffc.png "qar_drive4")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_drive4/) Hinged PCB [![Drive motor](img/e0849f1bfbee003da0eaafa63756fa0f.png "qar_drive5")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_drive5/) Drive motor [![Locking connectors, conformal coating, and hot glued adjustment potentiometers.](img/f19402e7eb3fd45f57e6b50f15ec8d6f.png "qar_drive6")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_drive6/) Locking connectors, conformal coating, and hot glued adjustment potentiometers.

## 电源包括备用电池

案件的其余部分是由电源，其特点是一个相当可怕的线圈除了一些强大的电容器。还有一个 LM123K 5V 3A 稳压器，似乎是负责为控制板供电。有趣的是，在主电源上方的高架“架子”上似乎有某种类型的备用电池。其中一个电池爆裂，不幸的是腐蚀得非常严重，但根据 PCB 上的丝网印刷判断，它可以为 D50761 提供 5V 和 12V，至少一小会儿。

 [![qar_psu1](img/38c658d6df7991bc7cfaa8dbecb59c43.png "qar_psu1")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_psu1/)  [![qar_psu2](img/eccff2cb3a4322ca1189c15b99761032.png "qar_psu2")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_psu2/)  [![qar_psu3](img/687ce2f6c94cb2421950156b123643ab.png "qar_psu3")](https://hackaday.com/2018/10/15/teardown-d50761-aircraft-quick-access-recorder/qar_psu3/) 

这几个电池似乎无法让耗电的磁带机运行相当长的时间，但也许这足以让 QAR 记录下系统在关机前电量耗尽的事实。或者，它可能只是帮助 D50761 度过瞬间的功率波动。

## 可疑的设计

总的来说，我对 D50761 QAR 的设计和构造如此不一致感到惊讶。这看起来像是一个大杂烩，一些组件看起来要遵循严格的标准，而另一些组件则近乎马后炮。

磁带机本身是一个奇迹，但相比之下，它背后的电源看起来像是古老的技术。控制板的布局过于简单，看起来很业余。一些连接器用坚固的锁夹来防止振动，而另一些连接器只是简单地推上去。“备用电池”(因为缺乏更好的术语)看起来特别像是后来版本的设备中添加的东西，而且没有在电池破裂时保护 D50761 的规定似乎是非常欠考虑的。

特别值得注意的是磁带机的边缘连接器。尽管驱动器和连接器本身都有孔，显然是为了让某种紧固件穿过，但都没有使用。这个 edge 连接器是如此的容易丢失，以至于我可以用一个手指就把它移除，这让我很困惑为什么他们没有保护这个连接，尽管它显然是为这个目的而设计的。

## 安慰奖

事实上，我一直在寻找一个“真正的”飞行数据记录器来进行拆卸，但这些似乎并不经常在易贝漂浮。至少不会以知识的名义破解它。搜索仍在进行中，但这个 D50761 QAR 出现了，我想它可能会作为临时替身。

事实证明，这本身就是一个耐人寻味的硬件。虽然没有真正的 FDR 强大，但 D50761 让我们对那个时代本质上非常高端的消费硬件有了一个迷人的了解。这将是有趣的听到任何读者谁可能有经验，更现代的 QAR 系统，以比较他们的当代建设质量。我们也很乐意听到任何可能在鼎盛时期实际使用过这种录音机的人的意见。

如果你想展示一些有趣的硬件，请不要犹豫给我们写信。