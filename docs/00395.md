# 用装饰者让你的 Python 更漂亮

> 原文：<https://hackaday.com/2018/08/31/an-introduction-to-decorators-in-python/>

许多 python 爱好者熟悉使用 decorators，但是很少有人了解幕后发生了什么，并且能够自己编写。学习它们的微妙之处需要一点努力，但是一旦掌握了，它们就是编写简洁、优雅的 Python 的一个很好的工具。

这篇文章将简要介绍这个概念，从一个基本的装饰器实现开始，然后逐一介绍几个更复杂的例子。

# 什么是室内设计师

装饰器通常与`@decorator`语法一起使用。你可能见过类似这些例子的 Python。

```

@app.route(&quot;/home&quot;)
def home():
    return render_template(&quot;index.html&quot;)

@performance_analysis
def foo():
    pass

@property
def total_requests(self):
    return self._total_requests

```

为了理解 decorator 做什么，我们首先要后退一步，看看我们可以用 Python 中的函数做些什么。

```

def get_hello_function(punctuation):
    &quot;&quot;&quot;Returns a hello world function, with or without punctuation.&quot;&quot;&quot;

    def hello_world():
        print(&quot;hello world&quot;)

    def hello_world_punctuated():
        print(&quot;Hello, world!&quot;)

    if punctuation:
        return hello_world_punctuated
    else:
        return hello_world

if __name__ == '__main__':
    ready_to_call = get_hello_function(punctuation=True)

    ready_to_call()
    # &quot;Hello, world!&quot; is printed

```

在上面的代码片段中，`get_hello_function`返回一个函数。返回的函数被赋值，然后被调用。函数使用和操作方式的灵活性是 decorators 操作的关键。

除了返回函数，我们还可以将函数作为参数传递。在下面的例子中，我们**包装了**一个函数，在它被调用之前添加了一个延迟。

```

from time import sleep

def delayed_func(func):
    &quot;&quot;&quot;Return a wrapper which delays `func` by 10 seconds.&quot;&quot;&quot;
    def wrapper():
        print(&quot;Waiting for ten seconds...&quot;)
        sleep(10)
        # Call the function that was passed in
        func()

    return wrapper

def print_phrase(): 
    print(&quot;Fresh Hacks Every Day&quot;)

if __name__ == '__main__':
    delayed_print_function = delayed_func(print_phrase)
    delayed_print_function()

```

这一开始会让人感到有点困惑，但我们只是定义了一个新函数`wrapper`，它在调用`func`之前会休眠。值得注意的是，我们并没有改变`func`本身的行为，我们只是返回了一个不同的函数，它在延迟后调用`func`。

运行上面的代码时，会产生以下输出:

```

$ python decorator_test.py
Waiting for ten seconds...
Fresh Hacks Every Day

```

## 让我们把它变漂亮

如果你在网上翻找关于装饰者的信息，你会反复看到的短语是“句法糖”。这很好地解释了 decorators 是什么:简单地说，这是节省输入和提高可读性的捷径。

`@decorator`语法使得将我们的包装器应用于任何函数变得非常容易。我们可以像这样重写上面的延迟代码:

```

from time import sleep

def delayed_func(func):
    &quot;&quot;&quot;Return `func`, delayed by 10 seconds.&quot;&quot;&quot;
    def wrapper():
        print(&quot;Waiting for ten seconds...&quot;)
        sleep(10)
        # Call the function that was passed in
        func()

    return wrapper

@delayed_func
def print_phrase(): 
    print(&quot;Fresh Hacks Every Day&quot;)

if __name__ == '__main__':
    print_phrase()

```

用`@delayed_func`装饰`print_phrase`会自动进行包装，这意味着无论何时调用`print_phrase`，我们都会得到延迟的包装，而不是原来的函数；`print_phrase`已被`wrapper`取代。

# 这为什么有用？

装饰者不能改变一个函数，但是他们可以扩展它的行为，修改和验证输入和输出，以及实现任何其他外部逻辑。编写 decorators 的好处来自于一旦编写后的易用性。在上面的例子中，我们可以很容易地将`@delayed_func`添加到我们选择的任何函数中。

这种应用的简易性对于调试代码和程序代码都是有用的。decorators 最常见的应用之一是提供关于函数性能的调试信息。让我们编写一个简单的装饰器，它记录函数被调用的日期和运行时间。

```

import datetime
import time
from app_config import log

def log_performance(func):
    def wrapper():
        datetime_now = datetime.datetime.now()
        log.debug(f&quot;Function {func.__name__} being called at {datetime_now}&quot;)
        start_time = time.time()

        func()

        log.debug(f&quot;Took {time.time() - start_time} seconds&quot;)
    return wrapper

@log_performance
def calculate_squares():
    for i in range(10_000_000):
        i_squared = i**2

if __name__ == '__main__':
    calculate_squares()

```

在上面的代码中，我们在一个计算数字 0 到 10，000，000 的平方的函数上使用了我们的`log_performance`装饰器。以下是运行时的输出:

