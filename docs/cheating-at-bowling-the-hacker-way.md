# 保龄球作弊，黑客的方式

> 原文：<https://hackaday.com/2019/11/24/cheating-at-bowling-the-hacker-way/>

任何去过保龄球馆的人都会知道心灵感应控制保龄球的首选(但无效)技术。[马克·罗伯]和[詹姆斯·布鲁顿]决定改变这种情况，他们发明了一种保龄球，只需倾斜身体，就可以遥控(而且很小心)。

他们从一个标准的保龄球开始，那是在车床上切成两半并挖空的。一根横梁位于球的中心线上，安装在每一半的轴承上，让球绕着它旋转。转向是通过移动重心完成的，通过重型伺服系统左右移动悬挂在横梁下方的钢摆。伺服系统由 Arduino 控制，IMU 检测球的方向。电源由 RC Lipo 电池提供。无线控制器是一个偷偷摸摸的小设备，贴在[Mark]的背上，用衣服盖住，通过 IMU 模块检测他倾斜的距离来控制球的方向。大脑是 Arduino Mini，NRF24L01 提供射频链接。

虽然这不是一个容易的构建，但它是一个相当简单的电子系统，具有现成的电子模块和性能板。天才在于实现它的娱乐价值。当[马克]“心灵感应”控制球时，孩子们脸上的表情，在炫耀他没有天生能力的事实后，绝对是无价的。前美国宇航局工程师马克·罗伯(Mark Rober)因其在 Youtube 上的热门视频而出名，这些视频涉及一些很酷的项目，如针对包裹窃贼的闪光诱杀装置(T1)和液体沙子热水浴缸(T3)。前玩具设计师詹姆斯·布鲁顿以他的机器人技术闻名，他展示了 [OpenDog](https://hackaday.com/2018/06/11/james-bruton-is-making-a-dog-opendog-project/) 和[功能星球大战机器人](https://hackaday.com/2016/12/10/speed-run-james-brutons-star-wars-builds/)。

对我们来说，这个黑客是一个娱乐和激励的完美例子，对年轻人和老年人都是一个强大的组合。休息过后，请观看精彩视频。

 [https://www.youtube.com/embed/wM5NHC97JBw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wM5NHC97JBw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

