# LED 矩阵和光电晶体管构成了一个倒车摄像头

> 原文：<https://hackaday.com/2019/05/06/led-matrix-and-a-phototransistor-make-a-reverse-camera/>

数码相机有一个传感器阵列，可以捕捉反射或透射到它上面的光线。这种构建更接近于反向摄像机——单个传感器在 led 矩阵上成像。我们认为这很棒。

我们必须承认，当我们第一次偶然发现[marciot]的 LED 矩阵扫描仪时，我们有点困惑。从下面的视频中，我们认为矩阵中的 led 既可用于检测入射光，也可用作显示器。我们以前见过[led 被用作光电二极管](https://hackaday.com/2018/12/13/ben-krasnow-builds-a-one-component-interferometer/)，所以这样一个奇妙的装置可以工作，但这不是这里发生的事情。光电晶体管连接到 Arduino Uno，位于 32×32 RGB LED 矩阵上方。当传感器观察时，扫描程序扫描矩阵中的 led，然后程序打开传感器在扫描过程中看到的 led。放置在矩阵上方很远的地方，会产生一个大圆盘状的光，看起来就像光电晶体管把光向下投射到矩阵上。通过在传感器和矩阵之间放置一些东西，投射出虚拟的阴影，这种效果得到了加强。靠近发光二极管使用时，传感器的作用更像一支光笔。

这是一个很酷的效果，看起来像一个有趣的项目扔在一起。不过，刷新时间可能会更快一些；或许 ESP32 能帮上忙。

 [https://www.youtube.com/embed/9F9EUaXhj5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9F9EUaXhj5M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [Arduino 博客](https://blog.arduino.cc/2019/05/01/use-an-led-matrix-as-a-scanner/)