# 创造黑洞:实践中被零除

> 原文：<https://hackaday.com/2018/11/21/creating-black-holes-division-by-zero-in-practice/>

除以零——算术的基本禁忌。它有点神秘，是互联网幽默的持续来源，无论是涉及爆炸的微控制器，宇宙的崩溃，还是通过让 Siri 告诉你你没有朋友来摧毁你自己的世界。

这也是为数不多的默认情况下`gcc`会警告你的事情之一，当我最近写关于编译器警告的文章时，这引起了一场相当生动的讨论，并带来了有趣的见解。如果你正在运行一个现代的操作系统，它甚至会给你一个信号，告诉你有什么地方出错了，让你用代码来处理。除以零不仅仅是理论上的，也是对信号的一个很好的介绍，所以让我们仔细看看。

很有可能，你第一次听说除法本身是在小学的时候，学校告诉你被零除是严格禁止的——很明显你不想让你的老师叫警察来抓你，所以你服从并避免这样做。但是就像生活中的许多其他事情一样，随着年龄的增长，它们变得越来越不受限制，被零除最终从禁止变成了不可能，并产生了一个不确定的结果。

的确，如果 *a* = b/0，这将反过来意味着 *a* ×0 = *b* 。如果 *b* 本身是零，那么这个等式对每一个数字都是正确的，这使得不可能为 *a* 定义一个具体的值。如果 *b* 是任何其他值，没有一个值乘以零会产生任何非零值。一旦我们进入微积分的领域，我们将会知道无穷似乎是答案，但那最终只是用另一个抽象的、令人难以置信的概念代替了一个。它也不能回答一个问题:所有这些在处理器中是如何实现的？

## 浮点除以零

