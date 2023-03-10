# C 的异步例程

> 原文：<https://hackaday.com/2019/09/24/asynchronous-routines-for-c/>

[Sandro Magi]注意到异步/等待习语最近在编程中变得更加普遍。据他说，他第一次遇到它是在 C#中，但是在 JavaScript 和 Rust 中也发现了这样的例子。这个想法很简单:允许一个函数返回，但是稍后再返回来完成一些需要很长时间的事情。当然，多线程是解决这个问题的一种方法，但是一般来说，这种技术意味着更多的协程设置，其中函数在某种程度上协作以获得良好的行为。[Sandro]从现有的 protothread 库中获得了一些想法，并使用它来创建一个系统，以便在 C 和 C++中获得这种效果。

添加这个“库”就像包含一个头文件一样简单。所有的魔法都发生在预处理器和编译器上。没有要链接的代码。异步例程只需要两个字节的开销，不像正常的线程，不需要预分配的私有堆栈。

这里有一个来自该项目的 GitHub 的简单例子:

```

#include "async.h"

typedef struct { 
    async_state;    // declare the asynchronous state
    timer timer;    // declare local state
} example_state;
example_state pt;

async example(example_state *pt) {
    async_begin(pt);

    while(1) {
        if(initiate_io()) {
            timer_start(&timer);
            await(io_completed() || timer_expired(&timer));
            read_data();
        }
    }
    async_end;
}

```

当然，`initiate_io`、`timer_start`、`timer_expired`、`read_data`、`io_completed`是在别的地方定义的。这个想法很简单。第一次调用 async 函数时，它会像平常一样运行，直到遇到某种形式的 await。那么它可能会回来。之后的每一次，函数都跳回 await 语句。当然，您可以拥有多个 await 语句。

在本例中，一旦 I/O 开始，代码将一直返回，直到 I/O 完成或定时器到期。然后它会返回一个最终答案。

这里的神奇之处在于 switch 语句(还有一个限制:不能在异步代码中使用 switch 语句)。该函数返回下一次要跳转的行号，或者返回-1 以结束循环。每个 await 生成一个具有当前行号的 case 标签。如果将-E 传递给 gcc 编译器，并查看预处理后的输出，就很容易看出这一点:

```

async example(struct async *pt) {
    switch((pt)->_async_kcont) { case 0:;

    while(1) {
        if(initiate_io()) {
            timer_start(&xtimer);
            case 21: if (!(io_completed() || timer_expired(&xtimer))) return 21;
            read_data();
        }
    }
    default: return ASYNC_DONE; };

```

当然，您可以自己滚动，但这是一个方便的语法快捷方式。在之前，我们已经在[小型系统上看到过](https://hackaday.com/2016/01/10/pic32-smart-watch-2/)[原线程](http://dunkels.com/adam/pt/index.html)的使用。Protothreads 甚至为一名黑客[赢得了一份工作](https://hackaday.com/2019/03/22/hacker-abroad-visiting-espressif-and-surprising-subway-ads/)。