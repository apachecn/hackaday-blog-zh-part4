# 用神经网络检测水果和蔬菜的成熟度

> 原文：<https://hackaday.com/2021/07/22/detecting-ripeness-in-fruit-and-vegetables-via-neural-networks/>

人类有识别适合食用的食物的天赋。例如，你本能地喜欢新鲜水果和蔬菜，但发现蛆虫滋生的腐肉令人作呕，这是有原因的。然而，我们喜欢尽可能多地自动化食品生产过程，这样我们就可以做其他事情，所以有必要让机器不时地将成熟和现成的产品从其余产品中分拣出来。[kutluhan_aktar]已经找到了一种方法来做到这一点，即利用神经网络的力量。

该项目的目标很简单，通过监测色素的变化来检测水果和蔬菜的成熟度。该项目不使用相机，而是依赖于 AS7341 可见光传感器的数据，该传感器更适合捕捉精确的光谱数据。这可以更好地读取水果反射的实际光线，这是由与成熟度直接相关的果皮色素决定的。

在几天的时间里，从一系列水果和蔬菜中获取样本读数，这允许建立一个处于不同成熟阶段的产品的数据库。然后，这被用于创建张量流模型，该模型可以以合理的确定度确定传感器下的水果的成熟度。

该建筑是先进传感技术与神经网络结合使用的一个很好的例子。我们怀疑这些结果比用廉价的网络摄像头合理确定的结果要准确得多，尽管我们很想看到这样的深入比较。

信不信由你，这不是我们在这些神圣的页面中唯一的水果光谱仪。休息后的视频。

 [https://www.youtube.com/embed/Mze7madcif8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Mze7madcif8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

