# 学习 Python 的循环方式:解释迭代器和生成器

> 原文：<https://hackaday.com/2018/09/19/learn-to-loop-the-python-way-iterators-and-generators-explained/>

如果你曾经编写过 Python，很可能你已经使用过迭代器而没有意识到这一点。自己编写并在程序中使用它们可以显著提高性能，尤其是在处理大型数据集或在资源有限的环境中运行时。它们还可以让你的代码更优雅，给你“Pythonic 式的”吹嘘的权利。

在这里，我们将通过细节，并向您展示如何推出自己的产品，同时说明它们为什么有用。

您可能熟悉 Python 中使用英式语法的对象循环，如下所示:

```

people = [['Sam', 19], ['Laura', 34], ['Jona', 23]]
for name, age in people:
    ...

info_file = open('info.txt')
for line in info_file:
    ...

hundred_squares = [x**2 for x in range(100)]

&quot;, &quot;.join([&quot;Punctuated&quot;, &quot;by&quot;, &quot;commas&quot;])

```

由于迭代器的魔力，这类语句是可能的。为了解释能够编写自己的迭代器的好处，我们首先需要深入一些细节，解开实际发生的事情。

# 迭代器和可迭代对象

迭代器和可迭代对象是两个不同的概念。这些定义看起来很难理解，但是它们非常值得理解，因为它们会使其他事情变得容易得多，特别是当我们开始享受发电机的乐趣时。和我们在一起！

## 迭代程序

一个**迭代器**是一个表示数据流的对象。更准确地说，是具有`__next__`方法的对象。当你使用 for-loop、list comprehension 或其他任何遍历对象的方法时，在后台的迭代器上调用`__next__`方法。

好吧，那我们来举个例子。我们所要做的就是创建一个实现`__next__`的类。我们的迭代器将只给出指定数字的倍数。

```

class Multiple:
    def __init__(self, number):
        self.number = number
        self.counter = 0

    def __next__(self):
        self.counter += 1
        return self.number * self.counter

if __name__ == '__main__':
    m = Multiple(463)
    print(next(m))
    print(next(m))
    print(next(m))
    print(next(m))

```

运行此代码时，它会产生以下输出:

```

$ python iterator_test.py
463
926
1389
1852

```

我们来看看是怎么回事。我们创建了自己的类，并定义了一个`__next__`方法，每次调用它都会返回一个新的迭代。迭代器总是需要记录它在序列中的位置，我们使用`self.counter`来做这件事。我们没有调用对象的`__next__`方法，而是在对象上调用了`next`。这是推荐的做事方式，因为它更好读，也更灵活。

酷毙了。但是如果我们尝试在 for 循环中使用它，而不是手动调用`next`，我们会发现有些不对劲。

```

if __name__ == '__main__':
    for number in Multiple(463):
        print(number)

```

```

$ python iterator_test.py
Traceback (most recent call last):
  File &quot;iterator_test.py&quot;, line 11, in &lt;module&gt;
    for number in Multiple(463):
TypeError: 'Multiple' object is not iterable

```

什么？不可迭代？但它是一个迭代器！

这就是迭代器和可迭代的区别变得明显的地方。我们上面写的 for 循环需要一个 iterable。

## 可重复的

一个**可迭代的**是一个*能够*迭代的东西。实际上，iterable 是一个具有`__iter__`方法的对象，该方法*返回一个迭代器*。这看起来有点奇怪，但是它确实有很大的灵活性；让我们解释一下为什么。

当在对象上调用`__iter__`时，它必须返回一个迭代器。迭代器可以是一个外部对象，可以在不同的可迭代对象之间重用，或者迭代器可以是`self`。没错:iterable 可以简单地将自身作为迭代器返回！这为编写一个紧凑的万能类提供了一个简单的方法，它可以做我们需要的一切。

![](img/df19a57e294547f8d561da4566db1c70.png)

澄清一下:字符串、列表、文件和字典都是可迭代的例子。它们本身就是数据类型，但是如果你试图以任何方式循环它们，它们都会自动运行良好，因为它们本身返回一个迭代器。

记住这一点，让我们通过简单地添加一个返回`self`的`__iter__`方法来修补我们的`Multiple`示例。

```

class Multiple:
    def __init__(self, number):
        self.number = number
        self.counter = 0

    def __iter__(self):
        return self

    def __next__(self):
        self.counter += 1
        return self.number * self.counter

if __name__ == '__main__':
    for number in Multiple(463):
        print(number)

```

它现在按照我们的预期运行。它也永远继续下去！我们创建了一个无限迭代器，因为我们没有指定任何最大条件。这种行为有时是有用的，但通常我们的迭代器在耗尽之前需要提供有限数量的条目。下面是我们如何实现最大限制:

```

class Multiple:
    def __init__(self, number, maximum):
        self.number = number
        self.maximum = maximum
        self.counter = 0

    def __iter__(self):
        return self

    def __next__(self):
        self.counter += 1
        value = self.number * self.counter

        if value &gt; self.maximum:
            raise StopIteration
        else:
            return value

if __name__ == '__main__':
    for number in Multiple(463, 3000):
        print(number)

```

