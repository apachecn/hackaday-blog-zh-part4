# 使用网络浏览器复选框玩毁灭战士(最后)

> 原文：<https://hackaday.com/2021/10/18/play-doom-using-web-browser-checkboxes-finally/>

如果你曾经觉得有必要只使用网络浏览器的复选框来渲染《毁灭战士》，[Andrew Healey]已经用他的第一人称射击游戏的最近端口覆盖了你。自然，这得到了我们*的赞同。*

是的，你没看错。你现在可以在一个 160 x 100 的 HTML 格式的复选框中玩毁灭战士，就像这样:☑.这个项目的秘密来源于另一位黑客 Brian Braun 的令人着迷的 Checkboxland 项目，他使用 HTML 复选框来生成各种艺术演示。

[Andrew Healey]还利用了 Cornelius Diekmann 的《末日之港》中的 WebAssembly，我们最近在 Hackaday 上讨论过。少量代码将两个项目捆绑在一起，最终结果是 160×100 分辨率，完全用 HTML 复选框呈现。

端口可以使用 Chrome 或 Edge 在这里播放[(其他浏览器如果不支持 CSS 中的`zoom`属性可能会有问题)。源代码也可以在](https://healeycodes.github.io/doom-checkboxes/) [GitHub](https://github.com/healeycodes/doom-checkboxes) 上获得。

虽然分辨率和调色板不是我们从厄运中期待的，但很可能通过修补抖动和阈值设置来进一步改善图形。通过进一步优化，更高的分辨率也是可能的。

我们将很难选择我们最喜欢的毁灭之港，因为名单[变得相当长](https://hackaday.com/tag/doom/)。然而，对于一些完全不同的东西，看看我们关于[末日如何被带到 Twitter](https://hackaday.com/2021/10/13/doom-played-by-tweet/) 的故事。

 <https://hackaday.com/wp-content/uploads/2021/10/Doom-via-Checkboxes_1.mp4?_=1>

[https://hackaday.com/wp-content/uploads/2021/10/Doom-via-Checkboxes_1.mp4](https://hackaday.com/wp-content/uploads/2021/10/Doom-via-Checkboxes_1.mp4)

感谢[Dan]的精彩提示。