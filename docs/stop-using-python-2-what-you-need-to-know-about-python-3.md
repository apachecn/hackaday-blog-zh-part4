# 停止使用 Python 2:关于 Python 3 你需要知道什么

> 原文：<https://hackaday.com/2018/08/15/stop-using-python-2-what-you-need-to-know-about-python-3/>

尽管 Python 3 在 2008 年发布，但许多项目仍然停留在 Python 2 上。

可以理解的是，将大型现有代码库移植到新版本会让许多开发人员不寒而栗。但是代码不可避免地需要维护，所以当所有可以修复一切的闪亮新特性都出现在新版本中时，扎根于过去真的值得吗？

我们将带您了解 Python 2 程序从 3.0 到当前版本(3.7)都缺少的一些特性。

## Python 3 为什么会出现

2008 年之前，Python 开发者有点头疼。这种始于 1989 年圣诞节的语言是吉多·范·罗苏姆的宠儿，现在正以飞快的速度发展。功能已经被添加，项目现在已经足够大，以至于早期的设计决策阻碍了实现。正因为如此，添加新特性的过程变成了围绕现有代码的一次黑客攻击。

解决方案是 Python 3:唯一一个故意破坏向后兼容性的版本。当时，这个决定是有争议的。一个公开使用的开源项目故意破坏旧代码是可以接受的吗？尽管遭到强烈反对，但还是做出了决定，这给了 Guido 和开发人员一个一次性的机会来清除多余的代码，修复常见的缺陷并重新设计语言。目标是在 Python 3 中只有一种显而易见的做事方式。十年后，我们仍在使用 3.x 版本，这证明了当时所做的设计选择。

## _ _ 未来 __ 就是现在

`__future__`导入是时间旅行的一部分，它允许你从 Python 的未来版本中选择一些特性。事实上，当前的 Python 版本 3.7 包含了来自尚未编写的版本的`__future__`导入！

