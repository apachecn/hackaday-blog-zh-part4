# 需要一门新的编程语言？试试 Zig

> 原文：<https://hackaday.com/2021/10/05/need-a-new-programming-language-try-zig/>

也许你听说过，也许没有。Zig 是一种新的编程语言,似乎越来越受欢迎。让我们快速探究一下它是什么，为什么它是独一无二的，以及你会用它做什么样的事情。(编者注:除了“[为了大义](https://www.youtube.com/watch?v=jQE66WA2s-A)”，自然。)

## 这是什么？

你可能听说过 [Rust，因为它已经在关键的底层基础设施](https://hackaday.com/2020/07/15/will-2020-be-the-year-of-rust-in-the-linux-kernel/)中取得了重大进展，如操作系统和嵌入式微控制器。作为一个过于简化的例子，它提供了内存安全和许多传统的运行时检查，并被推到了编译时。它是 Hackaday 上许多帖子的宠儿，因为它提供了一些独特的优势。随着 Rust 的崛起，可能会有一些新玩家的空间是有道理的。像 [Julia](https://julialang.org/) 、 [Go](https://golang.org/) 、 [Swift](https://developer.apple.com/swift/) ，甚至[球拍](https://racket-lang.org/)这样的语言都是相对较新的语言，争夺[各地软件工程师高度觊觎的份额](https://githut.info/)。

所以我们来谈谈齐格。从广义上来说，Zig 确实试图用 c 语言的简单性和易用性来提供 Rust 的一些安全性。

*   没有隐藏的控制流
*   没有隐藏的内存分配
*   没有预处理器，没有宏
*   对可选标准库的一流支持
*   通过设计实现互操作
*   可调运行时安全性
*   编译时代码执行

特别是最后一个，可能是最有趣的，但我们会回来。让我们看一些代码，但是跳过 hello world，直接打开一个文件。下面是 C++代码:

```
#include <iostream>
#include <fstream>
#include <string>

using namespace std;
int main (int argc, char const *argv[]) {
  ifstream file("nonexistingfile.txt");

  char buffer[1024];
  file.read(buffer, sizeof(buffer));

  cout << buffer << endl;

  file.close();
  return 0;
}

```

现在让我们看看一些类似的 Zig 代码:

```
const std = @import("std");

using namespace std.fs;

pub fn main() !void {
    const stdout = std.io.getStdOut().writer();

    const file = try cwd().openFile(
        "nonexistingfile.txt",
        .{ .read = true },
    );
    defer file.close();

    var buffer: [1024]u8 = undefined;
    const size = try file.readAll(buffer[0..]);

    try stdout.writeAll(buffer[0..size]);
}

```

(感谢 Erik Engheim 提供的 C++和 Zig [示例代码](https://erik-engheim.medium.com/software-reliability-c-vs-zig-dbb2d0005b9c)。)

正如您可能已经从文件名中猜到的那样，该文件并不存在。C++代码不显式检查任何错误，在这种情况下，它是完全有效的代码，没有显示任何失败的迹象。Zig，另一方面，我们必须尝试，因为该文件可能会失败。当它失败时，您会得到一个很好的堆栈跟踪:

```
error: FileNotFound
/usr/local/Cellar/zig/0.7.0/lib/zig/std/os.zig:1196:23: 0x10b3ba52e in std.os.openatZ (fileopen)
            ENOENT => return error.FileNotFound,
                      ^
/usr/local/Cellar/zig/0.7.0/lib/zig/std/fs.zig:754:13: 0x10b3b857e in std.fs.Dir.openFileZ (fileopen)
            try os.openatZ(self.fd, sub_path, os_flags, 0);
            ^
/usr/local/Cellar/zig/0.7.0/lib/zig/std/fs.zig:687:9: 0x10b3b6c4b in std.fs.Dir.openFile (fileopen)
        return self.openFileZ(&path_c, flags);
        ^
~/Development/Zig/fileopen.zig:8:18: 0x10b3b6810 in main (fileopen)
    const file = try cwd().openFile(

```

移除 try 会导致编译错误。这里的回溯尤其令人印象深刻，因为这是一种相对简单的语言，没有垃圾收集器、运行时或虚拟机。

让我们来谈谈 Zig 的其他一些特性:设计上的互操作性、可调整的运行时安全性和编译时代码执行。

“通过设计实现互操作性”意味着普通的 Zig 很容易被 C 使用，反过来又会使用 C。在许多其他语言中，比如 Python，你需要专门为 C 和 C++的互操作性整理数据。凭借内置的 Clang 编译器，Zig 可以在主代码中直接包含 C 文件。Zig 库的输出是一个可以直接输入 GCC 的`.o`文件。C 代码可以通过在函数定义的开头加上`export`来使用函数。结构和数据类型有相似的容易性。

“可调整的运行时安全性”意味着 Zig 的许多运行时检查可以根据应用程序打开或关闭。像整数溢出、边界检查、不可达代码等等。

您可能会注意到，在一些代码中，Zig 中有一种数据类型叫做`comptime`。您可以在函数参数和程序本身中使用它。这意味着该值在编译时必须是可计算的。它可以用来实现某种形式的泛型或模板。这是一个非常强大的功能，可以用有趣的方式使用。

## 你会用它做什么？

因为 Zig 是基于 LLVM 的，所以 Zig 的目标包括:

*   x86_64
*   ARM/ARM64
*   每秒百万条指令
*   （IBM 和 Apple 公司联合生产的）个人台式机…
*   masm32
*   RISCV64
*   Sparc v9
*   Linux 操作系统
*   马科斯
*   Windows 操作系统
*   FreeBSD
*   蜻蜓
*   UEFI

考虑到它与 C 的互操作性如此之好，用 Zig 等价物替换小块或库是非常简单的。

此外，Zig 可以用在微控制器上。作为一个精选的例子，[凯文·勒纳]最近经历了[将他的键盘固件从 Rust 转换到 Zig](https://kevinlynagh.com/rust-zig/)的旅程。Rust 的许多众所周知的语言特性，如特性、宏和模式匹配，都用于初始化和扫描按键端口。在 Zig 中，这些被替换为`inline for`，一个在编译时展开的 for 循环，以及一些对`comptime`的巧妙使用。[Kevin]特别指出了这种语言的一致性，以及他认为自己能够掌握这种语言的原因。

如果你正在寻找灵感，这里有一个用 Zig 写的 Github repo，里面有数百个优秀的例子。有 Gameboy 模拟器，HTTP/DNS 服务器，光线跟踪器，几个内核和引导程序，数据库和编译器。

## 我该如何开始？

在 Zig 的主页上有一个[学习区，在 ziglearn.org](https://ziglang.org/learn/)[的网站](https://ziglearn.org/)上也有很多很棒的资源。 [Ziglings 是一个 Github 项目](https://github.com/ratfactor/ziglings)，它有一些小的坏程序，需要一些小的调整就能重新工作，让你对 Zig 有一个感觉。也许仅仅尝试一下还不够，你需要深入语言实现本身的最深处。