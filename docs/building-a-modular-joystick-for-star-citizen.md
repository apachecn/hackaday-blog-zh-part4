# 为《星际公民》制作模块化操纵杆

> 原文：<https://hackaday.com/2022/07/21/building-a-modular-joystick-for-star-citizen/>

游戏杆非常适合玩游戏，但有时很难找到适合你个人游戏风格的游戏杆。[【谢妮】开发了 TinkerJoy 来满足他们自己的需求](https://www.reddit.com/r/TinkerJoy_Sigma/comments/vulue7/looking_good_semi_serious_effort_at_a_thumbpanel/)，同时给它一个模块化的设计，使其易于定制。

[![](img/772b2be8c890ba197ce54fc332fb8518.png)](https://hackaday.com/wp-content/uploads/2022/07/tinkerjoy_detail.jpg) 它是围绕一个金属核心建造的，根据用户的喜好附有 3D 打印面板。除了主体面板，触发器组件和按钮面板等部件可以四处移动和调整，以适应不同的游戏或不同的玩家。

一个测试单元已建成右手配置，具有四个按钮和两个开关滑块。除了主要的 X 轴和 Y 轴，它还有一个通过旋转操纵杆激活的 Z 轴，以及一个模拟制动器。每一个好的操纵杆都必须有一个触发器。目前，电子设备还没有集成。相反，STM32 BluePill 板位于控制杆的顶部，可以读取所有的控制并与 PC 对话。测试设置看起来工作良好，谢妮在《星际公民》中测试了设备。

构建自己的硬件的好处是，你通常可以自己做得更好。毕竟，出于经济和规模的原因，公司通常不得不为第 5-95 百分位进行构建。

 [https://www.youtube.com/embed/GRx8r043GW4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GRx8r043GW4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

