# 给你的门锁装上无线感应系统

> 原文：<https://hackaday.com/2019/03/25/wifi-your-door-lock-with-an-esp/>

物联网就在我们身边，随之而来的是智能相机、智能家庭显示器和智能家居锁的泛滥。实际上，这些智能便利中并没有多少智能，你可以很容易地构建自己的智能。这就是[MakerMan]用一些现成的部件和一点点代码所做的事情。现在他可以用 WiFi 打开他的门，这是一个很好的干净的建筑。

建造过程首先从移除门上现有的圆筒螺栓开始。这是由一个死栓取代，也有一些真正整洁的螺线管内远程激活。这是安装在门上的一种方式，门可以锁定，与一些熟练的钢锯工作的最小量的损害。之后唯一要做的就是给锁加上一些电子设备和大脑。

为此，[MakerMan]加了一个按钮，引向门外。这些电线中的一部分被接入了锁的机械装置，还有一些被引到了一个安装在电源插座旁边的工程外壳上。项目外壳包含一个 ESP-8266、电源调节器和继电器板，ESP 正在运行代码，该代码实例化了一个 web 服务器，只需在网页上单击几下就可以打开门。

当然，这可能不是地球上最安全的锁，5V 线性稳压器是用热熔胶固定在继电器板上的，但这是一个记录非常好的项目，所有代码都可以在档案中找到。

 [https://www.youtube.com/embed/vYCLJtFv9lI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vYCLJtFv9lI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

