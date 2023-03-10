# 将 GitHub 转变为 URL 缩短服务

> 原文：<https://hackaday.com/2020/11/18/turning-github-into-a-url-shortening-service/>

像 TinyURL 或 Bitly 这样的 URL 缩短服务早已成为现代网络的一个重要组成部分，并且非常受欢迎，甚至谷歌也已经关闭了自己的服务。创建自己的 shortener 也是一项有趣的工作，它的核心只需要一个漂亮的域名、某种形式的数据库来映射 URL，以及一点 web 技术来将它们粘合在一起。[Nelsontky]认为你甚至不必自己构建它的大部分，[但是你可以(ab)使用 GitHub 来完成它](https://github.com/nelsontky/gh-pages-url-shortener)。

使用 GitHub 页面托管 URL 缩短网站本身，[nelsontky]实际上是重新利用 GitHub 的问题跟踪系统，将缩短的标识符映射到原始 URL。每次重定向都是一个新的问题，问题编号作为缩短标识符，问题的标题文本存储原始 URL。为了映射请求，一段 JavaScript 从请求中提取问题号，通过 GitHub API 查找，如果找到有效的问题号(并且没有超出 API 速率限制)，就相应地重定向调用者。特别巧妙的是，GitHub Pages 通常只为存储在存储库中的静态文件提供服务，因此整个重定向逻辑实际上放在 404 错误处理页面中，允许对任意路径的请求。

虽然这可能不如[将你的整个网站内容直接放入 URL 本身](https://hackaday.com/2018/07/07/tiny-websites-have-no-server/)那么简洁，但它可以很好地结合[和这个旋转式电话](https://hackaday.com/2019/07/23/control-your-web-browser-like-its-1969/)来简单地拨打问题号码并访问你的书签——如果你一直想要自己的网站电话簿，这是完美的。如果你不喜欢每次想添加新 URL 时都要与 GitHub UI 交互的想法，[可以试试命令行工具](https://hackaday.com/2020/02/15/github-goes-gui-less/)。