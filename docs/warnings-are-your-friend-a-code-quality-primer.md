# 警告是你的朋友——代码质量入门

> 原文：<https://hackaday.com/2018/11/06/warnings-are-your-friend-a-code-quality-primer/>

如果有一件事是众所周知的，那就是用它搬起石头砸自己的脚。不可否认的是，C 提供的自由是有代价的，那就是我们有责任驯服和控制这种语言。从好的方面来看，由于这种语言的缺陷是众所周知的，我们有大量的工具可供选择，帮助我们消除最常见的问题和错误，这些问题和错误可能会在以后的道路上反噬我们。问题是，我们自己必须真正想要它，并积极倾听工具要说什么。

我们通常从安全的角度来看待这个问题，并关注可利用的漏洞，您可能不会将这些漏洞视为有效的威胁或您需要在项目中担心的事情。你可能是对的，并不是代码中的每个缺陷都会导致攻击者接管你的网络或烧毁你的房子，更可能的后果是更加平凡和无聊。但这并不意味着你不应该关心他们。

错误的、不可靠的软件是针对计算机的暴力的头号原因，无论你喜欢与否，人们都会根据你的代码质量来判断你。仅仅因为 Linus Torvalds 想要离开圣诞老人的淘气名单，并不意味着技术领域会突然变得不那么关键或失去敌意，在一个与世界分享你的工作从未如此容易的时代，可靠、高质量的代码将占上风，并使你从群众中脱颖而出。

公平地说，这是一个不同的故事，一些快速和肮脏的黑客，或在周末放在一起的一次性概念项目证明。在这些情况下，我们很容易逃脱更多的惩罚。但是，一旦我们走出最初的原型阶段，并着眼于更长期的、越来越复杂的开发，我们就不必担心语言或编程本身的基本的、容易预防的怪癖和陷阱。静态代码分析可以帮助我们找到并应对它们，同样，因为这是一个如此普遍的问题，不仅仅是在 C 语言中，我们有各种各样的工具可以使用。

然而，这里经常被忽略的一个工具是编译器本身，尤其是它的警告。记住开源，让我们看看如何利用`gcc`和`clang`来提高我们的代码质量，听听他们对我们代码的看法。

## 编译器警告

与编译器错误不同，编译器错误指示阻止编译器完全处理源代码的实际语言违规，警告指示我们的代码似乎不太对劲，即使它在语法上可能是正确的。编译器警告就像一个渴望给我们善意建议的好朋友。有时他们警告一个更深层次的问题，但有时他们是肤浅的。我们基本上有三个选项来处理警告:忽略它们，隐藏它们，或者就地修复实际问题。

根据本文的介绍，这看起来似乎与前两个选项无关，但事实并非如此。C 运行在从微型微控制器到大型服务器群的任何东西上，并不是每个警告都与我们的情况相关或适用，虽然关注正确的警告可以使我们免受痛苦，但其他人可能只是浪费我们的时间。

### 警告的编译器标志

默认情况下，编译器可能不会对警告说得太多，主要担心直接的代码问题，如被零除或可疑的指针转换。启用更多的警告选项取决于我们，我们将这些选项作为标志传递给编译器，`gcc`和`clang`都提供了一个很长的(并且大部分是兼容的)这样的标志列表。

为了启用给定的标志，我们通过`-Wflag`，为了禁用警告，我们通过`-Wno-flag`。如果我们对一个警告特别认真，`-Werror=flag`会把一个警告变成一个错误，迫使编译器中止它的工作。启用每一个可能的标志本身似乎是一项乏味的工作——的确如此。好消息是`gcc`和`clang`都提供了额外的元标志`-Wall`和`-Wextra`，它们组合了两组独立的通用警告标志。坏消息是，这些名字容易让人误解。`gcc -Wall`远没有启用*所有的*警告，甚至`gcc -Wall -Wextra`还遗漏了一部分。对于`clang`来说也是如此，但是它提供了一个额外的`-Weverything`标志来完全警告*的一切*，给了我们一个选择加入和选择退出的方法。

理论已经讲得够多了，是时候看看一些糟糕的代码了:

