# 无晶体管声音合成器

> 原文：<https://hackaday.com/2020/10/24/a-transistor-less-sound-synthesizer/>

没有晶体管的合成器几乎可以成为一个难题的基础，当然，没有晶体管，它必须使用真空管或类似的东西。[虽然不是【蟑螂博士】的合成器](https://hackaday.io/project/175327-transistorless-sound-synthesizer)，但它使用成对的发光二极管和光敏电阻作为有源元件，而不是晶体管。它的振荡器电路由[Patrick Flett]提供，使用一对 LED/LDR 组合来交替充电和放电电容器。这为另一个 LDR/LED 对供电，该对看起来像是驱动桥式整流器的缓冲器，其后有一个最终放大器。

结果是振荡，尽管频率在低音频范围内，并带有一组谐波。它的声音最好被描述为在较低频率下类似于小型单缸摩托车发动机的东西，并且我们看到它可能有各种有趣的可能性。

这种使用基于 LDR 的有源设备的方法可能是一个死胡同，可以追溯到 20 世纪 30 年代，但它仍然是一个有趣的探索领域。这不是我们第一次跟随[蟑螂博士]研究它，过去[我们已经看到同样的技术应用于逻辑门](https://hackaday.com/2019/10/24/light-emitting-logic-gates-built-from-scratch/)。

请听一下休息时间下方视频中的合成器。

 [https://www.youtube.com/embed/0p6bZt3jn0s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0p6bZt3jn0s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

