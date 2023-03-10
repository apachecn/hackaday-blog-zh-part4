# Arduino 绕线机速度惊人

> 原文：<https://hackaday.com/2020/10/20/arduino-bobbin-winding-machine-is-freaky-fast/>

缝纫最糟糕的事情之一是发现你的线轴——较小的线轴与针和较大的线轴一起工作来完成一针——在几针前用完了线。如果你幸运的话，机器的线轴上有一个观察窗，所以你可以很容易地知道它什么时候危险地接近用完，但许多机器(包括我们的)必须被拆开一半，在检查之前把线轴拆下来。

[![](img/a11ec6670dae48112e030263bcd2f507.png)](https://hackaday.com/wp-content/uploads/2020/10/bobbin-winder-cutter.jpeg) 准备好备用的线轴绝对是答案。我们大胆猜测，大多数(如果不是全部的话)机器都有一个内置的绕线器，但使用它们需要将机器脱线，并将其设置为缠绕线轴，而不是缝纫。如果你有大量的缝纫工作要做，并且负担得起，自动络筒机是天赐之物。[如果你是【创新先生】，你可以自己用丙烯酸、铝和 Arduinos](https://electricdiylab.com/diy-arduino-based-bobbin-winding-machine/) 做一个。

[![](img/f355fa75ec4b1c487b89bfa396ab8840.png)](https://hackaday.com/wp-content/uploads/2020/10/bobbin-winder-foam-donut.jpeg) 它是这样工作的:用多达 12 个空线轴装载聪明的小丙烯酸幻灯片，然后拨入速度百分比并按下开始按钮。线轴一次装载一个到钻夹头上，钻夹头在结实的 775 DC 马达的输出轴上。马达旋转得快得离谱，几秒钟就把线轴装好了。然后，线轴从斜坡上滑落到架子上，线被一根镍铬合金线切断。

卷绕线轴的一个重要部分是确保线在卷绕开始时保持在适当的位置。我们喜欢[创新先生]处理这部分问题的方式——轴承周围的一个小泡沫甜甜圈将线固定在适当的位置，足够开始缠绕。如果你想为自己制造一台这样神奇的机器，可以得到原理图、BOM 和 CAD 文件。与此同时，休息之后，请观看演示/构建视频。

还不相信缝纫酷到可以学？[我们自己的【珍妮榜】或许可以让你](https://hackaday.com/2016/10/26/why-you-should-own-a-sewing-machine/)皈依。如果这还不能让你明白，你可能想知道一些缝纫机是可以被破解的——[这个老姑娘有了第二次生命，成为一台电脑刺绣机](https://hackaday.com/2018/02/21/vintage-sewing-machine-to-computerized-embroidery-machine/)。如果这些都做不到，考虑一下[缝纫机也能给你第二次生命](https://hackaday.com/2018/05/28/stretching-my-skills-how-and-why-i-made-my-own-compression-sleeves/)。

 [https://www.youtube.com/embed/kGyuscK9GaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kGyuscK9GaA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢提示，[Baldpower]！