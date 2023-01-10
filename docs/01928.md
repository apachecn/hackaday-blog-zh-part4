# 返工 MT3608 升压转换器以降低空载电流消耗

> 原文：<https://hackaday.com/2019/01/27/reworking-mt3608-boost-converters-for-lower-idle-current-draw/>

MT3608 是一款受欢迎的升压转换器，能够以极低的成本轻松提升有用范围内的 DC 电压。模块可以从易贝采购，价格不到 2 美元，安装在印刷电路板上，随时可以使用。这些模块的一个缺点，特别是在使用电池时，是 1 到 1.5 毫安的空闲电流消耗。然而，不用担心——[有一个解决办法，由【又名卡西扬】提供。](https://www.youtube.com/watch?v=zJJcdptSH80&feature=youtu.be&t=101)(视频，下面嵌入。)

诀窍是在无负载连接时修改转换器的行为。升压转换器的使能引脚通过一个下拉电阻保持低电平，从而保持升压转换器关闭。在这种状态下，输出电压等于输入电压。然后在输出路径中安装一个电流检测电阻。当连接负载时，这会导致电流检测电阻上的压降。然后用它来开关一个晶体管，该晶体管将使能引脚连接到正供电轨，使转换器开启，从而达到最大升压输出电压。

[Aya]报道称，这大大降低了空闲电流消耗，对于电池供电项目尤其有用。但是，必须注意，电流检测电阻的大小必须适合给定负载。如果你对背景有点模糊，不用担心，我们之前已经讨论过升压转换器的本质。休息后的视频。

【感谢 Baldpower 的提示！】

 [https://www.youtube.com/embed/zJJcdptSH80?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=101&wmode=transparent](https://www.youtube.com/embed/zJJcdptSH80?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=101&wmode=transparent)

