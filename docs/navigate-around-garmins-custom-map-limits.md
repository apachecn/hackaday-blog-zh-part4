# 在 Garmin 的自定义地图限制中导航

> 原文：<https://hackaday.com/2019/10/04/navigate-around-garmins-custom-map-limits/>

如果您对 Garmins 的唯一体验是几年前的那辆租车，您可能会惊讶地发现，其中一些(主要是手持户外设备)允许自定义地图。这听起来很酷，直到你发现它的局限性。除非升级到高级版，否则它不允许地图文件大于 3MB。更糟糕的是，它会抑制大于一百万像素的地图的分辨率。好吧，拿出你的虚拟登山鞋，因为[facklere]将带你走下[DIY 数字制图之路](https://www.instructables.com/id/Create-Custom-Maps-for-Your-Garmin-GPS)。

你可以使用任何你想要的地图，只要它不是完全虚构的(尽管在这张地图上漫游中土世界会是一个有趣的黑客)。您的地图可以是纸张、PDF 或羊皮纸；只需要把它转换成 JPEG 格式。[facklere]想要使用的地图是一个巨大的 PDF，所以作为奖励，他展示了如何在 GIMP 中从 PDF 转换成 JPEG。接下来是复杂的部分——通过使用谷歌地球将地图覆盖在真实的道路上，在现实中扎根。

你还有一张巨大的地图。现在怎么办？秘制酱就是贴瓷砖。[facklere]使用了 [KMZfactory](https://sites.google.com/site/jromaya/kmzfactory) ,这是 Garmin maps 的一个免费地图编辑器，它为你多做了一点工作来分割图块，使它们保持在 1MP 的限制之内。完成后，上传到你的单位就可以上路了。

有一个旧的 Garmin 不做自定义地图？看看你是否能让 DOOM 运行起来。