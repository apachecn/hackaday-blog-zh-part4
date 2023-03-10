# 卓越的平板电脑获得 MicroSD 插槽

> 原文：<https://hackaday.com/2019/08/30/remarkable-tablet-scores-a-microsd-slot/>

现代平板电脑和手机的扩展选项越来越少，这是一个明显的趋势。找到一个可用的 microSD 插槽变得越来越罕见，这可能会特别令人沮丧。对[davisr]来说，这根本不行，[于是他们开始黑他们卓越的平板电脑。](http://www.davisr.me/projects/remarkable-microsd/)

![](img/d79f86e4f8c5ab2d3136320a0621a4cc.png)

A rotary tool was used to make a tidy slot for the microSD card.

卓越已经在主板上为 SDHC 接口准备了一套衬垫，准备就绪。尽管如此，硬件和软件都需要修改才能启动和运行。[davisr]首先将一些电线焊接到主板上，将它们连接到 microSD 插座上，该插座安装在平板电脑边缘的一个方便的角落。然后这个盒子被精巧地改造成一个可以插入和取出卡片的槽。完成这些后，内核被重新编译以支持 SDHC 接口，一切都准备好并运行了。

修改完成后，[davisr]现在有超过 150GB 的可用存储空间，这应该可以持续相当长一段时间。类似的攻击在其他平台上也是可能的。[即使是 Pi Zero 也可以用正确的 mod 挂载第二张 SD 卡！](https://hackaday.com/2017/08/05/add-a-second-sd-card-to-the-pi-zero/)