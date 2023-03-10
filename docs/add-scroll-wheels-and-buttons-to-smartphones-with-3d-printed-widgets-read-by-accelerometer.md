# 为智能手机添加滚轮和按钮，通过加速度计读取 3D 打印的部件

> 原文：<https://hackaday.com/2019/06/17/add-scroll-wheels-and-buttons-to-smartphones-with-3d-printed-widgets-read-by-accelerometer/>

第一款 LED 数字手表于 20 世纪 70 年代上市。他们需要一个按钮来打开显示器，这促使一位喜剧演员讽刺说，给一个独臂男人一个会很没品味。尽管自那以后手表和其他可穿戴设备的用户界面有所改善，但智能手机仍然存在一些可用性挑战。一些操作手机所需的触摸屏手势，如捏，在单手操作手机时几乎是不可能的，对于那些试图自拍时拇指粗短的人来说更是如此。

你可能会认为，大量的传感器和船上的原始计算能力可以提供更好的方式来控制手机。如果哥伦比亚大学(Columbia University)的一篇论文中描述的模块化机械输入部件流行起来，你可能是对的。被【常晓】*等人*称为“Vidgets”的触觉设备被设计成在启动时在手机的惯性测量单元(IMU)上创建特征加速度曲线。Vidgets 有多种形式，从按钮到滚轮，每一种都有相似的大小和形状，并被设计成可以停靠在 3D 打印手机壳背面的八个位置之一。一旦经过训练，该算法就会观察由启动 Vidget 引起的加速度信号，并向手机发送命令以模仿相应的手势。下面的视频演示了几个用例，其中虚拟萨克斯管是我们最喜欢的。

这真的是很聪明的东西，并深入到“为什么我没有想到这一点？”领土。需要走在 IMU 的前面，充分利用它们的能力吗？你可以从[【Al Williams】](https://hackaday.com/2017/06/26/mems-the-biggest-word-in-small/)的《微机电系统初级读本》开始。

 [https://www.youtube.com/embed/CmSIAoa8vqE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CmSIAoa8vqE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Itay Ramot]的提示，[via [Gizmodo](https://gizmodo.com/without-wires-or-bluetooth-this-case-lets-you-add-butt-1835447478)