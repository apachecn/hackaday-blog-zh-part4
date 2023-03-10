# 幽灵框架展示了不存在的人(和猫)

> 原文：<https://hackaday.com/2020/02/25/ghost-frame-shows-people-and-cats-that-dont-exist/>

[Dan]去年的项目直到现在才被我们忽略，但他的[Ghost Frame](https://danthegeek.com/2019/04/04/ghost-frame-display-images-of-people-and-cats-that-dont-exist/)是一个很好的例子，它将一些现代可黑客攻击的硬件与在线资源结合在一起，形成一个清晰的结果，我们喜欢它背后的清晰想法。鬼画框之所以如此命名，是因为它的目的实际上是为了展示现实世界中不存在的人(和猫)的照片。

[![](img/4f73f7437914eb012c17e8b397318735.png)](https://hackaday.com/wp-content/uploads/2020/02/7thiscatdoesnotexist.jpg)

This cat does not exist (thank goodness.) The computer doesn’t always get it right.

为了让它工作起来，[丹]使用了一个[阿达果 PyPortal](https://www.adafruit.com/product/4116) 作为设备的核心。它从 ThisPersonDoesNotExist.com(显示计算机合成的面部图像，不代表真实的人)提取图像，并显示它们，就好像它们是数码相框中的照片一样。格式化图像以在 PyPortal 的 320 x 240 显示器上很好地显示需要一些额外的工作；[Dan]用一个小的 PHP 脚本解决了这个问题，将图像转换成位图，并在此过程中正确缩放。PyPortal 使得从网络上获取资源变得简单，所以这种摆弄对[丹]的艺术眼光来说并没有太大的障碍。

那些猫呢？嗯，事实证明[ThisCatDoesNotExist.com](http://thiscatdoesnotexist.com/)也在那里，Ghost Frame 可以愉快地显示计算机生成的不存在的猫的图像，就像它显示虚构的人一样容易。然而，看起来不存在的猫一代的状态确实有些落后于人。该网站通常是正确的，但结果偶尔(有趣地)是奇怪的，正如你在这里看到的。

PyPortal 非常适合这种项目，它不仅仅可以显示静态内容。它内置了一些 GUI 功能，正如我们最近在这款触摸屏 21 点游戏中看到的[。](https://hackaday.com/2019/11/10/blackjack-game-plays-with-the-limits-of-pyportal/)