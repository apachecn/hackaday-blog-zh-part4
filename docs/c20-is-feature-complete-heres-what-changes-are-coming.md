# C++20 是功能完整的；下面是即将到来的变化

> 原文：<https://hackaday.com/2019/07/30/c20-is-feature-complete-heres-what-changes-are-coming/>

如果你对 C++有什么看法，你可能要么因为它的广泛性和多功能性而喜欢它，要么因为它过于复杂而讨厌它，宁愿坚持使用两种语言。不管怎样，这是你对这门语言形成新观点的机会。C++标准委员会最近聚集在一起，致力于语言标准的最新修订版 C++20 的定稿工作，决定 C++下一个主要版本的所有新特性。

继 C++17 之后，这将是 C++标准的第六个修订版，这种语言已经从它的“成为 C 的超集”时代走了很长的路。坦白地说，说到喜欢或讨厌这门语言，我还没有完全下定决心。我最大的问题是“用 C++编程”现在可能意味着太多不同的事情，从琐碎的“带类的 C”风格到编写使 Perl 看起来像散文的代码。这些年来，C++已经成为一种功能丰富、势不可挡的语言，随着 C++20 的加入，事情不会变得更容易。虽然，他们也不会变得更难。嗯，至少不一定。我猜？这很复杂，但这就是这门语言的本质。