为了表示我们的迭代器已经用尽，定义的协议将引发`StopIteration`。任何处理迭代器的结构都会为此做好准备，比如我们例子中的 for 循环。运行时，它会正确地停在适当的点上。

```

$ python iterator_test.py
463
926
1389
1852
2315
2778

```

# 偷懒是好的

那么，为什么能够编写我们自己的迭代器是值得的呢？

许多程序需要迭代生成的大量数据。传统的方法是计算列表的值并填充它，然后循环整个过程。然而，如果您正在处理大型数据集，这会占用相当大的内存。

正如我们已经看到的，迭代器可以按照惰性求值的原则工作:当你在迭代器上循环时，根据需要生成值。在许多情况下，使用迭代器或生成器的简单选择可以显著提高性能，并确保您的程序在使用比测试时更大的数据集或更小的内存时不会出现瓶颈。

现在我们已经快速浏览了一下，了解了发生了什么，我们可以转到一个更干净、更抽象的工作方式:生成器。

# 发电机

你可能已经注意到在上面的例子中有相当多的样板代码。生成器使得构建你自己的迭代器更加容易。没有对`__iter__`和`__next__`的大惊小怪，我们也不必跟踪内部状态或担心引发异常。

让我们把我们的多机重写为一个生成器。

```

def multiple_gen(number, maximum):
    counter = 1
    value = number * counter

    while value &lt;= maximum:
        yield value
        counter += 1
        value = number * counter

if __name__ == '__main__':
    for number in multiple_gen(463, 3000):
        print(number)

```

哇，这比我们的迭代器例子短多了。主要要注意的是一个新的关键词:`yield`。`yield`类似于`return`，但是它不是终止函数，而是简单地暂停执行，直到需要另一个值。相当整洁。

在大多数情况下，当您生成值，将它们追加到一个列表中，然后返回整个列表时，您可以简单地`yield`每个值！它可读性更好，代码更少，并且在大多数情况下性能更好。

谈了这么多关于性能的问题，是时候测试迭代器了！

这是一个非常简单的程序，将我们上面的多机与“传统的”列表方法进行比较。我们生成 463 的倍数，最高可达 100，000，000，000，并记录每个策略需要的时间。

```

import time

def multiple(number, maximum):
    counter = 1
    multiple_list = []
    value = number * counter

    while value &lt;= maximum:
        multiple_list.append(value)
        value = number * counter
        counter += 1

    return multiple_list

def multiple_gen(number, maximum):
    counter = 1
    value = number * counter

    while value &lt;= maximum:
        yield value
        counter += 1
        value = number * counter

if __name__ == '__main__':
    MULTIPLE = 463
    MAX = 100_000_000_000

    start_time = time.time()
    for number in multiple_gen(MULTIPLE, MAX):
        pass
    print(f&quot;Generator took {time.time() - start_time :.2f}s&quot;)

    start_time = time.time()
    for number in multiple(MULTIPLE, MAX):
        pass
    print(f&quot;Normal list took {time.time() - start_time :.2f}s&quot;)

```

我们在一些不同规格的 Linux 和 Windows 机器上运行了这个。平均来说，生成器方法快了三倍，几乎不占用任何内存，而普通的列表方法很快就占用了所有的 RAM 和相当大的交换空间。有几次，当普通的列表方法在 Windows 上运行时，我们得到了一个`MemoryError`。

# 生成器理解

您可能熟悉 list comprehensions:从 iterable 创建列表的简明语法。这里有一个例子，我们计算列表中每个数字的立方。

```

nums = [2512, 37, 946, 522, 7984]

cubes = [number**3 for number in nums]

```

碰巧我们有一个类似的构造来创建生成器(官方称为“生成器表达式”，但它们几乎与列表理解相同)。就像用`[]`换`()`一样简单。Python 提示符下的快速会话证实了这一点。

```

&gt;&gt;&gt; nums = [2512, 37, 946, 522, 7984]
&gt;&gt;&gt; cubes = [number**3 for number in nums]
&gt;&gt;&gt; type(cubes)
&lt;class 'list'&gt;
&gt;&gt;&gt; cubes_gen = (number**3 for number in nums)
&gt;&gt;&gt; type(cubes_gen)
&lt;class 'generator'&gt;
&gt;&gt;&gt;

```

同样，在上面的例子中不太可能有太大的不同，但这是一个两秒钟的变化，确实很方便。

# 摘要

当您处理大量数据时，明智地使用资源至关重要，如果您可以一次处理一项数据，那么迭代器和生成器就是不二之选。我们上面谈到的许多技术只是常识，但是它们以一种定义好的方式被构建到 Python 中的事实是很棒的。一旦你尝试了迭代器和生成器，你会发现自己惊人地频繁使用它们。