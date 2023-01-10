# Lambdas 代表 C——算是吧

> 原文：<https://hackaday.com/2019/09/11/lambdas-for-c-sort-of/>

现在很多编程语言都有 lambda 函数，或者我很乐意称之为匿名函数。有些人小题大做，但核心思想非常简单。有时候你需要一小段代码，你只在一个地方需要它——最常见的是，作为一个回调函数来传递另一个函数——那么为什么要给它一个名字呢？根据语言的不同，还可以有更多的东西，尤其是当你使用闭包和 currying 的时候。

例如，在 Python 中，map 函数将函数作为参数。假设你有一个列表，你想大写列表中的每个单词。Python 字符串有一个大写方法，您可以编写一个循环来将它应用于列表中的每个元素。然而，`map`和一个 lambda 可以更简洁地做到:

```
map(lambda x: x.capitalize(), ['madam','im','adam'])
```

这里的匿名函数接受一个参数 x，并对它调用 capitalize 方法。map 调用确保对每个项目调用一次匿名函数。

现代 C++有 lambda 表达式。然而，在 C 语言中，你必须通过名字定义一个函数并传递一个指针——这不是一个大问题，但是如果你有很多只使用一次的回调函数，那就麻烦了。很难想出那么多一次性函数的名字。然而，如果你使用 gcc，有一些非标准的 C 特性可以让你从 lambda 表达式中得到大部分你想要的东西。

## **为什么** GCC？

[![](img/4df70e432e7c225c0152961c297911bb.png)](https://hackaday.com/wp-content/uploads/2019/08/gcc.png) 你必须使用 gcc，因为这一招使用了两个不标准的语言特性。首先，gcc 允许嵌套函数。此外，您可以使用语句表达式。这是一个可以做函数所能做的一切的表达式。

这两件事，再加上对预处理器的滥用，可以让您将函数代码填充到您需要的地方，并让您不必为了传递给另一个子例程而命名您编写的每一个小函数。

如果您使用另一个编译器，它可能没有——事实上，可能没有——这些特性。不过，最后，你总是可以使用一个带有指针的适当函数。这个稍微好一点。

## 让我们**开始**

[![](img/6436e10bbb011eea054ff7ebbe845bb8.png)](https://hackaday.com/wp-content/uploads/2019/09/lambda.png) 我创建了一个简单的例子，你可能想在 c 中使用 lambda。你可以在 [GitHub](https://github.com/wd5gnr/clambda/blob/master/clambda0.c) 上找到它。有一个浮点数数组，`thelist`，和两个处理列表的函数。将每个值乘以 2 后，对列表进行平均。另一个执行相同的任务，但是首先将每个条目除以 3。

毫无疑问，这是一个人为的例子，但是很容易理解。如果你研究代码，两个平均函数`average2x`和`averagethird`几乎是一样的。唯一的区别是数学上的一点不同。

现在看[这个版本](https://github.com/wd5gnr/clambda/blob/master/clambda1.c)。这里，`average_apply`函数完成了所有的平均工作，但是它需要一个函数指针`fn`来完成你想要的数学运算。有两个函数来计算:

```
float twox(float x) { return 2*x; }
float xdiv3(float x) { return x/3; }
```

那么打电话就很容易了:

```
printf("%f\n", average_apply(twox));
printf("%f\n", average_apply(xdiv3));
```

## 当然…

这些小代码片段现在需要名字，我们不会在其他地方使用它们。那是 lambda 的最佳地点。你可以把它放在一个头文件中(虽然我只是把它放在了文件的顶部，例如):

```
#define lambda(lambda$_ret, lambda$_args, lambda$_body)\
({\
lambda$_ret lambda$__anon$ lambda$_args\
lambda$_body\
&amp;lambda$__anon$;\
})
```

这利用了我提到的 gcc 特性，以及 gcc 允许在标识符中使用美元符号的事实。这意味着您可能需要在 gcc 命令行上传递`-std=gnu99`来使其正常工作。这应该可以做到:

```
gcc -o clambda2 --std=gnu99 clambda2.c
```

现在，这些调用只是将这些函数放在了一起:

```
printf("%f\n", average_apply(lambda(float,(float x),{ return 2*x; })));
printf("%f\n", average_apply(lambda(float,(float x),{ return x/3.0; })));
```

顺便说一下，我知道你可以给一个函数传递一个因子 2 或 0.3333，但这不是重点。这些功能可以像你喜欢的那样复杂。像大多数编程问题一样，有许多方法可以解决这个问题。

## 警告

有一些警告。你不能指望 lambda 的作用域超出封闭函数，这样异步回调就不会起作用。在封闭范围内访问局部变量是不确定的。考虑以下代码:

```
int factor=10;
printf("%f\n",average_apply(lambda(float,(float x),{ return x/factor; })));
```

这可以编译，应该可以工作。对于这个[在线编译器](https://rextester.com/l/c_online_compiler_gcc)来说，它确实有效。但是，使用 Windows 10 的 Linux 系统，同样的代码会 seg fault。事实上，如果您没有设置 gcc -O2 选项，其他示例也会出现 seg 故障。在我的 Linux 机器上，它运行良好。我不知道这是 Windows 的错误还是 Linux 只是在掩盖错误。然而，看起来如果它能编译，它应该能工作，而且大多数情况下，它确实能工作。

## 在实践中

当然，你不一定要有带 c 的 lambdas，即使你想要，它们也不是很便携。但是，看看一些 gcc 特有的编译器特性是如何工作的仍然很有趣，并且尝试匹配它也是一项有趣的智力练习。

这项技术并不新鲜。如果你搜索，你可以在不同的地方找到相当多的相同想法的帖子，尽管每一个都有小的变化。当然，在最近[年份](https://hackaday.com/2019/07/30/c20-is-feature-complete-heres-what-changes-are-coming/)的 C++中，你可以毫无问题地使用 lambdas。顺便说一下，lambdas 也风靡了[云计算](https://hackaday.com/2018/01/17/an-alexa-skill-among-other-things-in-a-few-minutes/)，这是一个类似的想法。一个无需等待服务器请求就能运行的小功能。

GCC 标志 [GFDL。](https://en.wikipedia.org/wiki/en:GNU_Free_Documentation_License)