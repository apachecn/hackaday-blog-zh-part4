# 为 PythonAnywhere 和 GitHub 制作更新服务器

> 原文：<https://hackaday.com/2019/06/25/making-an-update-server-for-pythonanywhere-and-github/>

基于云的 ide 和开发工具已经发展了很多年，尽管大多数都有自由层的限制，并且可能不完全兼容其他服务，比如 GitHub。[Aadi Bajpai]喜欢使用 PythonAnywhere，也喜欢使用 GitHub 进行协作，所以他做了一个[更新服务器，一旦你推送 Github](https://medium.com/@aadibajpai/deploying-to-pythonanywhere-via-github-6f967956e664) ，它就会自动更新运行代码

PythonAnywhere 允许您通过 web 浏览器访问 python shell，还允许您运行可以通过自定义子域访问的 web 应用程序。尽管它没有与 GitHub 直接集成，但是您可以使用 bash shell 来访问 git 客户端。

在这次攻击中，[Aadi Bajpai]利用了 GitHub 的 webhooks，当检测到推送事件时就会触发这些 web hooks。运行在 PythonAnywhere 上的 flask 服务器被编写为一旦被 get POST 请求触发，它就在本地执行来自存储库的 git pull。还有一点工作，允许添加一点安全酱到食谱中，但这是一个非常优雅的解决方案，也可以用于其他情况。

[设置提醒通知](https://hackaday.com/2018/12/30/pushbutton-%e2%86%92-push-notification/)已经被证明是一项有趣的任务，尽管整合通知的不和谐或松弛增加了一点吹嘘的权利。