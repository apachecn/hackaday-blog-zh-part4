# 用树脂打印机愚弄指纹扫描仪

> 原文：<https://hackaday.com/2019/04/08/fooling-fingerprint-scanners-with-a-resin-printer/>

生物识别技术经常被用作一种访问控制的形式。虽然这最初只限于好莱坞电影中的银行金库，但现在在许多笔记本电脑和智能手机上都能看到这种功能。尽管有一长串的理由说明为什么这是一个坏主意，这项技术仍然越来越受欢迎。[darkshark]向我们展示了一个简单的利用方式，[使用 3D 打印机骗过 Galaxy S10 的指纹扫描仪](https://imgur.com/gallery/8aGqsSu)。

Galaxy S10 的有趣之处在于[它使用了超声波指纹传感器](https://www.lifehacker.com.au/2019/02/theres-a-trick-to-using-the-galaxy-s10s-ultrasonic-sensor/)，通过将传感器放置在屏幕下方，该传感器继续推动手机的硬件开发，实现最小化甚至无边框。传感器正在寻找你指纹脊的深度，而触摸屏验证你多肉手指的电容存在。这个黑客满足这两个检查。

[darkshark]从一张酒杯上的指纹照片开始。然后在 Photoshop 中进行处理，然后在 3DSMAX 用于创建几何图形来复制原始手指。在 AnyCubic Photon LCD 树脂打印机上制作零件后，假手指垫能够通过将指纹放在玻璃上并在上面触摸你的手指来成功解锁手机

[darkshark]指出，指纹是在近距离采集的，但镜头合适的相机可以在远处捕捉到类似的细节。另一件要注意的事情是，如果你的手机被盗，它很可能覆盖着油腻的指纹。像往常一样，它很好地提醒了我们，指纹不是密码，也不应该被当作密码对待。如果你需要温习基础知识，[我们有一本关于指纹扫描仪如何工作的很棒的初级读本](https://hackaday.com/2017/04/27/fundamentals-of-fingerprint-scanning/)，还有一本关于[为什么使用指纹来保证安全是个糟糕的计划](https://hackaday.com/2015/11/10/your-unhashable-fingerprints-secure-nothing/)。

感谢工程师的提示！]