# 已经有那本书了？通过 IoT 获取 ISBN 411

> 原文：<https://hackaday.com/2020/09/27/already-have-that-book-get-the-isbn-411-over-iot/>

你有没有在书店偶然发现一本你一直在寻找的好书，但却有一种挥之不去的感觉，你已经把它放在家里了？是啊，我们也是。如果我们上次有类似于[Kutluhan Aktar]的 ISBN 验证器的东西来确定我们是否已经有了它就好了。

为了使用这个方便的机器，[Kutluhan]在 4 x 4 薄膜键盘上输入相关书籍的国际标准书号(ISBN)。Arduino Nano 33 IoT 获取该 ISBN，并对照用 ISBN、标题、作者和页数创建的图书条目 PHP web 数据库[Kutluhan]进行检查。然后，它通过更新诺基亚 5110 的显示屏，让[Kutluhan]知道他们是否已经有了它。

如果你想在下次去书店之前做一个，这个项目是完全开源的。除非你不介意你的书虫同伴们害羞、好奇的目光，否则你可能想找出某种封闭的方式。

因为不知道下一步该读什么而停止阅读？查看我们的书籍，你应该阅读专栏,回到你的精神剧场中自娱自乐。

通过 [r/duino](https://www.reddit.com/r/arduino/comments/ivryr1/iot_isbn_verifier_w_nano_33_iot_and_nokia_5110/)