# 无人机上的倒立摆平衡

> 原文：<https://hackaday.com/2021/11/25/inverted-pendulum-balanced-on-a-drone/>

[Nicholas Rehm]白天在马里兰州约翰霍普金斯大学的应用物理实验室工作，因此对各种无人机应用有相当丰富的经验。问题在于“坚持”号火星漫游车着陆是如何工作的，这促使[尼古拉斯]在他的无人机下悬挂一块石头，通过绞盘连接。这被证明是有趣的。但我们更感兴趣的是，当你试图在飞行中的无人机顶部安装一个倒立摆会发生什么？(视频嵌入，如下)

这是一个[经典的控制理论问题](https://en.wikipedia.org/wiki/Inverted_pendulum)，你需要测量钟摆相对于底座的角度，通过计算钟摆角度的必要加速度来闭合回路。典型地，这仅在一维中被证明，但是用两个自由度平衡一个钟摆只是稍微复杂一点。

[Nicholas]首先尝试通过简单地从模拟操纵杆上移除定心弹簧来推导摆角，并使用它将摆杆连接到无人机机身。很明显，这有一个很大的缺点。钟摆与垂直方向的角度现在是操纵杆角度和无人驾驶飞机角度之和，这与相关的测量误差一起被证明是一个不可用的设置。不要气馁，[尼古拉斯]只是在摆的底部增加了另一个 IMU 板，并保持操纵杆机制仅作为枢轴。正如你在休息后的视频中看到的，这确实奏效了。

飞行控制器是[Nicholas']自己的项目， [dRehmFlight](https://github.com/nickrehm/dRehmFlight) (GitHub)，这是一个面向 Teensy 4.0 的 Arduino 库，使用无处不在的 MPU6050 6-DOF IMU。[Nicholas]还为控制器制作了一个[介绍视频](https://www.youtube.com/watch?v=tlD0C5CrWcA)，这可能会对那些希望沿着这条道路建造自己的垂直起降飞机的人有所启发。钟摆实验的代码写的时候还没有，也许以后会打到 GitHub？

想要更多倒立摆的乐趣，一定要看看这个简单的线性雪橇。关于[悬浮摆](https://hackaday.com/2021/02/25/demonstrating-the-mars-rover-pendulum-problem-with-a-drone-on-earth/)，我们不久前报道过 dRehmFlight，这也值得一看。

 [https://www.youtube.com/embed/XmYRQi48s-8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XmYRQi48s-8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

