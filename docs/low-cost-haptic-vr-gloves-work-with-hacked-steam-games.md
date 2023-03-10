# 低成本触觉虚拟现实手套工作与黑客蒸汽游戏

> 原文：<https://hackaday.com/2022/01/10/low-cost-haptic-vr-gloves-work-with-hacked-steam-games/>

[Lucas VRTech]在制造用于 Steam VR 游戏的[力反馈型触觉手套](https://hackaday.io/project/178243-lucidgloves-vr-haptic-gloves-on-a-budget)方面取得了一些重大进展。这个想法非常简单:手指的末端连接到一根缆绳上，缆绳从一个装有弹簧的卷轴中拉出；用来挂身份证的那种。

线轴本体可以旋转，但是从其突出的销与协同定位的伺服马达的臂接合。这将产生一个可编程的停止位置。但是这是一个很难停止的动作，用目前的硬件不可能精确地检测到停止的时间，也不可能控制它推动的力度。这些特性并不难实现，只不过是用一些定制的机电一体化技术再多开发一点点而已。

目前的原型侧重于成本，作为早期开发平台非常好。通过利用 3D 打印和易于采购的现成零件；就一把(咯咯！)的电位计，一些伺服电机和一个来自任何数量的 ESP32 开发板，你就大功告成了。真正的工作是在软件方面，因为游戏本身需要修改才能与 VR 手套硬件一起玩球。这是通过一个他们称之为 [OpenGloves](https://github.com/LucidVR/opengloves-driver) 的自定义 steam 驱动程序和社区开发的每个游戏的 mods 的组合实现的。现在有几个游戏可供测试，所以这肯定是我们中的一些人可以在一个周末内完成并参与其中的事情。

手套支架和每个手指单元的硬件资源可以在[项目 GitHub](https://github.com/LucidVR/lucidgloves) 中找到，以及 Arduino 的 ESP32 资源。

对于其他一些与触觉相关的灵感，这里有[一个力反馈鼠标](https://hackaday.com/2020/05/17/force-feedback-mouse-really-shakes-things-up/)，对于一个更加放手的反馈，我们有一个[风爆器项目](https://hackaday.com/2018/09/16/wind-blaster-haptic-feedback-thatll-make-you-recoil/)。

 [https://www.youtube.com/embed/ZTzn37Usa-U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZTzn37Usa-U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[iraqigeek]的提示！