# ESP32-Cam 会延时吗

> 原文：<https://hackaday.com/2020/01/28/esp32-cam-does-time-lapse/>

就在几年前，如果有人问你带 WiFi 的数码相机要多少钱，你可能不会说 6 美元。但这大约是[比特鲁尼]花了多少钱买了一台 ESP32-CAM。他想试着让这个小相机做时间推移，结果证明这很容易做到。

当然，细节决定成败。相机开始时需要在 USB 接口上进行配置，这使得能够设置 Arduino 集成和 WiFi 配置。因为它将图像的每一帧都存储在 SD 卡上，所以主板不能快速拍照。[Bitluni]报告说，3 秒钟的延迟是他能做到的最短时间，但在大多数情况下，他至少用了 10 秒钟。

该程序有一个实时预览窗口来帮助你设置镜头，但在你开始录制之前，应该关闭它，以免小处理器和 I/O 总线过载。结果是一堆 JPG 图像，如果你愿意，你可以很容易地在电脑上转换成视频。

这可能是在 3D 打印机上安装相机的好方法，尤其是如果想要延时效果的话。否则，您可能会同步到图层更改。现在[比特鲁尼]需要的是一个[轨道钻机](https://hackaday.com/2016/08/23/time-lapse-rig-puts-gopro-into-orbit-in-your-shop/)。

 [https://www.youtube.com/embed/0_pewS4IPN4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0_pewS4IPN4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

