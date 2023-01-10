# 告别 YouTube 子计数器设置为打破与 API 的变化

> 原文：<https://hackaday.com/2019/08/01/a-farewell-to-youtube-sub-counters-set-to-break-with-api-change/>

十年前，你可能从未想到你会需要这些东西，YouTube 用户计数器可能会排名很高。你可能已经猜到，一个数字每上升一点，多巴胺就会让人上瘾？

事实证明，很多人都想记录他们的在线粉丝总数，一个令人眼花缭乱的用户计数器生态系统已经出现。所有这些都依赖于 YouTube 为此目的而公开的 API，正如[Brian Lough]指出的那样[即将改变和打破所有的订阅计数器](https://www.youtube.com/watch?v=sHNI-WgN-UQ)。在 YouTube sub counter 领域，[Brian]既是推动者，也是其他 YouTube 显示的系列构建者。他为[构建了一个 Arduino 包装器来轻松获取 YT sub counts](https://github.com/witnessmenow/arduino-youtube-api)。下面的视频展示了他的作品，许多基于 RGB LED 矩阵显示器，就像在[他的俄罗斯方块主题子计数器](https://hackaday.com/2018/06/19/a-youtube-subscriber-counter-with-a-tetris-twist/)中使用的一样。它们都构建得很好，看起来很漂亮，但遗憾的是，当 API 在 8 月份发生变化时，它们注定会过时。

[API 变化的细节](https://support.google.com/youtube/thread/6543166)于 4 月公布，对于 subs 计数，它相当于舍入计数并显示大的计数，例如，510k 而不是 510，023。我们相信[Brian]和其他显示构建者将能够通过代码更改来挽救他们的一些计数器，但其他计数器可能需要硬件更改。谢谢你，YouTube。

 [https://www.youtube.com/embed/sHNI-WgN-UQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sHNI-WgN-UQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

