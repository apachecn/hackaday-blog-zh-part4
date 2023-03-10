# 不可思议的廉价袖珍焊机得到一个 ESP32 改造

> 原文：<https://hackaday.com/2019/11/04/improbably-cheap-pocket-welder-gets-an-esp32-makeover/>

如果你在某些阴暗的圈子里活动，你可能会注意到近来市场上突然出现了一批便宜得令人难以置信的“袖珍焊机”。它们都是一个主题的变体，大多数都有着极其乐观的规格和最低质量的最小配件。但是它们微小的尺寸和匹配的价格使它们对潜在的焊工不可抗拒，对硬件黑客也有吸引力。

车库里有一个 220 伏的插座等待充电，深知其中的风险，[RC-Cam 先生]购买了一台这种小型焊接机。它的缺点立即显现出来，于是[对焊机进行了彻底的返工](https://www.rc-cam.com/forum/index.php?/topic/4605-sparky-a-little-stick-welder-with-big-features/)。在解决了缺乏接地连接等安全问题后，[RC-Cam 先生]添加了一个颜色匹配的 3D 打印头罩，以容纳一个花哨的新 LCD 触摸屏显示器。支持这一点的是一个带蓝牙的 ESP32，它支持通过密钥卡进行远程控制。他还增加了一个电流感应板，利用焊机的分流器来测量焊接电流。使用华夫饼干铁和毫欧计方便地校准，传感器显示为焊机宣传的 200A 最大值更像 100A。他试图添加一些大型电解质来解决当前的问题，但没有成功。有了像样的毒刺和接地夹，改装后的焊机足以满足他的需求，在这个过程中学到了很多东西。我们称之为黑客胜利。

作为一个题外话，[这个老托尼]最近[做了一个类似的焊机](https://www.youtube.com/watch?v=--1lSmtuyUg)的审查，如果你想更多的内部细节。我们最近还报道了[将音箱转换成 TIG 焊机](https://hackaday.com/2019/09/12/modified-tombstone-welder-contains-a-host-of-hacks/)，这应该更符合你的风格。

 [https://www.youtube.com/embed/wUnMgO00LOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wUnMgO00LOM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

