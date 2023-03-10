# 挡风玻璃刮水器的超大 DIY 遥控伺服系统

> 原文：<https://hackaday.com/2018/07/13/supersize-diy-r-c-servos-from-windscreen-wipers/>

我们都熟悉购买业余爱好伺服的经历。市场上充斥着夸大规格、性能不佳的廉价克隆产品。即使是品牌伺服往往无法交付，有时你只是不能从典型的业余爱好伺服的小形状因子获得所需的扭矩或速度。

进入【詹姆斯·布鲁顿】和他的[从挡风玻璃刮水器电机](https://www.youtube.com/watch?v=3pYWLF8qw-g)DIY 遥控伺服。挡风玻璃刮水器电机像芯片一样便宜，是典型的废品。电机轴通过滑轮和一些线连接到电位计，提供必要的闭环反馈。Arduino 提供了大脑，而不是使用伺服系统中的传统模拟电路。这意味着 PID 控制可以在 duino 上实现，并调整以获得不同负载特性的最佳响应。还有不同接口选项的选择:虽然[James]的 Arduino 代码接受 PWM 信号来替代嵌入式 R/C 伺服系统，但微控制器的添加意味着可以使用许多其他输入信号类型和协议。事实上，我们最近写了关于[串行总线伺服系统及其众多优势](https://hackaday.com/2018/07/05/wrangling-rc-servos-becoming-a-hassle-try-serial-bus-servos/)。

我们特别喜欢这一点，因为工业伺服电机的价格壁垒；当然，这种解决方案没有现成产品提供的精度或扭矩，但对许多黑客来说已经足够了。顺便说一句，这是我们最喜欢的开源项目之一的灵感来源:ODrive，，它专注于利用工业用廉价无刷电机的能量。

 [https://www.youtube.com/embed/3pYWLF8qw-g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3pYWLF8qw-g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

