# 紧凑型 M&M 分拣机随处可见

> 原文：<https://hackaday.com/2021/06/20/compact-mm-sorter-goes-anywhere/>

让我们面对现实吧——吃不同颜色的糖果，比如 M&Ms 或彩虹糖，如果你先按颜色分类，会更有趣一点。不好玩的部分是必须手工完成。[Jackofalltrades_]决定为工程类解决这个由来已久的问题，因为它太棒了，而且它满足了项目对传感、驱动和自主排序的要求。我们大胆猜测，它也满足了[Jackofalltrades_]对巧克力的需求。

它是这样工作的:M & Ms 巧克力豆被一个接一个地挑选出来，放入暗室进行颜色检查，然后根据结果分配到合适的小房间。[Jackofalltrades_]不负众望，用 RGB LED 和光敏电阻构建了一个颜色检测系统。RGB LED 以最大亮度依次发出红光、绿光和蓝光，并从光电池读取电压读数来判断糖果的颜色。开始时，机器需要每种颜色读入一个并存储为参考。然后，它可以对整袋进行分类，将每个 M&M 与参考值进行比较，并用每个新的 M&M 更新它们，以创建一种滚动平均值。

我们喜欢这台机器漂亮而紧凑的设计，它是为了最大限度地发挥 3D 打印机作为少数可用工具之一的作用而设计的。机械设计特别优雅。它巧妙地使用步进驱动旋转，只需要一个部件就可以完成隔离每一个的大部分整个过程，将它传递到暗室进行颜色检查，然后将其分配到下面罐子的正确部分。请务必在休息后观看演示。

需要下一级分类器吗？这里有一个定位和分离糖果涂层巧克力的圣杯的方法——[花生 M &没有得到花生的 Ms](https://hackaday.com/2020/11/08/hey-you-left-the-peanut-out-of-my-peanut-mms/)。

 [https://www.youtube.com/embed/6h3y0Ycefz0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6h3y0Ycefz0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

