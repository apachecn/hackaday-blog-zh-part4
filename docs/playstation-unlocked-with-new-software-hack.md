# PlayStation 通过新软件破解解锁

> 原文：<https://hackaday.com/2021/03/15/playstation-unlocked-with-new-software-hack/>

最初的 PlayStation 现在可能快 30 岁了，但这并不意味着黑客已经放弃了对它的蚕食。[由[Marcos Del Sol Vives]发布的一个新漏洞允许用户在这款经典主机的所有早期硬件版本上运行复制的游戏](https://orca.pet/tonyhax/)，而你需要触发它的所有东西就是一份*托尼·霍克的职业溜冰者 2*。

这个漏洞被恰当地命名为 tonyhax，它利用了在*托尼·霍克* 2、3 和 4 的“创建溜冰者”模式中发现的经典缓冲区溢出。当游戏看到存储卡上保存的自定义角色时，它会自动加载名称字段以显示在屏幕上，但结果是开发者没有想到在加载之前检查名称的长度。由于这一疏忽，可以使用一个精心设计的长名称将可执行负载加载到控制台的内存中。

[![](img/fd966604724bf961ad40e3e54474ca62.png)](https://hackaday.com/wp-content/uploads/2021/03/tonyhax_detail.png)

The name contains the memory address of the payload.

有效载荷可以是任何东西，比如自制游戏，但在这种情况下，[马科斯]全力以赴，开发了一个简单的工具，可以解锁控制台的光驱，这样它就可以玩刻录到 CD-r 上的游戏。一旦 tonyhax 漏洞被加载，你只需将正版的*托尼·霍克*光盘换成你想玩的任何刻录的游戏。到目前为止，所有测试过的游戏都运行正常，甚至那些跨多个光盘的游戏也是如此。

[Marcos]不仅提供了准备加载到 PlayStation 存储卡上的保存文件(通过 PC 工具，或在被黑客攻击的 PS2 的帮助下)，还提供了 tonyhax 的完整源代码。这为利用加载其他工具、模拟器和独立游戏打开了大门，但由于 PlayStation homebrew 场景与较新的控制台相比相对有限，因此需求可能有限。

与用于在 PlayStation 上玩盗版游戏的传统物理修改相比，[这种新的软件方法要容易得多](https://hackaday.com/2018/11/05/how-the-sony-playstation-was-hacked/)。期待在不久的将来看到预装了这个漏洞的存储卡登陆你最喜欢的进口网站。

 [https://www.youtube.com/embed/TO6msoWZa2I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TO6msoWZa2I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



【感谢 NeoTechni 的提示。]