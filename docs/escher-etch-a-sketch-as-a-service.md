# 埃舍尔:蚀刻素描作为一种服务

> 原文：<https://hackaday.com/2019/12/18/escher-etch-a-sketch-as-a-service/>

不管是好是坏，科技界已经完全致力于将尽可能多的产品推向“云端”。当然,《黑客日》的读者能看穿这些公司流行语。这只是一种花哨的说法，意思是每次你想使用这项服务时，你都必须通过互联网连接某个服务器。在某种程度上，[【马特·威尔士】已经和埃舍尔](https://medium.com/@mdwdotla/escher-the-worlds-first-cloud-controlled-etch-a-sketch-f2d5b7f1bd44)完美地论证了这个概念。这是一个普通的蚀刻素描，但因为别人拥有它，你必须有一个活跃的互联网连接才能使用它，这使它成为云的荣誉市民。

埃舍尔采用 3D 打印的形式安装和替换经典绘画玩具的旋钮，允许两个 NEMA 17 踏步机代替人手。由于设计巧妙，[Matt]可以轻松地将 Etch-a-Sketch 拉出，并以传统方式使用它，尽管不可否认的是，握住齿轮旋钮的人体工程学可能需要一点时间来适应。但是谁想用他们的手呢？

[![](img/353f5e67359bc2a3337ea4e09c132032.png)](https://hackaday.com/wp-content/uploads/2019/12/escher_detail.jpg) 在电子方面，展会的明星是 Adafruit Feather HUZZAH32 开发板，配有一个电机控制器，可以为步进器提供 12 V 电压。[Matt]甚至经历了制作定制电压调节器 PCB 的麻烦，该 PCB 将步进器的电压降低到羽毛的 5 V。完全没有必要，我们就喜欢这样。

对于观众中的软件人员，[Matt]详细讲述了他如何通过 Google Firebase 让他的硬件与网络对话。即使互联网上的草图没有引起你的兴趣，我们也可以想象他将 g 代码文件从浏览器推入羽毛的深度肯定会引起你的兴趣。

听说[这不是第一个自动蚀刻草图](https://hackaday.com/2015/02/02/automated-etch-a-sketch-re-produces-famous-artwork/)这几年来[一直在这些页面上出现](https://hackaday.com/2014/03/28/an-etch-a-sketch-to-fetch-the-time/)可能会有点惊讶，但这可能是我们见过的最完全实现的版本。