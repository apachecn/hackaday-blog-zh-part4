# 用生锈的自行车强制限速

> 原文：<https://hackaday.com/2019/06/15/enforce-speed-limits-with-a-rusty-bike/>

他们说你不能管理你不能测量的东西，这一点在[这辆被用来测量比利时一个街区](https://github.com/aliekens/flitsfiets)的汽车速度的自行车的案例中确实如此。如果我们正确理解从荷兰语翻译过来的[的话，尽管有人投诉，警察并没有强制执行限速。作为一个解决方案，当地居民建造了一辆装有雷达枪的自行车，收集数据，然后用于说服警察在这条道路上执行速度限制。](https://translate.googleusercontent.com/translate_c?depth=1&rurl=translate.google.com&sl=nl&sp=nmt4&tl=en&u=https://github.com/aliekens/flitsfiets&xid=17259,15700023,15700186,15700191,15700256,15700259&usg=ALkJrhjru44_uqNblSxPXNCOyOa3xy-xNA)

自行车不是这个建筑的功能部分，因为它看起来并不打算移动。相反，之所以选择它，是因为它不显眼(意思是:生锈且不值钱)，而且只是将雷达装置和电子设备放在后面的行李箱中。该雷达经过特别校准，误差小于 1%，并使用深循环铅酸电池运行了大约 8 天。给它装上一个兼容 Arduino 的盾牌，运行一些软件(github 页面上提供的)就足以让它启动并运行了。

这是一个令人印象深刻的公民行动主义壮举，为当地警方提供准确的数据，以改变社区的问题。这项技术不仅得到了很好的利用，而且将昂贵的电子产品藏在一辆生锈的自行车中的社会工程也超出了我们的想象。

感谢[Jo_elektro]的提示！