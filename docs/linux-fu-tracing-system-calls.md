# Linux Fu:跟踪系统调用

> 原文：<https://hackaday.com/2020/04/07/linux-fu-tracing-system-calls/>

Linux 和类似操作系统的一个好处是，你可以研究任何你想研究的东西。如果一个程序有问题，你可以反编译它，调试它，跟踪它，如果必要的话，甚至挖掘内核的源代码和程序可能使用的大多数库。然而，这样做的工具并不是你每天都会用到的。一个非常有趣的工具是`strace`。使用它你可以看到任何程序进行了什么系统调用，这有时可以给你关于程序如何工作的重要线索，或者更常见的是，为什么它不工作。

让我们考虑一下该命令最不复杂的用法。假设您想创建从`testxmit.grc`到`/tmp`目录的符号链接。这个命令很简单:

```
ln -sf testxmit.grc /tmp
```

但是如果你告诉`strace`去运行它，这个命令就变成了:

```
strace ln -sf testxmit.grc /tmp
```

不过，您可能希望使用 shell 或`-o`选项将输出重定向到一个文件。有些命令会生成很多内容，通常输出的前一两页并不是您真正关心的内容。

## **让我们看看**

让我们看看输出:

```
execve("/bin/ln", ["ln", "-sf", "testxmit.grc", "/tmp"], 0x7fff51ddf6f8 /* 91 vars */) = 0
brk(NULL) = 0x562301ce6000
... 
openat(AT_FDCWD, "/usr/lib/locale/locale-archive", O_RDONLY|O_CLOEXEC) = 3
fstat(3, {st_mode=S_IFREG|0644, st_size=3004096, ...}) = 0
mmap(NULL, 3004096, PROT_READ, MAP_PRIVATE, 3, 0) = 0x7f7c45298000
close(3) = 0
stat("/tmp", {st_mode=S_IFDIR|S_ISVTX|0777, st_size=1360, ...}) = 0
lstat("/tmp/testxmit.grc", 0x7fff7ae555d0) = -1 ENOENT (No such file or directory)
symlinkat("testxmit.grc", AT_FDCWD, "/tmp/testxmit.grc") = 0
lseek(0, 0, SEEK_CUR) = -1 ESPIPE (Illegal seek)
close(0) = 0
close(1) = 0
close(2) = 0
exit_group(0) = ?
+++ exited with 0 +++
```

在顶部，有 25 行代码处理将共享库加载到内存空间，4 行代码处理区域设置。我将第一个“真正的”行用粗体显示，程序在这里调用 stat on `/tmp`，然后确保该文件不存在。最后，你得到真正的系统调用(`symlinkat`)，然后是一些关闭程序的东西。一个系统调用要做很多工作。

你大概可以算出等号右边的部分是调用的返回值。通常，零代表成功，其他数字代表不同的意思。然而，例如，`openat`调用返回一个文件描述符(3 ),您可以在下一行看到它被发送到`fstat`。

## **在实践中**

当然，ln 命令是有效的，但是请迁就我一下，说我们想了解传递给`symlinkat`的参数是什么。您可以使用`-e`选项来减少输出的大小:

```
strace -e symlinkat ln -sf testxmit.grc /tmp
```

如果你按顺序做这些例子，你会注意到一些奇怪的事情。第二次运行该命令时，您会得到对`symlinkat`的两次调用。第一个失败是因为文件已经存在。第二个是一些随机的文件名。取下`-e`让你看到一切(我只展示有趣的部分):

```
symlinkat("testxmit.grc", AT_FDCWD, "/tmp/testxmit.grc") = -1 EEXIST (File exists)
openat(AT_FDCWD, "/dev/urandom", O_RDONLY) = 3
read(3, "\337\336\10\324\254\233", 6)   = 6
close(3)                                = 0
getpid()                                = 29340
getppid()                               = 29338
getuid()                                = 1000
getgid()                                = 1000
symlinkat("testxmit.grc", AT_FDCWD, "/tmp/CuzoNWnv") = 0
renameat(AT_FDCWD, "/tmp/CuzoNWnv", AT_FDCWD, "/tmp/testxmit.grc") = 0
```

注意，随机部分来自于从/dev/urandom 读取一些数据。如果您不想要所有这些输出，请尝试:

```
strace -e synlinkat,renameat ln -sf testxmit.grc /tmp
```

## **其他选项**

`-p`选项允许您提供正在运行的程序的 PID。将输出发送到一个文件，然后用一个`tail -f`来监控这个文件是一个很好的技巧。默认情况下，您只能看到 32 字节的呼叫数据，这可能还不够。你可以用`-s`选项来调整尺寸。

到目前为止，我们只看了简单的程序。但是如果你想跟踪多线程，检查一下`-f`和`-ff`选项。

如果你想调查程序调用了什么，那么`-c`选项会给你一个摘要。

```
% time     seconds  usecs/call     calls    errors syscall
------ ----------- ----------- --------- --------- ----------------
  0.00    0.000000           0         2           read
  0.00    0.000000           0         7           close
  0.00    0.000000           0         2           stat
  0.00    0.000000           0         3           fstat
  0.00    0.000000           0         1           lstat
  0.00    0.000000           0         1         1 lseek
  0.00    0.000000           0         6           mmap
  ...
  0.00    0.000000           0         4           openat
  0.00    0.000000           0         1           renameat
  0.00    0.000000           0         2         1 symlinkat
------ ----------- ----------- --------- --------- ----------------
100.00    0.000000                    46         5 total
```

**当然，还有更多…**

这只是可以用来检查 Linux 程序的众多工具之一。调试器通常是有用的，尤其是如果您有源代码的话。还有其他工具可以检查符号表和转储可执行文件。但这些是下次的话题。

你最喜欢的 Linux 逆向工程工具是什么？请在评论中告诉我们。