# 逐步创建编译器

> 原文：<https://hackaday.com/2022/11/27/create-a-compiler-step-by-step/>

虽然 JavaScript 可能不是编写产品编译器的理想语言，但您可能会喜欢[“创建您自己的编译器”教程](https://citw.dev/tutorial/create-your-own-compiler)，它对“[超级小编译器](https://github.com/jamiebuilds/the-super-tiny-compiler)”进行了带注释的演练，并教您从头开始编写编译器的基础知识。

超级小编译器本身大约有 200 行代码。源代码很好，超过 1000 个，但那是因为[识字编程](https://en.wikipedia.org/wiki/Literate_programming)的评论。花哨的标题注释大约是实际编译器的一半大。

编译器的目标是获取 Lisp 风格的函数，并将它们转换成等价的 C 风格的函数调用。例如:`(add 5 (subtract 3 1)`会变成`add(5,subtract(3,1))`。

当然，有几种快捷方法可以很容易地做到这一点，但是编译器使用的结构与大多数成熟的现代编译器一样。有一个解析器，一个抽象表示阶段，和代码生成。

即使你不喜欢幻灯片放映的方式，有文化的评论 JavaScript 易于阅读，非常有教育意义。如果你不知道 JavaScript，如果你知道任何通用的编程语言，它应该还是很容易解决的。

页面的左下方有两个按钮:详细和内部。你可以随时按这些。由 verbose 按钮产生的文本旁边会有一条蓝线，关于内部的文本旁边会有一条红线。这允许你根据你想要阅读的细节来调整体验。

这个[并不是我们看到的第一个被分解的编译器。如果你对现有编译器为源输入生成的内容感兴趣，我们总是对](https://hackaday.com/2020/01/05/all-youve-ever-wanted-to-know-about-compilers/)[编译器浏览器](https://hackaday.com/2019/09/13/peek-into-the-compilers-code-lots-of-compilers/)印象深刻。