```

#include <stdio.h>

enum count {NONE, ONE, OTHER};

int main(int argc, char **argv)
{
    int ret;
    enum count count = argc - 1;    // [1] signedness silently changed*

    switch (count) {
        case NONE:
            printf("%s\n", argc);   // [2] integer printed as string
            ret = 1;
                                    // [3] missing break
        case ONE:
            printf(argv[1]);        // [4] format string is not a string literal
            ret = 2;
            break;
    }                               // [5] enum value OTHER not considered
                                    // [6] no default case

    return ret;                     // [7] possibly uninitialized value
}

```

除了风格和品味之外，根据您自己的定义和哲学，我们可以在这几行代码中解决大约七个问题，将一个`int`参数传递给一个`%s`格式可能是最明显的一个。让我们仔细看看。

其中一些问题在我们的特定情况下可能不会造成任何伤害，例如将有符号整数转换为无符号整数(`[1]`)，但在其他情况下可能会造成伤害。另一方面，当需要一个字符串时打印一个整数是未定义的行为，很可能以 segfault ( `[2]`)结束。缺少的`break`语句(`[3]`)将继续传递`argv[1]`到`printf()`，当它没有设置值时也是如此。回过头来看[指针对指针的排列](https://hackaday.com/2018/04/19/when-4-1-equals-8-an-advanced-take-on-pointers-in-c/)，`argv[argc]`是`NULL`，造成了这里另一个未定义的行为。接受未经组织的用户输入本身就是一个坏主意，将它传递给`printf()`为[格式字符串攻击](https://en.wikipedia.org/wiki/Uncontrolled_format_string) ( `[4]`)打开了大门。如果不处理每一个`enum`值(`[5]`)并且在`switch` ( `[6]`)中忽略一个默认情况，那么当我们有多个命令行参数(`[7]`)时，就会导致`ret`被未初始化地返回。

默认情况下，在 x86_64 上`clang` 7.0.0 会警告我们其中的三个(`[2]`、`[4]`和`[5]`)，而`gcc` 8.2.1 会在没有任何警告的情况下让我们愉快地通过。很明显，我们必须加强我们的警示旗游戏。让我们看看元标志`-Wall`、`-Wextra`和`clang`的`-Weverything`是如何处理的。注意`-Wextra`本身很少有意义，最好将其视为`-Wall`的补充。

![](img/86aa4ccf0f7a32c31d0d1060e36aa6cc.png)

这些是一些发人深省的结果。不幸的是，只有在编译 C++代码时，`clang`才不关心 C 中的隐式失败(即在`switch`中缺少`break`),并且它通常更喜欢完整的`enum`处理而不是默认情况。另一方面，对于`gcc`，很明显我们需要更仔细地研究一下[手册](https://gcc.gnu.org/onlinedocs/gcc/Warning-Options.html)。以下是我们获取几乎所有警告的方法:

```

$ gcc -Wall -Wextra -Wformat-security -Wswitch-default

```

好了，现在我们终于把警告印出来了，是时候再把它们去掉了。

## 修复您的警告

消除所有警告后，我们的`main()`函数可能如下所示:

```

int main(int argc, char **argv)
{
    int ret = -1;
    enum count count = (enum count) (argc - 1);

    switch (count) {
        case NONE:
            printf("%d\n", argc);
            ret = 1;
            break;
        case ONE:
            printf("%s\n", argv[1]);
            ret = 2;
            break;
        case OTHER:
            // do nothing
            break;
    }

    return ret;
}

```

不过要小心，将一个未检查的整数赋给`enum`通常不是最好的主意，当它是`argc`时更是如此。此外，在这个例子中，`switch`中缺少的`break`是一个真正的错误，但在其他情况下，您可能想要故意通过`case`失败。用一个`/* fall through */`注释(或类似的拼写变体)替换`break`会让`gcc`高兴——并且会提醒你和其他开发者这是故意的。

不过，有时候消除警告有点棘手。以下面这个涉及到[函数指针](https://hackaday.com/2018/05/02/directly-executing-chunks-of-memory-function-pointers-in-c/)的例子为例:

```

// callback function pointer
void (*some_callback)(int, void *);

// callback implementation
void dummy_callback(int i, void *ptr)
{
    // do something with i but not with ptr
}

```

有了`-Wall -Wextra`，编译器会抱怨`ptr`参数没用。但是，如果您根本不需要它，而回调声明却坚持要拥有它，该怎么办呢？嗯，您可以将参数转换为`void`，或者深入编译器属性的世界。这是其中任何一个的样子:

```

void dummy_callback(int i, void *ptr)
{
    (void) ptr;
    // do something with i but not with ptr
}

void dummy_callback(int i, void *ptr __attribute__((unused)))
{
    // do something with i but not with ptr
}

```

选择哪个由你自己决定，编译器每次都会生成相同的代码。但是现在让我们坚持属性。

## 编译器属性

我们刚刚看到，我们可以使用特殊的编译器属性来单独抑制警告，而不会完全禁用它们。冒着听起来优柔寡断的风险，我们也可以使用属性从编译器获得新的警告。是的，我们刚刚摆脱他们，所以我们为什么想要得到新的？简单:一旦我们建立了警告文化，我们就可以用它来通知其他开发人员(包括我们未来的自己)我们希望如何处理某些函数或数据。

假设我们为一个更大的软件项目编写一个模块，其中一个特定的函数返回值决定整个模块的命运。我们希望确保无论是谁调用这个函数，都不会忽略这个值。使用`__attribute__((warn_unused_result))`，我们可以让编译器成为信使。

```

int specific_function(void) __attribute__((warn_unused_result));

...

specific_function(); // compiler warns about unused return value
(void) specific_function(); // nice try, still a warning though
int ret = specific_function(); // now we're good

```

以类似的方式，我们可以使用两个属性来控制我们的指针，尤其是当涉及到可能的`NULL`指针时，并且生成更多的警告。

```

// declare that the first parameter mustn't be NULL
void some_function(char *, int) __attribute__((nonnull(1)));

// declare that return value can't be NULL
char *another_function(void) __attribute__((returns_nonnull));

```

虽然这允许一些编译器优化，但它也为开发人员定义了一个契约:`NULL`不是该参数的有效选项，您不必担心`NULL`被返回。

```

some_function(NULL, 0xff); // warning that parameter is NULL

if (another_function() == NULL) {
    // warning that check is always false
}

```

同时，如果我们真的在`another_function()`中返回了`NULL`，我们也会得到一个警告。并不是说我们真的可以用它来执行任何事情，最终他们只是没有任何后果的警告。

## 添加后果

如果你真的很重视警告，你可以决定用`-Werror`标志把它们都变成错误。不过，你可能需要重新考虑一下，并不是每一个警告都是致命的，需要立即处理。有时候你只是想把你的想法从脑子里拿出来放到编辑器里，看看结果如何，把清理工作留到以后。一个有用的方法是分离您的构建环境，在开发过程中留下警告，但是一旦您构建了一个发布或者合并到 master，就要收紧规则。

是否真的必须是`-Werror`由您决定，也可以选择只将个别警告变成错误。假设我们想要严格控制我们的`NULL`相关属性:`-Wnonnull`将启用警告，`-Werror=nonnull`将启用警告并将它们视为错误。注意，`-Werror=flag`隐式地设置了`-Wflag`，所以我们不需要担心警告是否会被启用，只要我们把它们变成错误，它们就会出现。

## 从这里去哪里

不幸的是，在我们最后的例子中有一些缺点。虽然编译器会检测上面演示的`NULL`场景，但它们很容易被绕过，不管是有意还是无意:

```

    int ret = specific_function();
    // return check ends here
    // whether you actually use its value doesn't matter

    char *ptr = NULL;
    some_function(ptr, 0xff); // only explicit NULL parameters raise warnings

    ptr = another_function();
    if (ptr == NULL) { // no more warning that it will always be false
        ...
    }

```

这是否让倾听警告变得毫无意义？绝对不是，如果我们积极地消除它们，我们几乎总能得到更好的代码。然而，也不要让没有警告给你一种错误的安全感。编译器警告是我们的第一道防线，它们可以帮助我们提高代码质量，但它们不是灵丹妙药。让您的代码稳定可靠需要多种工具。但是话说回来，我们有更多的 C 语言可用，下一次我们将使用`lint`和它的朋友来看看更多的静态代码分析。