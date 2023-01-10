# 不用浏览器就能上网

> 原文：<https://hackaday.com/2022/01/17/hack-the-web-without-a-browser/>

这是一个经典问题。你想在你的程序中使用数据，但它是在网页上。当然，有些网站有 API，但通常情况下，你只能靠自己。您可以通过 HTTP 加载整个页面并解析它。或者你可以用一些工具来“刮”网站。一个有趣的方法是 woob——浏览器之外的网络。

该系统使用一系列在特定站点定制的后端。有一个官方后端的集合，你也可以创建自己的。一旦你有了一个后端，你就可以配置它并从 Python 中使用它。下面是一个查找银行账户余额的示例:

```
>>> from woob.core import Woob
>>> from woob.capabilities.bank import CapBank
>>> w = Woob()
>>> w.load_backends(CapBank)
{'societegenerale': <Backend 'societegenerale'>, 'creditmutuel': <Backend 'creditmutuel'>}
>>> pprint(list(w.iter_accounts()))
[<Account id='7418529638527412' label=u'Compte de ch\xe8ques'>,
<Account id='9876543216549871' label=u'Livret A'>,
<Account id='123456789123456789123EUR' label=u'C/C Eurocompte Confort M Roger Philibert'>]
>>> acc = next(iter(w.iter_accounts()))
>>> acc.balance
Decimal('87.32')
```

可用后端的列表令人印象深刻，但是最终，您会想要创建自己的模块。幸运的是，有很多关于如何做到这一点的文档。该框架允许您将数据发布到网站上，并轻松阅读结果。每个后端也有一个测试，可以检测网站的变化是否破坏了代码，这是这种方案的常见问题。

我们没有看到黑客日后端。太糟糕了。然而，有许多基于控制台和使用 QT 的应用程序示例。例如，您可以搜索电影、管理食谱或约会网站。

当然，这个问题有许多可能的解决方法。也许你需要弄清楚[的下一班火车什么时候离开](https://hackaday.com/2013/01/08/picture-frame-that-scrapes-train-times-from-the-web/)。