# 哨兵水枪依靠激光雷达

> 原文：<https://hackaday.com/2020/06/24/sentry-water-gun-relies-on-lidar/>

随着我们进入夏季，超级透雨者和他们的同类成为在炎热中降温的必不可少的方式。不满足于自己追逐目标，[【马塞尔】建造了一个哨兵水枪来执行他的命令](https://hackaday.io/project/171861-sentry-water-gun-lidar-tracking)。

这种构建利用典型的 3D 打印机组件来完成工作。Minitronics 2.0 板用于运行该节目，包装了 40 MHz 的 SAMD21 微控制器，用于大量的咕哝。它也兼容 Arduino，这使得编程变得很容易。它与 NEMA17 和 NEMA23 步进器以及一个外部驱动板相结合，将枪转向目标。目标探测是通过一个探测附近物体范围的雷达 A1。该数据用于计算通过继电器控制的螺线管发射的水流击中目标所需的摇动角度和倾斜度。

这是一个有趣的建筑，很好地浸泡了那些在泳池边玩耍的人。[Marcel]旨在通过减少齿隙和提高回转速度来进一步提高性能。哨兵枪在这些地方永远是受欢迎的建筑。休息后的视频。

[hack adayprize 2020](https://prize.supplyframe.com)主办单位:[![Supplyframe](img/193ca31946d20fcfa39296cb816a4c50.png)](https://supplyframe.com/)[![Digi-Key](img/4fc24a8a6b4498aecfe987b00009d192.png)](https://www.digikey.com/)[![Microchip](img/8dd361210bbb0e5592c24f87e4e2267e.png)](https://www.microchip.com/)

 [https://www.youtube.com/embed/JFVZ-LVM_vs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JFVZ-LVM_vs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

