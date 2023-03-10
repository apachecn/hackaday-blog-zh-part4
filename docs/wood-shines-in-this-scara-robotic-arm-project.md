# 伍德在这个 SCARA 机械臂项目中大放异彩

> 原文：<https://hackaday.com/2018/09/13/wood-shines-in-this-scara-robotic-arm-project/>

[igarrido]分享了一个已经进行了很长时间的项目；[一个木质桌面机械臂，命名为 Virk I](http://automaticartisan.com/2018/09/08/virk-i-open-hardware-scara-robot/) 。木材是澳大利亚黑木，看起来很华丽。[igarrido]很清楚这是一个附带项目，但已决定尝试生产八个单元的小批量产品，以尝试衡量人们对该设计的兴趣。他在业余时间一直忙于切割零件和组装。

除了精美的木材，一些有趣的元素包括中空的旋转接头，这意味着更少的电缆杂乱和更整洁的组装。3D 打印机驱动程序是 CNC 设计的常用工具，Virk I 也不例外。原型由 RAMPS 1.4 板驱动，但[igarrido]解释说，虽然这可以移动关节，但并不理想。要真正有用，驱动程序需要有 [SCARA](https://en.wikipedia.org/wiki/SCARA) 运动学支持，他说据他所知，开源 3D 打印机驱动程序没有提供这种支持。如果没有这样的驱动程序，软件就不知道关节之间是如何物理关联的，而这是进行统一和连贯的运动所必需的。因此，用户必须单独控制电机和关节，而不是能够将手臂作为一个整体移动到特定的坐标。尽管如此，Virk I 可能是推动这一发展所需要的。下面嵌入了一些测试动作的视频，显示了到目前为止一切是如何工作的。

 [https://www.youtube.com/embed/_dSPJBb9PuE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_dSPJBb9PuE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们还记得 SCARA 的另一个机器人手臂项目， [Evezor](https://hackaday.com/2017/05/22/evezor-robotic-arm-engraves-400-coasters/) ，它出色地雕刻并堆叠了 400 个单独编号的杯垫作为功能证明，但它的 Kickstarter 活动需要一个高目标，最终没有成功。[伊加里多]的目标是更容易实现的一组八架私人原型机，如果你有兴趣加入开发团队，他已经在网上[找到了更多的规格和一个 Q & A](http://automaticartisan.com/virk/) 。