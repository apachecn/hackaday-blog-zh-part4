# 在 ESP32 上呈现 HTML 和 CSS

> 原文：<https://hackaday.com/2022/03/18/render-html-and-css-on-an-esp32/>

随着可负担得起的微控制器的可用计算能力不断增加，它们与能够运行基于 Linux 的操作系统的较低层应用处理器之间的界限不可避免地变得模糊。在很大程度上，微控制器忙于幕后任务，但正如这里的许多项目所展示的那样，当涉及到面向用户的应用时，它们也非常能干。现在[Andy Green]通过在 ESP32 上为 libwebsockets 制作了一个基于 h2 的概念验证 HTML + CSS 渲染器[，扩展了平价硅的可能性。在微控制器上上网冲浪而不满足于纯文本体验？为什么不呢！](https://libwebsockets.org/git/libwebsockets/tree/READMEs/README.html-parser.md)

他坦率地承认，这远远不是一个完整的 HTML 呈现引擎，因为虽然它可以解析和呈现支持 JPEG 和 PNG 图像的 HTML 和 CSS，但它只能处理 HTML 的子集，并且不能容忍任何畸形。也没有 JS 支持，考虑到可用的资源，这不足为奇。

尽管有这些限制，它仍然是一件令人印象深刻的作品，我们希望有一天能够在诸如 badge . team European conference badges 这样的设备上显示 Hackaday。绝对值得一看的项目！