好吧，没那么夸张，一个`__future__`导入只是一个打开新语法的明确指示器，新语法是当前版本的一部分。我们认为我们应该提到它，因为[下面列出的一些 Python 3 特性](https://docs.python.org/2/library/__future__.html)可以在 2.6 和 2.7 中导入和使用`__future__`，这两个版本分别在 3.0 和 3.1 中发布。话虽如此，当然还是建议升级，因为新功能在过去的版本中是“冻结”的，不会从当前版本的发展和维护中受益。

在 Python 3 中你错过了什么…

## 打印是一种功能

是的，我们知道大多数人都意识到了这一点，但这是皮达尼斯最常用的说法之一。`print`从一个关键字移到一个函数，这样才有意义。

这段 Python 2 代码

```

print "Fresh Hacks Every Day"
print "Foo", "some more text on the same line as foo"

```

在 Python 3 中会变成下面这样。

```

print("Fresh Hacks Every Day")
print("Foo", end='')
print("some more text on the same line as foo")

```

## 加大拆包力度

这里我们有一个包含一些数据的元组。在 Python 2 中，我们已经可以解包成不同的变量，如下所示:

```

person = ("Steve", "Hammond", 34, "England", "spaces")
name, surname, age, country, indent_pref = person

```

但是假设我们只关心名字和缩进偏好。在 Python 3 中，我们现在可以这样解包:

```

person = ("Steve", "Hammond", 34, "England", "spaces")
name, *misc, indent_pref = person

# These would also work
name, surname, age, *misc = person
*misc, indent_pref = person

```

这在解包时提供了更大的灵活性——如果处理的元组比本例中的元组更长，这将非常方便。

解包通常用在 for 循环中，尤其是当使用像`zip()`或`enumerate()`这样的东西时。作为应用新语法的一个例子，我们现在有一个函数`get_people_data()`，它返回一个元组列表，就像上面的`person`例子一样。

```

for name, *misc, indent_pref in get_people_data():
    if indent_pref is not "spaces":
        print(f"You will feel the full wrath of PEP 8, {name}.")

```

这很有效。但是，如果我们能够以一种比字符串更好的方式存储缩进偏好，那不是很好吗？类似于 C 语言中的`enum`？

## 枚举

Python 中的枚举。多好的款待啊。由于大众的需求，它们从 3.4 开始就在标准库中了。

现在我们可以这样定义缩进偏好:

```

from enum import Enum

class Indent(Enum):
    SPACES = 'spaces'
    TABS = 'tabs'
    EITHER = 'either'

person = ("Steve", "Hammond", 34, "England", Indent.SPACES)
# or
person = ("Steve", "Hammond", 34, "England", Indent("spaces"))

# Let's try and initialise with an invalid value
person = ("Steve", "Hammond", 34, "England", Indent("invalid value"))
# 'ValueError: 'invalid value' is not a valid Indent

```

语法看起来有点奇怪，但在处理数字常量或字符串初始化时会很有用。

## 分开

一个简单但主要的变化是:在 Python 3 中除整数时，我们默认得到真正的浮点数除法(在 Python 2 中除两个整数总是得到一个整数结果)。

这是 Python 2 的行为:

```

>>> 1 / 3
0
>>> 5 / 2
2

```

而在 Python 3 中，我们获得了更高的准确性:

```

>>> 1 / 3
0.3333333333333333
>>> 5 / 2
2.5

```

如果需要，当然可以用于楼层整数划分。

如果您要将代码从 2 移植到 3，这种变化绝对应该注意到；这是一个容易被忽略的问题，可能会导致程序逻辑出现重大问题。

## 链接异常

捕捉一个异常，然后引发另一个异常是很常见的。这可能是因为您的应用程序有一组已定义的自定义异常，或者只是因为您希望提供更多关于出错原因的信息。

这里我们有一个程序，它粗略地计算出获得一定比例年薪所需的工作天数。

```

class InvalidSalaryError(Exception):
    pass

def days_to_earn(annual_pay, amount):
    """Return number of days worked to earn `amount`."""
    try:
        annual_frac = amount / annual_pay
    except ZeroDivisionError:
        raise InvalidSalaryError("Could not calculate number of days")
    return 365 * annual_frac

if __name__ == '__main__':
    print(days_to_earn(0, 4500))
    print(days_to_earn(20000, 4500))

```

我们可以看到，如果年薪被指定为零，并且发生了一个`ZeroDivisionError`,这将被捕获，并引发一个`InvalidSalaryError`。

让我们试着用 Python 2 运行这个。

```

$ python days_calc.py
Traceback (most recent call last):
  File "exception_chaining.py", line 13, in <module>
     print(days_to_earn(0, 4500))
  File "exception_chaining.py", line 9, in days_to_earn
    raise InvalidSalaryError("Could not calculate number of days")
__main__.InvalidSalaryError: Could not calculate number of days

```

因为我们捕获了`ZeroDivisionError`，它被吞掉了，所以只显示了`InvalidSalaryError`回溯。

现在让我们用 Python 3 来运行它。

```

$ python3 days_calc.py
Traceback (most recent call last):
  File "exceptions_chaining.py", line 7, in days_to_earn
    annual_frac = amount / annual_pay
ZeroDivisionError: division by zero

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "exceptions_chaining.py", line 13, in <module>
    print(days_to_earn(0, 4_500))
  File "exceptions_chaining.py", line 9, in days_to_earn
    raise InvalidSalaryError("Could not calculate number of days")
__main__.InvalidSalaryError: Could not calculate number of days

```

我们得到了一个更加详细的错误报告，解释了导致`InvalidSalaryError`的原因，并完成了对`ZeroDivisionError`的回溯。这在您使用他人编写的代码时特别有用，因为这些代码可能没有最详细的错误消息。

我们不会在这里深入讨论，但是也有新的`raise ... from`语法，它允许显式的异常链接。

### 附注:用 Python 处理大数

在上面的程序中，我们不得不处理成千上万的。写像`20000`或`0b001110100010`这样的长数字是眯着眼睛看屏幕的秘诀。把他们分开怎么样:`20_000`，`0b_0011_1010_0010`？这是 Python 3 使您的生活变得更简单的另一种方式——[数字文本中的可选下划线](https://www.python.org/dev/peps/pep-0515/)，这有助于使内容更具可读性。

## Unicode 和字节

在 Python 2 中，字节和字符串的概念基本上是可以互换的，两者都属于`str`类型。这导致了一些非常糟糕的转换结果和不可预测的行为。需要记住的是，在 Python 3 *中，所有的字符串都是 unicode* 。文本和字节之间的区别被有意地创造出来，提供了一种更加明确的工作方式。

在下面的例子中，我们在 Python 2 和 3 的解释器中测试了字节串、“正常”字符串和 unicode 字符串的类型。

Python 2.7:

```

>>> type(b'foo')
<type 'str'> # In Python 2, a bytestring is a normal string!
>>> type('foo')
<type 'str'> # The same bytes type as above
>>> type(u'foo')
<type 'unicode'>

```

Python 3.7:

```

>>> type(b'foo')
<class 'bytes'> # In Python 3, this has its own bytes type
>>> type('foo')
<class 'str'> # In Python 3, 'str' means unicode
>>> type(u'foo')
<class 'str'> # It's a normal string

```

这意味着在 Python 3 中处理编码要清晰得多，即使这是以多几个`.encode()`秒为代价的。有可能当你的程序与外界的任何东西通信时，比如文件或套接字，你将不得不编码和解码你的数据。

举个例子，如果你使用`pyserial`来读/写一个串行设备，你需要显式地编码和解码你的消息。

```

import serial

PORT = '/dev/ttyACM0'
BAUD = 115200
ENCODING = 'utf-8'

if __name__ == '__main__':
    ser = serial.Serial(port=PORT, baudrate=BAUD)

    ser.write('hello'.encode(ENCODING))
    response_bytes = ser.readline()
    response_str = response_bytes.decode(ENCODING)

```

## 字符串格式

Python 2 中格式化字符串的方式类似于 C:

```

author = "Guido van Rossum"
date = 1989
foo = "%s started Python in %d" % (author, date)

# Guido van Rossum started Python in 1989

```

文档明确指出，这种格式化方式“表现出各种各样的怪癖，导致许多常见的错误(例如无法正确显示元组和字典)”。它也不灵活，并且在处理长字符串时看起来变得很难看。

我们现在有两种格式化字符串的新方法。一个是超方便，一个是超强大。

### 格式化字符串文字

通常被称为“f 字符串”，它们提供了一种非常简单的方法来引用当前作用域中任何可用的变量。

检查这段代码的直观性和可读性:

```

author = "Guido van Rossum"
date = 1989
foo = f"{author} started Python in {date}"

# Guido van Rossum started Python in 1989

```

花括号内的任何内容都将被计算为一个表达式，所以如果您愿意，可以在字符串内放置小的逻辑或语句。在一个字符串中包含程序逻辑可能不太可读，但是如果它只是被记录以提供额外的调试信息，那么它真的很方便。

```

author = "Guido van Rossum"
date = 1989 
foo = f"{author.split()[0]} started Python {2000 - date} years before the turn of the century"

# Guido started Python 11 years before the turn of the century

```

### 的。格式方法

在 Python 3 中，每个字符串都有一个`.format`方法，它提供了一系列令人眼花缭乱的格式化选项，涵盖了绝大多数用例。我们在这里不做详细介绍，因为它被反向移植到了 2.6 和 2.7，所以对大多数 Python 2 用户来说不会是一个大的升级。

以下是我们最喜欢的指南之一供参考。

## 进口

假设您正在使用 Python 2，并且具有以下文件层次结构:

```
pkg
├──service.py
└──misc.py
run.py
utils.py
```

`run.py`简单地从`pkg`包中的`service`模块导入和调用一些东西。

但是`service.py`依赖于`utils.py`中包含的函数。所以在`service.py`的顶部我们有这样一句话。

```

import utils

```

似乎相当谦逊，一切都会很好。但是，如果我们的文件夹结构现在改变了，并且`pkg`获得了一个新的`utils`模块，该怎么办呢？

```
pkg
├──service.py
├──misc.py
└──utils.py
run.py
utils.py
```

混乱时刻:我们的代码现在在`pkg`中切换和使用`utils.py`文件。如果我们碰巧安装了一个名为`utils`的库，事情会变得更加混乱。这种方法没有得到足够的定义，并且一直导致 Python 2 中不可预测的行为。

Python 3 来拯救:如果不清楚导入应该是绝对的还是相对的，就不再支持语法。根据需要,`service.py`的顶部可以变成以下任何一个选项。

```

# To import from within pkg, either use relative
from . import utils
# or absolute
from pkg import utils

# To import from the same level as run.py, use absolute
import utils

```

在这个例子中，这个特性可能看起来有点精致，但是当处理包含大的包/导入层次结构的大代码库时，你会很高兴的。

## 其他的

有很多很多其他的特性提供了 Python 2 的改进和全新的特性，即使有些特性只在特定领域有用。以下是几个例子:

*   `asyncio`库的加入使得编写异步程序变得轻而易举。现代编程中的必备。
*   其他主要的标准库补充(如`concurrent.futures`、`ipaddress`和`pathlib`)
*   在 Python 2 中访问一个父类是不必要的语法负担。在 Python 3 中，`super()`变成了[更加神奇的](https://docs.python.org/3/library/functions.html#super)。
*   许多内置函数，如`zip()`、`map()`和`filter()`，现在返回迭代器而不是列表。在许多情况下，这会在你不知不觉中节省大量的内存。

## 工具

如果您决定将代码从 Python 2 移植到 Python 3，有一些现有的工具可以让您的生活更轻松。

*   [2to 3](https://docs.python.org/2/library/2to3.html)–官方自动化代码翻译工具。是的，它会为你移植代码！不能保证捕捉到所有内容，但是做了大量繁琐的语法修改。
*   caniusepython 3——一个漂亮的实用程序，用于检测哪些项目依赖关系阻碍了你的飞跃。
*   自动化并简化 Python 代码的测试。它允许您轻松地在多个版本的 Python 上测试您的代码，这对于任何项目来说都是非常棒的，但是当您在不同版本上测试新移植的代码库是否成功时，它尤其方便。

## 结论

升级到 Python 3 的理由数不胜数——不仅仅是因为新特性的便利性，还因为 Python 开发人员会定期修复语言中随机出现的模糊错误，仅在 Python 3 中。只有经过最严格测试的、永远不需要修改的代码库才有理由继续使用 Python 2。其他一切都应该享受 Python 开发人员为使这种语言成为今天的样子而付出的巨大努力。