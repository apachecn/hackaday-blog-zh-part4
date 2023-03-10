# Linux Fu :(几乎)立即为命令行程序提供 Python 图形用户界面

> 原文：<https://hackaday.com/2019/10/14/linux-fu-python-guis-for-command-line-programs-almost-instantly/>

不是每个程序员都喜欢创建 GUI 代码。大多数黑客类型不介意命令行界面，但很少有普通用户欣赏它们。然而，如果你用 Python 写命令行程序，Gooey 可以帮上忙。通过利用一些 Python 特性和一个通用的 Python 习语，您可以毫不费力地将命令行程序转换成 GUI。

这个想法很简单。几乎所有的命令行 Python 程序都使用`[argparse](https://docs.python.org/3/library/argparse.html)`来简化从命令行选择选项和参数，并提供一些帮助。Gooey decorator 会选择所有选项和参数，并为其创建一个 GUI。如果你想改变某些特定的东西，你可以把它变得更复杂，但是如果你对默认设置满意，就没什么其他的了。

起初，这篇文章可能看起来像一个 Python Fu 而不是 Linux Fu，因为——首先——我们将把重点放在 Python 上。但是只要看看袖手旁观，你就会发现它是如何在许多操作系统上做很多事情的，包括 Linux。

## 把手放在某物或者某人身上

我们必须尝试一下。下面是来自`argparse`手册页的代码，扩展到主函数内部:

```

import argparse

def main():

   parser = argparse.ArgumentParser(description='Process some integers.')
   parser.add_argument('integers', metavar='N', type=int, nargs='+',
         help='an integer for the accumulator')
   parser.add_argument('--sum', dest='accumulate', action='store_const',
        const=sum, default=max,
   help='sum the integers (default: find the max)')

   args = parser.parse_args()
   print(args.accumulate(args.integers))

main()

```

您可以在命令行运行它(我们称之为 iprocess.py):

```
python iprocess.py 4 33 2
python iprocess.py --sum 10 20 30
```

在第一种情况下，程序将选择并打印最大的数字。在第二种情况下，它会将所有参数加在一起。

创建一个 GUI 只需要两步(除了安装 Gooey):首先，在文件的顶部导入 Gooey:

```
from gooey import Gooey
```

然后在主定义之前的行上添加 decorator @Gooey(并且，是的，它确实需要在之前的行上，而不是在同一行上):

```
@Gooey
def main():
```

结果看起来像这样:

[![](img/cdb12d3412d6c90c6fb17cdcd3eb1938.png)](https://hackaday.com/wp-content/uploads/2019/09/dlg0.png)

您可能想要调整结果，也可以非常容易地添加验证，因此一些字段是必需的或者必须包含特定类型的数据。

## 当然这在 Linux 上行得通，但是…

当然，Python 可以在许多不同的平台上运行。那么为什么这是 Linux Fu 的一部分呢？因为您可以很容易地使用它来启动任何命令行程序。没错，这也可以在其他操作系统上运行，但是在有很多命令行程序的 Linux 上尤其有用。

我们第一次看到这个是在 Chris Kiehl 的博客上，他为 ffmpeg 做了一个 GUI——或者我想是 Gooey——它有很多命令行选项。想法是为程序编写一个简单的 argparse 设置，然后告诉 GUI 在组装命令行后实际启动什么可执行文件。

![Chris Kiehl ffmpeg GUI](img/344917ce57f0648e6c42d48b4515b034.png)

这是克里斯的代码:

```

from gooey import Gooey, GooeyParser

@Gooey(target="ffmpeg", program_name='Frame Extraction v1.0', suppress_gooey_flag=True)
def main():
   parser = GooeyParser(description="Extracting frames from a movie using FFMPEG")
   ffmpeg = parser.add_argument_group('Frame Extraction Util')
      ffmpeg.add_argument('-i',
      metavar='Input Movie',
      help='The movie for which you want to extract frames',
      widget='FileChooser')
   ffmpeg.add_argument('output',
      metavar='Output Image',
      help='Where to save the extracted frame',
      widget='FileSaver')
   ffmpeg.add_argument('-ss',
      metavar='Timestamp',
      help='Timestamp of snapshot (in seconds)')
   ffmpeg.add_argument('-frames:v',
      metavar='Timestamp',
      default=1,
      gooey_options={'visible': False})

parser.parse_args()

if __name__ == '__main__':
   main()

```

如果你不想写 Python，你甚至可以选择创建一个 Gooey 可以阅读的 JSON 文件。它的效用很容易看到，但我很想听一些具体的例子，看看它在什么地方会派上用场。如果你已经在使用 Gooey，或者在读完这篇文章后打算尝试一下，请在下面的评论中告诉我们。

当然，并不是所有的[Python GUI](https://hackaday.com/2019/05/10/python-and-pi-provide-heads-up-display-for-your-experimental-airplane/)都是一样的。也不是所有的 [Python 图形](https://hackaday.com/2019/03/07/make-xkcd-style-plots-from-python/)。