# 用壁垒挤压烟囱

> 原文：<https://hackaday.com/2022/11/24/squish-that-stack-with-rampart/>

[P . B . Richards]和[Aaron Flin]哀叹现代 JavaScript 环境的资源饥渴，并计划开发一个内存和 CPU 更少的系统，更适合低端平台。想想 Nginx、NodeJS 和您的数据库风格，以及所有这些都需要多少资源才能正常运行。现在试着把这些放在一个树莓馅饼上。嗯，他们做到了，创造了 [Rampart:一个基于 JavaScript 的完整栈开发环境](https://www.rampart.dev/) 。

通常的网络应用程序有很多技巧来优化速度，但据开发者称，Rampart 仍然相当快。它存在的原因纯粹是关于资源使用，从屏幕截图来看，Rampart HTTP 服务器的内存不到 10 MB。它似乎支持相当多的技术，如 HTTPS、WebSockets、SQL search、REDIS，以及各种实用程序和操作系统功能，所以不应该太轻量级，以至于开发重要的应用程序需要太多的工作。他们提出的一个有趣的观点是，当部署到现代服务器农场时，Rampart 如此节俭可能会相当高效。无论如何，如果您有一个合理的应用程序可以嵌入到一个小平台上，那么这可能值得一看。

这些年来，我们已经看到了很多 JavaScript 运行时，比如最近的[](https://hackaday.com/2022/07/08/a-new-javascript-runtime-fresh-out-of-the-oven/)，但是总会有更多的空间。