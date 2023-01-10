# 约瑟夫·普鲁萨想让你改变文件格式

> 原文：<https://hackaday.com/2019/11/01/josef-prusa-wants-you-to-change-file-formats/>

我们都经历过。你在 Thingiverse 上找到了那个时尚弄潮儿模型——我们不会评价。您下载了 STL，准备好观看它在您的打印床上实现的魔力。但切片机抱怨说它不是多方面的或防水的或类似的东西。多么令人失望。这部分是由于 STL 文件格式的缺点。有一种更新的格式，3MF，Josef Prusa 和 Jakub Koí[希望你开始使用它](https://blog.prusaprinters.org/3mf-file-format-and-why-its-great/)。

STL——stereo lithography 的缩写——是一种简单的格式，只保存一堆三角形。如果您需要零件的任何信息，如颜色或材料。更糟糕的是，在我们假设的例子中，没有关于三角形如何关联的定义，所以你可以创建“坏的”STL 文件。即使是格式正确的文件也很难处理。例如，您可能以英寸为单位进行缩放，而文件设置为毫米。

原来 3MF 实际上是一个 ZIP 存档，它可以包含很多信息。该文件可以包含一个或多个模型、颜色、切片数据、版权、图像等等。由于压缩，ZIP 文件通常也更短。不过，最重要的是，这种文件格式不允许非流形模型，并且消除了歧义，因此一切都可以很好地打印出来。如果你的切片器将数据存储到文件中——就像 Prusa 一样——其他使用相同软件的人也可以获取你的设置。

这种格式其实并不新鲜——它出现在 2015 年左右——但还没有被广泛采用。Prusa 鼓励你在 3MF 中上传模型，即使你也为还没有转换的人添加了一个 STL 副本。

所以你会开始用 3MF 吗？或者你已经是了？他们说，文件格式是开放的。所以如果你最喜欢的工具不喜欢 3MF，你可以自己添加支持。

 [https://www.youtube.com/embed/BABdR9d8Cp4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BABdR9d8Cp4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