总之，[新特性的清单](https://en.wikipedia.org/wiki/C%2B%2B20)很长，结合所有的规范提案甚至更长，每一个新特性都可以填充它自己完整的文章。但是为了大致了解 C++明年会有什么变化，让我们来看一下 C++20 中等待我们的一些主要的新特性、变化和增加。从更好的类型检查和编译器错误消息到类似 Python 的字符串处理，以及取代`#include`系统的计划，这里有很多东西在发挥作用！

## 让事情更安全

作为一种语言，对实现细节的更自由和更少的限制为开发人员提供了很大的灵活性——同时也带来了许多误解的可能性，这些误解注定会在将来的某个地方导致错误。直到今天，它仍然是 C 的最大资产和弱点，C++在根源上仍然有足够多的相似之处。在这方面，限制肯定会有所帮助，但增加限制往往是不受欢迎的选择。好的一面是，C++在适当的地方做出了妥协，在语言层面留下了灵活性，并由开发人员自行决定增加了限制。

### 编译器建议:显式常数

早在 C++11 中， [`constexpr`](https://en.cppreference.com/w/cpp/language/constexpr) 关键字是作为常规`const`声明的附加项引入的，它定义了一个可以在编译时计算的[常量表达式](https://en.cppreference.com/w/cpp/language/constant_expression)。这为编译器提供了大量的优化机会，但也使得它可以声明，例如，一个函数将返回一个常量值。这有助于更清楚地展示一个函数的意图，避免将来一些潜在的麻烦。举以下例子:

```

int foo() {
    return 123;
}

constexpr int bar() {
    return 123;
}

const int first = foo();
const int second = bar();

```

虽然这两个函数在技术上没有什么区别，并且都将返回一个常量值，该常量值将有效地分配给一个`const`变量，`bar()`将清楚地表明这一事实。在`foo()`的例子中，这实际上更像是一个巧合的副作用，没有完整的上下文，函数的返回值应该是一个常量并不明显。使用`constexpr`消除了这里的任何疑问，避免了可能的意外副作用，从长远来看会使代码更加稳定。

已经有一段时间了，`constexpr`已经经历了几年的改进，C++20 将会带来更多的改进，特别是在消除以前存在的使用限制方面。大多数新标准允许 [`virtual constexpr`函数](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2018/p1064r0.html)，开发者可以在`constexpr` 内部使用[/`catch`(前提是内部没有抛出异常)，并且](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2018/p1002r0.pdf)[可以在`union`](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2018/p1330r0.pdf) 内部改变成员。

最重要的是，[`std::string`](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2018/p0980r0.pdf)[`std::vector`](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2018/p1004r1.pdf)以及[其他一堆以前在标准库中缺失的地方](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2018/p1032r1.html)都将充分利用`constexpr`。哦，如果你想检查一段代码是否在常量求值中实际执行，你可以使用 [`std::is_constant_evaluated()`](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2018/p0595r2.html) 来完成，它会相应地返回一个布尔值。

注意，`constexpr`代码声明它*可以*在编译时被计算，因此是一个有效的常量表达式，但它不一定必须这样，也不保证计算会在编译时发生，而是可以推迟到运行时。这主要与编译器优化有关，不会影响程序的行为，但也表明`constexpr`主要是一个意图标记。

```

constexpr int foo(int factor) {
    return 123 * factor;
}

const int const_factor = 10;
int non_const_factor = 20;

const int first = foo(const_factor);
const int second = foo(non_const_factor);

```

这里，`first`将在编译时被求值，因为所有涉及的表达式和值都是常数，因此在编译时是已知的，而`second`将在运行时被求值，因为`non_const_factor`本身不是常数。尽管`foo()`仍将返回一个常量值，但这并不能改变事实，编译器只是还不能确定具体是哪个值。为了确保编译器*将*知道该值，C++20 引入了 [`consteval`](https://en.cppreference.com/w/cpp/language/consteval) 关键字，将一个函数声明为 [*立即函数*](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2018/p1073r3.html) 。将`foo()`声明为`consteval`而不是`constexpr`现在确实会导致错误。事实上，即时函数在编译时实际上只有*和*是已知的，因此这就把`consteval`函数变成了宏函数的替代函数。

在常量表达式验证严格性的另一端是新的 [`constinit`](https://gist.github.com/EricWF/128781c188b1a4fca7581e7ea943d58b) 关键字，它主要告诉编译器一个对象将用一个常量值静态初始化。如果你熟悉 [*静态初始化顺序惨败*](https://isocpp.org/wiki/faq/ctors#static-init-order) ，这是一个解决问题的尝试。

但是常量表达式并不是 C++20 唯一的旨在提高编译时验证和稳定性的变化。

### 概念的概念

虽然从技术上来说并不是一个全新的事物，但是*概念*已经从[的一个实验性特征](https://en.cppreference.com/w/cpp/experimental/constraints)发展成为[语言标准](https://en.cppreference.com/w/cpp/language/constraints)的一个成熟部分，允许向模板添加语义约束，并最终使泛型编程变得更加具体。

与[类型特征](https://en.cppreference.com/w/cpp/header/type_traits)有点关系，概念确保模板中使用的数据满足一组特定的标准，并在编译过程的开始验证这一点。举个例子，不是检查对象`is_integral`，而是使用类型`Integral`的对象。因此，如果某个概念的定义要求没有得到满足，编译器可以提供一个简短而有意义的错误消息，而不是从模板代码本身的某个深处倾倒错误和警告，如果不深入研究该代码，这些错误和警告将没有多大意义。

除了让编译器知道需要什么数据之外，它还向其他开发人员清楚地显示了需要什么数据，这有助于首先避免错误消息，并避免以后导致错误的误解。另一方面，概念也可以用来约束模板函数的返回类型，将变量限制为一个概念而不是一个通用的`auto`类型，后者可以被认为是 C++的`void *`返回类型。

一些基本概念将在标准库中提供[，如果您不想等待更新的编译器，GCC 从版本 6 开始就实现了实验概念，您可以使用`-fconcepts`命令行参数启用它们。请注意，在最初的草案和当前的参考文件中，概念名称是使用`CamelCase`、](https://en.cppreference.com/w/cpp/header/concepts)[定义的，但它们将被更改为`snake_case`、](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2019/p1754r0.pdf)以保持与所有其他标准标识符的一致性。

### 范围是新的迭代器

范围本质上是覆盖集合中一系列值的迭代器，例如列表或向量，但不是不断拖动迭代器的开始和结束，范围只是在内部保存它们。

就像概念一样，在 C++20 中，范围也已经从实验状态转移到了[语言标准](https://en.cppreference.com/w/cpp/ranges)，这并不是巧合，因为范围依赖于概念，并使用它们来改进旧的迭代器处理，使之有可能向处理的值添加约束，具有相同的好处。在约束值类型之上，范围引入了*视图*作为范围的一种特殊形式，它允许对一个范围进行数据操作或过滤，返回初始范围数据的修改版本作为另一个范围。这允许它们被链接在一起。假设您有一个整数向量，并且您想要检索平方形式的所有偶数值——范围和视图可以帮助您实现这一目标。

有了所有这些改变，编译器将对类型检查有更大的帮助，并且会给出更多有用的错误信息。

## 字符串格式

说到错误信息，或者说一般的输出，根据作者的提议 [`libfmt`库](https://github.com/fmtlib/fmt)将被集成到语言标准中，命名为`std::format`。本质上，这提供了 Python 的字符串格式化功能！相比于`cout`移位业务的笨拙，以及在 C++环境中使用`printf()`感觉有点不对劲的事实，这绝对是一个受欢迎的增加。

虽然 Python 风格的格式化提供了与`printf()`几乎相同的功能，只是格式字符串语法不同，但它消除了一些冗余，并提供了一些有用的附加功能，如二进制整数表示，以及带或不带填充字符的居中输出。然而，最大的优势是可以为自定义类型定义格式规则，表面上看这就像 Python 的`__str__()`或 Java 的`toString()`方法，但它也增加了自定义格式类型。

以`strftime()`为例——尽管这是一个 C 函数，其行为类似于`snprintf()`,区别在于它为其格式字符串定义了自定义的、特定于时间的转换字符，并期望`struct tm`作为参数。有了正确的实现，`std::format`可以扩展成那样，事实上这就是[即将对](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2019/p1361r1.pdf) [`std::chrono`库](https://en.cppreference.com/w/cpp/chrono)添加的将要做的。

### 源位置

当我们谈到如何以方便的方式进行格式化时，[c++ 20](https://en.cppreference.com/w/cpp/experimental/source_location)的另一个实验性特性是 [`source_location`](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2019/p1208r5.pdf) 功能，它提供了从当前调用上下文中方便地访问文件名、行号或函数名的功能。与`std::format`相结合，它是实现定制日志功能的主要候选，实际上是像`__FILE__`和`__LINE__`这样的预处理宏的现代替代物。

## 模块

看来慢慢消除预处理器的使用是 C++未来的一个长期目标，`consteval`本质上取代了宏函数，`source_location`淘汰了最常用的宏之一，最重要的是:[模块](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2019/p1103r3.pdf)，一种分割源代码的新方法，旨在最终取代整个`#include`系统。

虽然有些人说它早就应该出现了，但其他人认为在这一点上添加模块相当关键，一些开发人员[已经表达了他们对当前状态的担忧](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2019/p1427r0.pdf)。不管你对这个问题的看法如何，可以肯定地说，这是对这门语言整体本质的重大改变，但同时也是一项足够复杂的任务，不会在一夜之间完成。时间会告诉我们模块的最终结果。如果你很好奇并且已经想看一看，那么 [GCC](https://gcc.gnu.org/wiki/cxx-modules) 和 [Clang](https://clang.llvm.org/docs/Modules.html) 在某种程度上都已经有了模块支持。

但是等等，还有更多！

## 其他一切

这个列表还在继续，随着[协程](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2018/n4723.pdf)成为 C++20 将会添加的[的又一个主要特性。](https://en.cppreference.com/w/cpp/language/coroutines)

至于其他的，会有的

*   新的[同步库](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2019/p1135r5.html)
*   [可协同中断的加入中断](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0660r0.pdf)
*   [*飞船操作员* `<=>`](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2019/p1614r1.html) 进行三方比较
*   [`using enum`](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2019/p1099r4.html) 去掉一些名称空间分离的杂音
*   对 lambda 表达式的一系列补充
*   有些[部分贬低了`volatile`的](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2019/p1152r3.html)

不过不要担心，真正重要的部分不会改变。

所以总而言之，C++有很多新特性，有些特性肯定值得兴奋。

当然，这些新特性和扩展中的一些在其他语言中已经存在很长时间了，甚至不是从一开始就存在。有趣的是，看看这些曾经受 C++影响的语言现在是如何影响 C++本身的未来的。