```

$ python decorator_test.py
Function calculate_squares being called at 2018-08-23 12:39:02.112904
Took 2.5019338130950928 seconds

```

# 处理参数

在上面的例子中，`calculate_squares`函数不需要任何参数，但是如果我们想让我们的`log_performance`装饰器与任何接受任何参数的函数一起工作呢？

解决方案很简单:允许`wrapper`接受参数，并将这些参数直接传递给`func`。为了允许任意数量的参数和关键字参数，我们使用了`*args, **kwargs`，将所有参数传递给包装的函数。

```

import datetime
import time
from app_config import log

def log_performance(func):
    def wrapper(*args, **kwargs):
        datetime_now = datetime.datetime.now()
        log.debug(f&quot;Function {func.__name__} being called at {datetime_now}&quot;)
        start_time = time.time()

        result = func(*args, **kwargs)

        log.debug(f&quot;Took {time.time() - start_time} seconds&quot;)
        return result
    return wrapper

@log_performance
def calculate_squares(n):
    &quot;&quot;&quot;Calculate the squares of the numbers 0 to n.&quot;&quot;&quot;
    for i in range(n):
        i_squared = i**2

if __name__ == '__main__':
    calculate_squares(10_000_000) # Python 3!

```

注意，我们还捕获了`func`调用的结果，并将其用作包装器的返回值。

# 确认

decorators 的另一个常见用例是验证函数参数和返回值。

这里有一个例子，我们正在处理以相同格式返回 IP 地址和端口的多个函数。

```

def get_server_addr():
    &quot;&quot;&quot;Return IP address and port of server.&quot;&quot;&quot;
    ...
    return ('192.168.1.0', 8080)

def get_proxy_addr():
    &quot;&quot;&quot;Return IP address and port of proxy.&quot;&quot;&quot;
    ...
    return ('127.0.0.1', 12253)

```

如果我们想在返回的端口上做一些基本的验证，我们可以像这样写一个装饰器:

```

PORTS_IN_USE = [1500, 1834, 7777]

def validate_port(func):
    def wrapper(*args, **kwargs):
        # Call `func` and store the result
        result = func(*args, **kwargs)
        ip_addr, port = result

        if port &lt; 1024:
            raise ValueError(&quot;Cannot use priviledged ports below 1024&quot;)
        elif port in PORTS_IN_USE:
            raise RuntimeError(f&quot;Port {port} is already in use&quot;)

        # If there were no errors, return the result
        return result
    return wrapper

```

现在很容易确保我们的端口得到验证，我们只需用`@validate_port`修饰任何适当的函数。

```

@validate_port
def get_server_addr():
    &quot;&quot;&quot;Return IP address and port of server.&quot;&quot;&quot;
    ...
    return ('192.168.1.0', 8080)

@validate_port
def get_proxy_addr():
    &quot;&quot;&quot;Return IP address and port of proxy.&quot;&quot;&quot;
    ...
    return ('127.0.0.1', 12253)

```

这种方法的优点是验证是在函数外部完成的——对内部函数逻辑或顺序的更改不会影响验证。

## 处理函数属性

假设我们现在想要访问上面的`get_server_addr`函数的一些元数据，比如名称和 docstring。

```

&gt;&gt;&gt; get_server_addr.__name__
'wrapper'
&gt;&gt;&gt; get_server_addr.__doc__
&gt;&gt;&gt;

```

灾难！因为我们的`validate_port`装饰器本质上是**用我们的包装器替换了**它所装饰的函数，所以所有的函数属性都是`wrapper`的，而不是原始函数的。

好在这个问题比较普遍，标准库中的`functools`模块有解决方法:`wraps`。让我们在我们的`validate_port`装饰器中使用它，现在看起来像这样:

```

from functools import wraps

def validate_port(func):
    @wraps(func)
    def wrapper(*args, **kwargs):
        # Call `func` and store the result
        result = func(*args, **kwargs)
        ip_addr, port = result

        if port &lt; 1024:
            raise ValueError(&quot;Cannot use priviledged ports below 1024&quot;)
        elif port in PORTS_IN_USE:
            raise RuntimeError(f&quot;Port {port} is already in use&quot;)

        # If there were no errors, return the result
        return result
    return wrapper

```

第 4 行表明`wrapper`应该保留`func`的元数据，这正是我们想要的。现在，当我们尝试访问元数据时，我们得到了我们想要的。

```

&gt;&gt;&gt; get_server_addr.__name__
'get_server_addr'
&gt;&gt;&gt; get_server_addr.__doc__
'Return IP address and port of server.'
&gt;&gt;&gt;

```

# 摘要

装饰器是让你的代码库更加灵活和易于维护的好方法。它们提供了一种对函数进行运行时验证的简单方法，对于调试也很方便。即使编写定制的装饰器不是你的事情，当理解第三方代码和利用已经编写好的装饰器时，理解是什么让它们起作用将是一个重要的资产。