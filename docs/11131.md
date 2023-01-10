# 用这个闪烁着核苷酸代码的徽章来庆祝 MRNA 疫苗

> 原文：<https://hackaday.com/2021/08/24/celebrate-mrna-vaccine-with-this-badge-that-blinks-the-nucleotide-code/>

为了庆祝接种第二剂疫苗，[保罗·克林格]结合了我们最喜欢的两样东西——闪光灯和可穿戴技术——[创造了一个令人敬畏的 mRNA 疫苗徽章](https://github.com/PaulKlinger/mrna_vaccine_badge)。

这种徽章被设计成像挂件一样佩戴，将在 10 分钟内缓慢闪烁 Moderna 疫苗的所有 4000 个核苷酸。休息后观看视频，了解实际情况。如果您获得了辉瑞疫苗，请不要担心，您可以使用徽章背面的界面按钮切换到辉瑞的 mRNA 序列。徽章上甚至有一个方便的图例，如果你的微生物学技能有点生疏，可以识别脂质。

在电路板的背面，您会发现一些限流电阻、一个 CR2032 电池座和运行一切的 ATtiny1617 微控制器。为了帮助将 mRNA 序列转换为 LED 脉冲，【Paul】编写了一个 Python 脚本，该脚本将自动从标准`.fasta`文件导入核苷酸字符串，并将每个核苷酸存储在 2 位中，从而使整个序列适合微控制器的程序存储器。

这不是[保罗的]第一个 RNA 相关的项目；他最初开发了前面提到的 Python 脚本，将包含超过 30，000 个核苷酸的整个新冠肺炎序列压缩到他的[病毒 Blinky 项目的程序内存中，我们去年](https://hackaday.com/2020/03/24/another-blinky-light-project-with-a-covid-19-twist/)报道了该项目。

 [https://www.youtube.com/embed/r8VF4bMJ7uo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/r8VF4bMJ7uo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过[遥控/电子](https://www.reddit.com/r/electronics/comments/p4ybdc/a_little_blinky_badge_that_shows_the_sequence_of/)