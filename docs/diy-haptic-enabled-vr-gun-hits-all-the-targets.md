# DIY 触觉虚拟现实枪击中所有目标

> 原文：<https://hackaday.com/2022/09/17/diy-haptic-enabled-vr-gun-hits-all-the-targets/>

[Robert Enriquez]设计的这款 [VR 触觉枪](https://github.com/robegamesios/VRHapticGun)是将不同的现成产品拼凑在一起，并与 ESP32 开发板结合在一起的结果。结果呢？一个集成了 VR 控制器(意味着它可以在 VR 中被跟踪和使用)的枪架，由于有一个随着每次射击而移动的电机，它可以提供温和的力反馈。

[![](img/76ae6e02e162b69c7fa9e44b6f782be9.png)](https://hackaday.com/wp-content/uploads/2022/09/I-built-a-Haptic-Gun-for-VR-Games-DIY-12-42-screenshot.png) 但这还没完！利用 ESP32 板的 WiFi 功能，该枪还可以响应由[发送的信号，这是一款旨在驱动商业触觉硬件](https://github.com/bhaptics/bhaptics-half-life-alyx)的软件。该软件连接到虚拟现实游戏，并通过网络发送信号告诉枪支正在发生什么，而[罗伯特]的固件对这些信号采取行动。简而言之，每次【罗伯特】在 VR 中开枪，手里的枪都会与游戏事件同步后坐。效果是温和的，但当涉及到触觉反馈时，一点点就可以走很长的路。

事实上，这种实验在业余爱好者的能力范围内是容易和负担得起的，这很好，虚拟现实当然有足够的空间让业余爱好者开辟新的领域，正如我们在低成本触觉虚拟现实手套等项目中看到的那样。

[Robert]介绍了他的枪的设计的每个阶段，解释了他如何将各种方形钉安装到圆孔中，并提供了该项目的 GitHub 资源库中零件和资源的链接。在分页符下面有一个视频游览，但如果你想直接跳到 Valve 的*半衰期的演示:Alyx* ，[这里有一个链接，可以在](https://youtu.be/5z2f2qFMsvU?t=619)的 10:19 测试点火。

有许多改进等着我们去做，但是[罗伯特]绝对理解让某些东西工作的价值，即使它有点粗糙。毕竟，没有什么能像原型一样填写待办事项列表或暴露隐藏的问题。观看视频游览中的所有细节，嵌入在下面。

 [https://www.youtube.com/embed/5z2f2qFMsvU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5z2f2qFMsvU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

