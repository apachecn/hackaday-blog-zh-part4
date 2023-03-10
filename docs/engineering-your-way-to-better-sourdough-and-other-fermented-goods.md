# 工程你的方式更好的发酵面团(和其他发酵产品)

> 原文：<https://hackaday.com/2020/01/08/engineering-your-way-to-better-sourdough-and-other-fermented-goods/>

Trent Fehl 是一名工程师，曾为 SpaceX 和 Waymo 等知名公司工作。当他开始烘焙时，他把这些工程技能带回家，解决了厨房里的一个经典问题:将酸面团发酵剂保持在成功发酵所需的理想、有点压抑的可接受温度范围内。

酸面团发酵剂是一团野生酵母，你可以用面粉、水和耐心自己制作。它不仅仅适用于酸面团面包——你可以从罐子里舀一些出来，用来做煎饼、华夫饼、椒盐卷饼和许多其他面包类的美味。发酵剂是一种有生命的东西，一个充满发酵的容器，它吃面粉，有特定的温度需求。观点略有不同，但活跃生长的可接受温度范围约为 60°F 至 82°F。太冷了，启动器将进入休眠状态，尽管它可以通过一点点爱而复活。但是如果发酵剂太热，所有的酵母和细菌都会死亡。

虽然当然有商业产品试图解决温度控制的问题，但大多数似乎是针对那些生活在温度永远不会超过 80 华氏度的仙境中的人。这些设备大多不能制冷，只能供热。但是，如果你生活在一个气候从湿热到寒冷干燥四季分明的地方，那该怎么办呢？

答案就在[室](https://www.trentfehl.com/projects/chamber/)里，这是特伦特创造的一个温度调节的避风港，让这些野生酵母茁壮成长。它使用帕尔贴装置根据需要加热和冷却盒子，以保持混合物在 26°C/78.8°f 下发酵。

借助帕尔贴装置，Trent 只需改变流经帕尔贴的电流方向，就能改变腔室内的温度。他用一个由 Raspberry Pi Zero 驱动的 H 桥模块来实现这一点。当室内开始变得太热时，外墙上的风扇会将热量排出。当天气变得太冷时，室内的第二个风扇会吸入温暖的空气。

特伦特说，该室表现非常好，他记录的温度低至 60 华氏度，高至 82 华氏度。他主要用它来制作酸面团，但它也可以用于其他对温度敏感的食品科学，如腌制、种植蘑菇或制作酸奶。我们认为它也是发酵康普茶的理想选择。

Chamber 工作得很好，Trent 在使用它的时候把进一步的开发搁置了。他确实有几个改进的想法，所以如果你想帮忙，可以看看他的网站和 T2 的 Github repo。

 [https://www.youtube.com/embed/Zbus1_F7ffc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Zbus1_F7ffc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

