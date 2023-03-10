# Linux Fu:映射文件

> 原文：<https://hackaday.com/2020/03/20/linux-fu-mapping-files/>

如果你使用 C 或 C++，你可能已经学会了如何打开一个文件并从中读取数据。通常，我们一次读一个字符或一行。至少，看起来是这样。实际情况是，在您和硬盘驱动器之间通常有相当多的缓冲区，因此您对一个字符的请求可能会触发对 2，048 个字符的读取，然后您的后续调用会从缓冲区返回。甚至可以有多层缓冲器来供给缓冲器。

一台现代电脑可以做得比使用像`fgetc`这样的老式电话阅读好得多。假设你的程序有一个巨大的虚拟地址空间，并且你的计算机有一个非常好的内存管理单元，你可以要求操作系统简单地将文件映射到你的内存空间。然后，您可以像对待任何其他字符数组一样对待它，让操作系统完成剩下的工作。

操作系统不需要一次读入整个文件，它只是为你保留空间。任何时候你点击一个不在内存中的页面，操作系统都会在无形中为你抓取。不经常使用的页面可能会被丢弃并在以后重新加载。在幕后，操作系统做了很多事情，所以你可以轻松地处理非常大的文件。完成这一切的调用是`mmap`。

当然，总有一个陷阱。如果您有一个非常大的文件，您可能需要做一些工作来映射它的一部分，然后再映射一次。使用映射创建或扩展文件也需要更多的工作。尽管如此，内存映射在大多数情况下还是很容易做到的，并且非常值得学习。

## 决定

你必须决定的第一件事是，你是想读文件还是既读又写文件。如果只需要读权限，可以要求私有映射。这意味着您将获得现有的文件，您所做的任何更改都将简单地将页面复制到您自己的私有副本中。通常情况下，您不会更改以这种方式打开的文件，除非您创建一个新文件将更改写入您自己的文件。

然而，如果你想像写内存一样写文件，你需要一个共享映射。这可用于与其他进程共享数据，但也确保文件在您进行更新时得到更新——嗯，某种程度上。我们稍后会谈到`msync`。

## 阅读是基础

类似于 [wc (mmwc)](https://github.com/wd5gnr/linux-fu-mmap/blob/master/mmwc.c) 的简单字数统计程序，可以在网上找到[示例代码。它不使用](https://github.com/wd5gnr/linux-fu-mmap)[标准 I/O 调用(stdwd)](https://github.com/wd5gnr/linux-fu-mmap/blob/master/stdwc.c) ，而是使用`open`打开文件进行读取，然后将它映射到程序的地址空间。我们需要知道文件大小:一个针对`stat`的任务。以下是部分代码:

```

int fd = open(filename, O_RDONLY); // open file
struct stat finfo;
char *b;
if ( fd == -1 )
  {
  perror(filename);
  return 2;
  }
if ( fstat( fd, &amp;finfo ) == -1 ) // learn size of file
  {
  perror(filename);
  return 3;
  }
b=mmap( NULL, finfo.st_size, PROT_READ, MAP_PRIVATE, fd, 0 ); // map to memory
if ( b == MAP_FAILED )
  {
  perror("mmap");
  return 4;
  }

```

`mmap`的论据很简单。第一个是地址。除非你要做一些特别的事情，否则你几乎不需要指定地址。如果你这样做，有许多关于如何设置地址的规则，这些规则因平台而异。通过指定`NULL` , `mmap`将为您挑选一个位置。下一个参数是后跟标志的长度。在这种情况下，我们告诉系统我们只想读取文件。我们还指定了一个私有映射，然后是文件句柄和从文件开始的偏移量。

一旦这个调用成功，`b`变量就有了一个指向内存中整个文件的指针。将它打印出来就像:

```

while (--len) putchar *b++;

```

下面的代码实现了一个简单的字数统计引擎。注意函数`do_work`从不使用任何与输入文件相关的调用。它只是处理内存中的数据:

```

while (len--) // process each character
 {
 if ( *b == '\n' ) l++;
 if ( isspace(*b) )
  {
  if (state==1)
   {
   w++;
   state=0;
   }
  }
  else state=1;
  b++;
}

```

## 写作和 msync 的考虑

编写有点棘手，因为文件是共享的，而且还需要已经有内容。例如，你可以使用`lseek`来设置一个文件位置，然后在末尾写一些东西，这样文件就被预加载了。

在 Linux 2.6.19 之前，你必须调用`msync`来确保文件写到磁盘，但是现在你不用了。然而，如果您认为您的代码可以在旧的内核上运行，那么在写入映射文件时使用`msync`可能是明智的。

在示例程序 [mmup.c，](https://github.com/wd5gnr/linux-fu-mmap/blob/master/mmup.c)中，我们通过就地处理文件来回避大小问题。另外，我还打电话到`msync`里。`mmap`行与前一版本相似:

```

b = mmap( NULL, finfo.st_size, PROT_READ|PROT_WRITE, MAP_SHARED, fd, 0 );

```

看看转换代码有多简单:

```

int do_work( char *b, unsigned int len )
  {
  while (len--)
    {
    *b=toupper(*b);
    b++;
    }
  return 0;
}

```

那不是很容易吗？

目前编译器和库都相当不错，所以我将把性能测量留给感兴趣的人作为练习。这在很大程度上也取决于您的磁盘 I/O 系统有多好。理论上，内存映射 I/O 应该比真正进行磁盘 I/O 的程序快。但是，库可能会在背后进行缓冲甚至映射，所以性能差异可能非常小。但是不管性能如何，代码的简化是一个很大的优势。

## 完美？

这看起来很棒，但是你应该意识到一些潜在的问题。我们习惯于认为，如果我们从磁盘中读取一些数据，没有任何问题，我们就可以忘记它。但是映射一个文件并不等同于读取它。假设您将一个文件映射到网络驱动器上，并可能从中读取一些页面。然后网络瘫痪。新的页面读取将导致错误，因为底层文件现在已经不在了。你可以捕捉到表明这一点的`SIGBUS`信号，但接下来你会怎么做？

当然，如果您仍然支持 32 位操作系统，您可能会发现在处理大文件时很快就会用完地址空间。的确，你可以在文件中创建一个带有偏移量的小窗口，但是这需要更多的工作。

另一方面，`mmap`使得许多文件处理程序更简单，更容易编写。在您的 Linux 编程技巧中，它是值得拥有的。