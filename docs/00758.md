# 整理乐高就像做一盒巧克力

> 原文：<https://hackaday.com/2018/09/27/sorting-lego-is-like-making-a-box-of-chocolates/>

你知道巧克力糖的生产和乐高积木的分类有共同点吗？他们都使用相同的技术将巧克力块或砖块变成一个个沿着传送带往下移动。至少这是[帕科·加西亚]在制作[他的乐高分类器](https://medium.com/@pacogarcia3/tensorflow-on-raspbery-pi-lego-sorter-ab60019dcf32)时发现的。

然而，他没有马上发现这一点。他首先试验了自己的技术，发现如果他将一批砖块垂直于传送带的运行方向丢进传送带，那么他随后的分离尝试就不会成功。然后，他转向[【阿基尤基的】乐高分拣机](https://hackaday.com/2011/04/08/nxt-machine-sorts-lego-blocks-automatically/)寻求灵感，并以一定角度将它们扔到传送带上，确保一些砖块在其他砖块前面。他发现的另一个技巧在下面的巧克力分类视频中得到了很好的展示，如图所示。也就是说，使用皮带上的导向装置来产生速度差。当砖块被压在导轨上时，移动速度比传送带慢，但当砖块离开导轨时，它会加速到传送带的速度，从仍在导轨上的砖块上脱离，从而将它们分离。

进一步的发现与巧克力生产无关，除非是为了质量控制。一旦一块砖被分离出来，就必须进行分类。为此，他使用了谷歌的 Inception v3 神经网络。但首先，他必须重新训练它识别不同类型的乐高积木，这是我们以前见过的用于识别扑克牌的方法。为了进行再培训，他需要许多不同砖块的图像，这些图像被分成不同的类型。在那里他想出了一个聪明的计策。他用了自己的分类器。例如，要获得一堆不同颜色和方向的 1×1 砖块的图像，他只需通过排序器运行它们，将图像保存到文件中，并将它们分配给 1×1 砖块类。然后，他使用配有 GeForce GT 730 GPU 的台式机进行重新训练，每块砖大约需要 2.7 秒。不过，对于分类，他在树莓派上运行训练好的神经网络，每块砖需要 3.8 秒。最终的分类器工作得相当好，分类准确率达到 89%。请观看下面的视频。


 [https://www.youtube.com/embed/uCuQsNwX1QY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uCuQsNwX1QY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/CrGrcaJoyws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CrGrcaJoyws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[途径 [adafruit](https://blog.adafruit.com/2018/09/21/use-tensorflow-and-raspberry-pi-to-build-an-automatic-lego-sorter-piday-raspberrypi-raspberry_pi/)