让我们从浮点数开始。如今，它们通常使用 [IEEE 754 格式](https://en.wikipedia.org/wiki/IEEE_754)来表示和存储在内存中，将值本身分成符号、指数和分数的单独字段。如果我们在内存中查看一个 [`float`](https://en.wikipedia.org/wiki/Single-precision_floating-point_format) 或 [`double`](https://en.wikipedia.org/wiki/Double-precision_floating-point_format) ，它不会有太大的意义，因为它的实际值是由这三个独立的字段构造的。为了演示这一点，我们可以将一个`float`转换成一个`int`并打印出来。注意，我们必须通过指针转换来实现，否则我们只能得到浮点数的整数部分。

```

float fval = 12.34f;
int *iptr  = (int *) &fval;
printf("%f -> 0x%08x\n", fval, *iptr);
// output: 12.340000 -> 0x414570a4

```

无论是`0x414570a4`还是`1095069860`都不会给我们任何暗示，这是`12.34`的号码。然而，这种表示形式为一些特殊情况留下了空间，如无穷大和*不是一个数字*，零除以零将得到的结果，因为该方程没有唯一的答案，因此不能用常规数字表示。这意味着我们可以继续前进，除以零，我们想要的，IEEE 754 格式已经涵盖了我们。

```

fval = 1 / 0.0f;
printf("%f -> 0x%08x\n", fval, *iptr);
// output: inf -> 0x7f800000

fval = 0 / 0.0f;
printf("%f -> 0x%08x\n", fval, *iptr);
// output: -nan -> 0xffc00000

```

换句话说，浮点数有内置的机制来处理被零除的情况，而不会造成严重破坏。并不是说它真的有帮助，我们不能用`inf`或`nan`做太多事情，并且关于无穷大的算术运算要么保持无穷大(可能改变了符号)，要么变成`nan`，这是一个死胡同。任何算术运算都不能再把`nan`变成其他任何东西。

## 整数被零除

如果您自己尝试了前面的例子，您可能会注意到，在所有关于编译器警告的讨论把我们带到这里之后，您没有看到一个警告。由于浮点数有自己明确定义的方法来处理被零除的情况，所以它不会造成编译器必须警告的威胁。如果我们有合适的 FPU，或者有足够的资源在软件中模拟浮点运算，这一切都很好。然而，如果我们处理整数，我们有一个主要的问题:无穷大的概念不存在于我们有限的可用值范围内。即使我们最终得到了一个有大量比特的数据类型，我们也只能表示一个非常非常大的数字，但永远不会是无穷大。这一次，编译器*将*警告一个明显的被零除的尝试。

```

// zerodiv.c
int main(void) {
    int i = 10/0;
    return 0;
}

```

```

$ gcc -o zerodiv zerodiv.c
zerodiv.c: In function ‘main’:
zerodiv.c:3:15: warning: division by zero [-Wdiv-by-zero]
     int i = 10/0;
               ^
$

```

如果我们继续做下去会发生什么？毕竟，这只是一个警告，我们从编译器那里得到了一个功能性的可执行文件，没有什么能阻止我们运行它。好吧，让我们来看看在 x86_64 上发生了什么:

```

$ ./zerodiv
Floating point exception (core dumped)
$

```

我们开始了，因为我们不能以任何方式表示结果，程序就崩溃了。但是是什么导致了那次事故呢？

在更复杂的处理器中，指令集提供专用的除法操作码，并且除法本身是在硬件中执行的。这允许处理器在执行操作本身之前检测到一个零因子，从而导致硬件异常。在我们的例子中，操作系统捕捉到了异常，并发出了浮点异常信号`SIGFPE`——不要介意这个有点误导的名字。就像浮点数一样，硬件除法指令有办法避免实际上被零除。但是，如果处理器没有这样的专用硬件，比如 8 位 AVR 或 ARM Cortex-M0，会怎么样呢？毕竟，除法并不是一个特别新的概念，只有现代处理器技术才使它成为可能。

如果你回想你的学生时代，纸笔除法主要是循环中移位、比较和减法的结合。这些都是最简单的处理器中可用的基本指令，这使得它们可以用一系列其他指令来代替除法。如果你好奇的话，AN0964 描述了 AVR 的概念。虽然也有更复杂的方法，但在某些情况下，除法指令在幕后没有任何不同，它只是有专用的硬件来将其包装在单个操作码中。

然而，对于处理器来说，无法判断特定的一系列常规操作实际上是在执行除法，这需要留意除数是否不为零。我们必须在分开之前自己手动检查。如果我们不这样做，它就会永远快乐地循环和比较([或 1267+年](https://www.youtube.com/watch?v=BT7dxgs0gjo))，直到它找到一个满足不可能的数字，也就是说，它只是陷入了一个无限循环。机械计算器是展示这一点的伟大设备。

虽然这将使宇宙保持完整，但它本质上使你的程序没有响应，就像任何其他无限循环一样，这显然是不好的，因为它最有可能处理其他事情。因此，如果您在没有硬件除法器的架构上执行除法或模运算，并且除数不是来自保证它不为零的预定义集合，请确保您事先检查该值。事实上，即使有合适的硬件支持，这也可能是个好主意。即时崩溃可能比可能未被发现的无限循环要好，但无论哪种方式，您的代码都不会做它应该做的事情。

## 回到 SIGFPE

接收硬件异常的一个不同之处是，我们可以对它采取行动，硬件异常要么变成中断，要么变成类似`SIGFPE`的信号。不要太深入细节:[信号](https://en.wikipedia.org/wiki/Signal_(IPC))是一种通知我们正在运行的程序某个特定事件已经发生的方式——分段错误(`SIGSEGV`)、程序终止(`SIGTERM`和更激烈的`SIGKILL`)，或者之前遇到的浮点异常`SIGFPE`，等等。我们可以在代码中捕捉大部分这些信号，并根据需要采取行动。比如我们抓到`SIGINT`，可以在 CTRL+C 按下的时候优雅的关机，或者干脆忽略。

这意味着，我们可以捕捉一个零发生的除法，例如保存我们当前的程序状态，或者写一些日志文件条目，让我们重现我们最初是如何到达这里的，这可能有助于我们避免将来出现这种情况。那么，是时候写一个信号处理器了。请注意，代码略有简化，`sigaction`手册页是关于掩码和错误处理的更多信息的好来源。

```

// zerodiv.c
#include <stdio.h>
#include <signal.h>

// SIGFPE callback function
void sigfpe_handler(int sig, siginfo_t *si, void *arg) {
    // print some info and see if it was division by zero that got us here
    printf("SIGFPE received at %p due to %s\n", si->si_addr,
            ((si->si_code == FPE_INTDIV) ? "div by zero" : "other reasons"));
    // do whatever should be done
}

int main(void) {
    int i = 123;
    struct sigaction sa;

    // set sigfpe_handler() as our handler function
    sa.sa_sigaction = sigfpe_handler;
    // make sure we get the siginfo_t content and reset the original handler
    sa.sa_flags = SA_SIGINFO | SA_RESETHAND;

    // set up the signal handling for SIGFPE
    sigaction(SIGFPE, &sa, NULL);

    printf("before: %d\n", i);
    i /= 0; // doing the nasty
    printf("after:  %d\n", i);

    return 0;
}

```

如果我们编译并运行它，我们可以预期除以零的警告，然后得到如下输出:

```

$ ./zerodiv
before: 123
SIGFPE received at 0x55f2c333b208 due to div by zero
Floating point exception (core dumped)
$

```

由于我们添加了`SA_RESETHAND`标志，程序仍然会因最初的异常而终止。如果我们省略了这个标志，它就不会，但这并不意味着我们已经成功地解决了这个问题。在 x86_64 上，信号处理程序只是在一个无限循环中结束，一遍又一遍地打印消息。我们必须通过调用信号处理程序中的`exit(int)`来显式终止该进程。

另一方面，ARM Cortex-A53 处理器(你可以在 Raspberry Pi 上找到的那个)似乎会在处理后自动重置异常标志，因此程序会在从信号处理器返回后继续运行，显示`after: 0`。这表明除以零被定义为结果为零。我没有成功重置 x86_64 上的标志，因此出现了无限循环，但这并不一定意味着这是不可能的，我只是无法自己实现它。然而，在 x86_64 上我们还可以做另外一件事:跳过除法。

### 跳过除法

注意信号处理器回调中的第三个`void *arg`参数？它将包含接收信号时的上下文，这使我们能够访问保存的寄存器，包括指令指针，当我们离开信号处理程序时，它将被恢复。如果我们反汇编我们的代码，我们会看到，在这个特定的例子中，我们的部分是一个 2 字节的指令:

```

$ objdump -d ./zerodiv |grep -2 div
    125b:       b9 00 00 00 00          mov    $0x0,%ecx
    1260:       99                      cltd   
    1261:   --> f7 f9                   idiv   %ecx
    1263:       89 85 5c ff ff ff       mov    %eax,-0xa4(%rbp)
    1269:       8b 85 5c ff ff ff       mov    -0xa4(%rbp),%eax
$

```

如果我们将指令指针寄存器`RIP`(或 32 位 x86 上的`EIP`)增加两个字节，当我们从信号处理程序返回时，将继续执行`idiv`之后的`mov`指令。这种寄存器调整听起来是一个非常糟糕的主意，所以你可能不应该这样做:

```

#include <stdio.h>
#define __USE_GNU // this and the file order is important to succeed
#include <ucontext.h>
#include <signal.h>

// adjusted signal handler
void sigfpe_handler(int sig, siginfo_t *si, void *arg) {
    // cast arg to context struct pointer holding the registers
    ucontext_t *ctx = arg;
    // print some info
    printf("SIGFPE received at %p\n", si->si_addr);
    // add 2 bytes to the instruction pointer register
    ctx->uc_mcontext.gregs[REG_RIP] += 2;
}

// main() remained as it was

```

```

$ ./zerodiv 
before: 123
SIGFPE received at 0x555c1ef5b243
after:  123
$

```

tadaa——这个部门被跳过了，这个项目幸存了下来。价值本身与试图分割之前保持不变。显然，任何依赖该部门结果的后续操作很可能是无用的和/或具有未知的后果。之前的树莓 Pi 也是同样的情况，结果是零。仅仅因为一个随机的结果被定义为一个未定义的情况，并不意味着潜在的数学问题被解决了，一切都变得有意义了。快速果断的失败往往是更好的选择。

所以我们有它。除以零时，你不会产生黑洞，但你也不会从中获得多少有用的东西。