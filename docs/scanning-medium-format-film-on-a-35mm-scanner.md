# 在 35mm 扫描仪上扫描中画幅胶片

> 原文：<https://hackaday.com/2021/07/28/scanning-medium-format-film-on-a-35mm-scanner/>

扫描电影是伟大的存档目的，以及分享数码照片。然而，如果你扫描的是 120 张胶片，也就是中画幅，购买必要的硬件可能会很贵。相对来说，35 毫米扫描仪更为常见，因此[Christian Chapman]决定对其进行改进，以适应中号胶片。

黑客是针对 Plustek 8100 的，需要在两个方面修改扫描仪。首先，考虑到更大的胶片，驱动器必须被扫描以扫描更长的范围。其次，必须更换胶片托架的一部分，这样它就不会出现在扫描仪的视野中。

前者是通过使用 sane-genesys 扫描仪软件后端实现的，可以很容易地修改该软件以适当地调整扫描长度值。后者是通过 3D 打印替换组件来实现的，这些组件可以在不阻挡必要区域的情况下进行安装。

这是一个整洁的黑客和一个允许[基督教]既扫描中画幅电影，也过扫描 35mm 电影，以捕捉链轮孔区域的细节。我们以前也见过完全定制的胶片扫描仪。如果你有自己的扫描仪，[一定要给我们写信！](http://hackaday.com/submit-a-tip)