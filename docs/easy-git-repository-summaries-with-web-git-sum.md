# 使用 Web-git-sum 的简易 Git 存储库摘要

> 原文：<https://hackaday.com/2019/03/25/easy-git-repository-summaries-with-web-git-sum/>

对于那些托管自己的 git 存储库的人来说，有许多创建方便的 web 可访问前端的解决方案，但是[mitxela]对其中任何一个都不太满意。在尝试了许多备选方案并思考了他的需求之后，他意识到他真正需要的是一个列出最近提交的摘要页面，以及一个包含分支和标签列表的文件树。为此，他创建了 [web-git-sum](https://mitxela.com/projects/web-git-sum) 。这是一个 bash 脚本，运行在 git 的 post-receive 钩子上，只生成两个文件:一个摘要页面和一个存储库索引。你可以在 git.mitxela.com 的[看到输出的演示。](https://git.mitxela.com/)

[mitxela]的文章详细介绍了 git 存储库是如何工作的，这些存储库是如何通过 HTTP 提供服务的，并涵盖了提供方便和可访问的 web 前端的一些不同选项。并不是所有的存储库都是一样的，对一个库有效的可能对另一个库不一定有效或者不能很好地扩展。

对私有 git 服务器的想法感兴趣？我们详细介绍了如何设置一个(剧透:真的很简单。)