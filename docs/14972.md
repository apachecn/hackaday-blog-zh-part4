# 通过将 DIP 芯片变成……QFN 来制作手持 NES？

> 原文：<https://hackaday.com/2022/10/02/making-a-handheld-nes-by-turning-dip-chips-into-qfn/>

有了 Dremel 你可以成就很多。例如，很明显，你可以把原来的 NES 缩小到手持式。CPU 和 PPU(图像处理单元)都是 40 针 DIP 芯片，这使得 NES 缩小有点棘手。然而,【Redherring32】不会就此止步，而[只用一个 Dremel 切割轮就把这些蘸酱芯片变成了 QFN 风格的安装模具](https://twitter.com/redherring32/status/1571606175614996480) ( [Nitter](https://nitter.net/redherring32/status/1571606175614996480) )。为什么？当然是为了实现他的 TinyTendo 掌上游戏机项目。

DIP 芯片触点通过称为引线框的金属引脚网从芯片中伸出。[Redherring32]切入引线框，只留下芯片的有用部分，引线框部分保留为类似 QFN 的接触垫。然后，芯片被安装到[tiny tendo PCB](https://twitter.com/redherring32/status/1562537277750153217/)上一个定制的底座上，连接到所有其他元件，谢天谢地，现在可以以 SMD 形式获得这些元件。

这个技巧一直在起作用，毫无疑问，我们很快就会看到 TinyTendo 作为一个独立的项目发布。就在一年前，我们看到[redherring 32]被切割成这些芯片，我们想知道它的用途是什么。现在，我们知道了:这是他的 [OpenTendo 项目的逻辑延续，](https://hackaday.com/2020/03/22/a-nes-motherboard-for-the-open-source-generation/)对最初的 NES 进行主板逆向工程和重新设计，这一努力无疑受到了许多 NES 爱好者的赞赏。通常，人们不会将实际的芯片切割成很小的尺寸——相反，他们会在主板上切割，这种做法被称为[‘修剪’，](https://hackaday.com/tag/trimmed/)，这种做法在这些年里为我们带来了许多基于原始硬件的微型游戏主机。

> 将它们切割成大致尺寸，并仔细打磨边缘，使芯片达到最终尺寸后，它们看起来会是这样的:[pic.twitter.com/MTbYyHrvZ5](https://t.co/MTbYyHrvZ5)
> 
> —redherring 32(@ redherring 32)[2022 年 9 月 26 日](https://twitter.com/redherring32/status/1574448587278352384?ref_src=twsrc%5Etfw)