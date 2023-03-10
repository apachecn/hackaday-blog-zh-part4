# 问黑客日:树脂打印机建立板

> 原文：<https://hackaday.com/2022/07/20/ask-hackaday-resin-printer-build-plates/>

FDM 3D 打印的早期是狂野的。让塑料粘在你的构建板上是一个挑战。蓝色胶带和涂有发胶的玻璃在很长一段时间里都是王者。随着时间的推移，出现了更好的涂层，许多人使用覆盖有某种 PEI 的弹簧钢。然而，当谈到树脂打印机时，选择似乎更少了。我们最近有机会在两台不同的打印机上尝试了三种不同的构建表面:Nova3D Bene4 和 Anycubic Photon M3。我们学到了很多。

## 树脂印刷评论

如果你还没有象征性地将你的脚趾浸入树脂中——从字面上看这将是非常混乱的——打印机足够简单。有一个底部有一层透明膜的液态树脂罐或大桶。大桶放在一个液晶显示屏上，下面有一个紫外线源。

[![](img/eef6032a7c8abb9e42347ad47f90018a.png)](https://hackaday.com/wp-content/uploads/2022/07/plate.png)

nova 3d 中的典型造型盘(图片由【帕特里克·威廉姆斯】)

一个造型盘从上方进入大桶，正好位于胶片上方。液晶显示器允许一些紫外线通过，从而固化大桶中的树脂。幸运的话，塑料会粘在薄膜和模板上。曝光完成后，打印机会稍微抬起构建板，幸运的话，塑料会从胶片上脱落并粘在板上。然后盘子会下降到比上一次稍微高一点的位置，整个过程重复进行。

## 权衡取舍

像所有工程一样，3D 打印是一系列的权衡。在构建板的情况下，你想要的东西是硬化的树脂会比水箱底部的薄膜粘得更好。然而，当你想让它松手的时候，你也想要一个能让它松手的东西。

[![](img/9f58dd4e6e19b0f99c712616e38b6a02.png)](https://hackaday.com/wp-content/uploads/2022/07/bplate.png)

A spring steel plate with a magnetic backing sticker, ready to install

我们用过的大多数打印机只有一个扁平的金属制造板。这种方法效果很好，但是很难去除指纹。使用刮刀时，你必须注意不要失去手指或损坏零件。这就是我们在 Nova3D 打印机上找到的那种模板。然而，我们很快转向了弹簧钢板。这在概念上类似于你用 FDM 打印机做的事情。一个磁性标签放在真正的构建板上，弹簧钢粘在上面。唯一的问题是，你必须告诉印刷商，构建板现在比它认为的要厚。

[![](img/9c3ae28e89e4e72ee59ae79bf976940d.png)](https://hackaday.com/wp-content/uploads/2022/07/M3-Laser-engraved-Build-Plate.png)

The Anycubic Photon M3’s laser-engraved build plate

另一台打印机，光子 M3，有一个特殊的激光切割构建表面，并不完全光滑。Anycubic 已经在几台打印机上使用了这种方法，并声称它可以提高粘附力，还有助于在部件下找到一个工具进行拆卸。你可以从图像中看到，它的表面有一种轻微雕刻的钻石图案。

## 严峻的考验

老实说，金属拉丝床很疼。我个人曾不止一次在试图切掉零件时割伤自己，也不止一次在这个过程中弄碎零件。我的床上有多处抓痕。

[![](img/de6f06ba573c850474b0222e66f97609.png)](https://hackaday.com/wp-content/uploads/2022/07/ent.jpg)

Scraping the raft off of this smooth metal build plate can be tough

光子 M3 的床显然更好。我不能说更好的粘附部分，因为我通常没有这个问题。但它确实让楔入零件变得更加容易。据推测，该模式给工具提供了一些工作间隙，但从纹理床上移除零件的压力要小得多。

但是，你一旦去了弹簧钢，就很难再回去了，在我看来。你可以把盘子拉下来，把整个东西放进洗衣机里。然后，你可以简单地弯曲板，弹出部分了。没有工具，没有割伤，没有划痕。这些印版非常便宜，所以你甚至可以有多个印版，并在清洗最后一个印版时轻松地印上一个新的印版。

## 每个人都有

然而，结果是值得努力的。光子的纹理表面上的章鱼比光滑的金属床更容易离开，但仍然不容易。同样的章鱼放在钢板上也很容易操作，而且马上就会爆炸。

 [![The octopus clings to the patterned bed on the way to the bath](img/8854f593c5fcfb1b5ecc29c824bb2c3c.png "oct")](https://hackaday.com/2022/07/20/ask-hackaday-resin-printer-build-plates/oct/) The octopus clings to the patterned bed on the way to the bath [![Octopus on steel sheet, ready to pop off.](img/96d8af0eb2d79d724d29b29921170d09.png "oct2")](https://hackaday.com/2022/07/20/ask-hackaday-resin-printer-build-plates/oct2/) Octopus on steel sheet, ready to pop off.

当然，那是我的看法。我喜欢弹性平板床。你怎么想呢?我发现的唯一真正的缺点是，你必须修改打印机或固件来告诉打印机不要将新的更厚的打印床向下驱动到 LCD 中。对于 Nova3D 来说，这涉及到打印一个小垫片，使其更早地触及限位开关。没什么大不了的，但也不是即插即用。

如果你浏览打印机论坛，你会发现人们谁去了灵活的建设板系统似乎很高兴，总的来说。有少数情况下磁铁不粘或附着力差。但是绝大多数情况下，你会听到积极的故事。这让我想知道为什么我们没有看到任何像这样的板作为库存项目，或者至少作为内置支持偏移 Z 轴传感器的选项。

我承认，我不像我想象的那样经常树脂打印。当然，结果很好。但是混乱是实质性的，特别是如果你开始有点笨拙的话。然而，弹簧钢床真的有帮助。气味是一样的，树脂还是滴得到处都是，但至少你可以轻松去除印迹。如果你想把它们扔进洗衣机，在一个轻质的盘子上处理它们比移动整个印刷床组件更容易。当然，如果你不喜欢它，去掉磁性标签，取消你的 Z 轴模式，回到原来的样子也不是很难。

你觉得怎么样？你用什么样的床做树脂？你喜欢吗？还有其他选择吗？让我们在评论中知道，如果你在这方面做了什么好项目，[给我们留下链接](https://hackaday.com/submit-a-tip/)。

在之前，我们已经讨论过[柔性平板床。如果你还没有尝试过树脂印刷，我们可以告诉你一些关于](https://hackaday.com/2020/10/26/improved-flexible-build-plate-for-sla-is-ready-to-rock/)[的事情。](https://hackaday.com/2019/10/02/when-does-moving-to-resin-3d-printing-make-sense/)