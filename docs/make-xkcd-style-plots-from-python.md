# 从 Python 制作 XKCD 风格的绘图

> 原文：<https://hackaday.com/2019/03/07/make-xkcd-style-plots-from-python/>

[兰道尔·门罗]当然理解数据图形化表示的力量。他的 xkcd 网络漫画中的幽默情节是许多读者最喜欢的部分之一。他们独特的 Tufteian 风格传递信息——在这种情况下，一个妙语——没有过多的装饰。老实说，我们永远也看不够。最近的 [reddit 帖子](https://www.reddit.com/r/programming/comments/awsq9d/xkcdstyle_plots_in_matplotlib/)提醒我们，你可以使用 Matplotlib 在 [Python 中为你自己的数据生成类似的外观(幽默或其他)。](https://matplotlib.org/api/_as_gen/matplotlib.pyplot.xkcd.html)

如果已经用 Matplotlib 生成了一个图，激活 xkcd-mode 就像调用 pyplot 对象上的方法一样简单:

```
matplotlib.pyplot.xkcd()
```

文档建议您安装“幽默无”字体以获得最佳效果。在我们的一台 linux 机器上，我们可以通过一个简单的:

```
sudo apt-get install fonts-humor-sans
```

其他操作系统无疑也会有类似的咒语。真的就这么简单。事实上，上面的特色图片是用这个最简单的脚本生成的:

```
#!/usr/bin/env python3

import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(0, 1, 100)
y = (x > 0.5) * (x - 0.5)

plt.xkcd(scale=5, length=400)
plt.xticks([])
plt.yticks([])
plt.ylabel('Downloads of "humor sans" font')
plt.text(0, 0.25, 'Article on xkcd() published')
plt.plot(x, y)
plt.plot([0.3, 0.475], [0.2, 0.025], 'black')
plt.gca().set_aspect(2*9/16)
plt.savefig('xkcd_plot.png', dpi=300)
```

除了为那些没有多少艺术天赋的人生成幽默的图表之外，这些情节还可以用来代替手绘草图，以表明一个简单的模型或预期的结果。这些情节的滑稽外观传达了这样一种想法，即它们并不代表实际数据，也许只是一个概念。我们在 2018 年黑客日超级会议的[一次会谈中看到了这一点。](https://hackaday.com/2019/01/25/how-to-deal-with-a-cheap-spectrum-analyzer/)

我们之前也报道过一些 xkcd 漫画，比如他们在 2010 年微妙地诋毁 Arduino 的时候，那是很酷的。