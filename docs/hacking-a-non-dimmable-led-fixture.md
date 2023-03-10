# 黑掉不可调光的 LED 灯具

> 原文：<https://hackaday.com/2021/02/24/hacking-a-non-dimmable-led-fixture/>

对于我们大多数人来说，拥有不可调光的 LED 灯泡但需要可调光的解决方案很简单，就是开车去商店买合适的灯泡。但这看起来很无聊，更不用说浪费了，所以当[Leo Fernekes]面临这个问题时，他想办法让一个不可调光的灯泡变得可调光。

公平地说，这次黑客攻击也有财务方面的原因。[Leo]有一堆便宜的不可调光的灯具，他想投入使用。他从拆卸和逆向工程一个灯带开始，灯带只包含一个发光二极管和一个小型降压转换器。他对电路的分析使他想到了调光的解决方案:在 led 周围插入一个 MOSFET 作为分流器。此外，增加一个二极管来隔离 led 和电流调节器，可以通过微控制器对灯进行简单的 PWM 控制。

就像这些事情的典型情况一样，情况很复杂。[Leo]发现定时问题导致 led 闪烁；修复方法是添加一个同步电路，巧妙地利用了他为电路选择的 PIC16 微控制器内的触发器。他的原型包含了这些修改，加上一个支持建筑照明控制 DALI 协议的接口。像往常一样，[Leo]很快指出，将线电压混合到您的项目中并非没有风险，他会尽力减轻风险。和他的项目一样，[Leo]给出了恰到好处的细节来理解他设计背后的理论。

 [https://www.youtube.com/embed/xjb_dSbR2_0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xjb_dSbR2_0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

