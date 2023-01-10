# 提升内华达山脉

> 原文：<https://hackaday.com/2022/06/13/upscaling-the-sierras/>

如果你在 80 年代中期到 90 年代玩过很多游戏，你可能会记得 Sierra 的在线冒险游戏中的图标。它们色彩明亮(16 种颜色)，富有动感和深度。为了表达敬意，[eviltrout]努力提升图片的档次。尽管以 160×200 的 16 色进行渲染，然后进行拉伸，但存储所有这些位图，即使每像素只有 4 位，也会占用软盘上所有可用的存储空间。游戏中的工程师决定采用矢量方法来解决光栅问题。

当[eviltrout]尝试升级背景时，他开始编写一些代码，从游戏引擎中提取绘制命令，称为冒险游戏解释器(AGI)。将 vector 命令与具有最佳压缩的等效 PNG 版本进行比较，AGI vector 版本的大小大约是其一半。对于一对 80 年代的游戏开发者来说还不错。由于都是矢量命令，所以以高得多的分辨率绘制它们应该相对简单。至少，他是这么想的。第一个问题是洪水填充。由于画布较大，线条间有空隙，洪水逃逸。采取了一些方法，例如使用低分辨率参考和行进正方形，但都不令人满意。最终，[eviltrout]扩大了洪水填充，使用了更粗的线条。他还首先渲染到较低的分辨率，并连接相同颜色的相邻线条。最后，他使用 ImageMagick 去噪输出中的白点。

我们发现这种效果很迷人，但有些人可能会说你把艺术扭曲成了艺术家从未想过的样子。但是，就像所有的图形增强一样，一些艺术自由在没有原始艺术家参与的情况下被剥夺了。代码可以在麻省理工学院许可的 [GitHub 上获得](https://github.com/eviltrout/agi-upscale)。休息后的视频。

 [https://www.youtube.com/embed/sclZDCjUVvI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sclZDCjUVvI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

