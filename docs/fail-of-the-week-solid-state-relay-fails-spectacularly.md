# 本周失败:固态继电器惊人地失败了

> 原文：<https://hackaday.com/2018/08/24/fail-of-the-week-solid-state-relay-fails-spectacularly/>

如今很多时候，我们黑客似乎有点像糖果店里的孩子。点击一下鼠标就能买到这么多很酷的设备，很容易先订购，然后再问质量问题。大多数情况下，这一切都很顺利，但采购有问题的组件的主要风险是，当某个部件出现故障时，一个下午的黑客攻击就泡汤了。

然而，当你将你的项目连接到家庭电源时，风险要高得多，正如[Mattias Wandel]最近了解到的，当时控制他的热水器的固态继电器发生故障，结果几乎是悲剧性的。泰然自若地无视他刚刚发现他几乎烧毁了自己的房子的事实，[Mattias]参观了犯罪现场，并交付了受害者的尸体，一辆 Fotek SSR-25DA。看起来他把它安装得很好，给了它一个像样的散热器，但这东西还是烧着了。继电器的印刷电路板的唯一完整的残留物是安装在后板上的三端双向可控硅开关。[Mattias]怀疑 PCB 痕迹在他度假回来时变热了，它控制的热水器打开了；在装满冷水的水箱中，这两种元素都是必需的，并且需要足够的电流来熔化高压走线上堆积的焊料。随着焊料的消失，痕迹也消失了，剩下的就是历史了。这是一个可怕的场景，值得一看，如果你有任何 SSR 控制负载接近其额定极限。

这个故事的寓意是:如果可能的话，购买高质量的组件并[测试它们](https://hackaday.com/2012/12/20/mains-rated-solid-state-relay-test-box/)；有疑问时，减额；确保燃烧的部件不会点燃其他东西。同时，你会想复习[防火的基本知识](http://hackaday.com/2016/12/06/hack-safely-fire-safety-in-the-home-shop/)。

 [https://www.youtube.com/embed/FV9t1GFVbhU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FV9t1GFVbhU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

