# Linux Fu: Shell 脚本文件嵌入

> 原文：<https://hackaday.com/2021/04/09/linux-fu-shell-script-file-embedding/>

你需要打包一堆文件，送到某个地方，在目的地用它们做一些事情。这种情况并不少见。显而易见的答案是创建一个归档文件——可能是 zip 或 tar 文件——并包含一个 shell 脚本，您必须告诉用户在解压缩后运行该脚本。

这可能是显而易见的，但是对于远程用户来说，这需要做很多假设。他们需要知道如何解压文件，还需要知道在解压后运行您的神奇命令脚本。但是，您可以轻松地创建一个包含文件的 shell 脚本，甚至是许多文件的存档，然后在运行时检索该文件并对其进行操作。从远程用户的角度来看，这要简单得多。你得到一个文件，执行它，你就完成了。

理论上，这并不难做到，但是有很多细节。Shell 脚本没有被编译——至少通常没有——所以 shell 只读取完成工作所需的内容。这意味着如果你的脚本小心退出，你可以添加尽可能多的“垃圾”到它的末尾。shell 永远不会查看它，所以可以将有效载荷存储在那里。

## 那又怎样？

那么，唯一的技巧就是找到脚本的结尾，从而找到有效载荷的开始。考虑一下这个文件，`deliver.sh`:

```

#!/bin/bash
WORKDIR=$( mktemp -d )

#find last line +1

SCRIPT_END=$( awk '
  BEGIN { err=1; } 
  /^\w*___END_OF_SHELL_SCRIPT___\w*$/ { print NR+1; err=0; exit 0; } 
  END { if (err==1) print "?"; }
' "$0" )

# check for error

if [ "$SCRIPT_END" == '?' ]
then
   echo Can\'t find embedded file
   exit 1
fi
# Extract file
tail -n +$SCRIPT_END $0 >"$WORKDIR/testfile"

# Do something with the file
echo Here\'s your file:
cat "$WORKDIR/testfile"
echo Deleting...
rm -r "$WORKDIR"
exit 0
# Here's the end of the script followed by the embedded file
___END_OF_SHELL_SCRIPT___
A man, a plan, a canal, Hackaday!

Not exactly a palindrome, but there's no pleh for it.

```

## 多个文件

如果您不介意在最后传输充满二进制垃圾的脚本文件，那么恢复的文件也可以是压缩的 tar 文件或 zip 文件。诀窍是创建您的基本脚本并将文件附加到它。因此，我可能将`deliver.sh0`作为整个文件，直到并包括`___END_OF_SHELL_SCRIPT___`标识符。然后，为了创建最终的脚本，您可以说:

```
cat deliver.sh0 bundle.zip >deliver.sh
```

## 编码、重复使用、回收

有时您不希望二进制字符弄乱您的 shell 脚本。也许您想通过电子邮件发送脚本，但又担心路径中的各种邮件系统会对您的数据造成什么影响。将二进制数据编码为文本字符串非常容易(当然，伴随着相关的大小损失)。例如，你可以简单地说:

```
cp deliver.sh0 deliver.sh
base64 bundle.zip >>deliver.sh
```

要恢复文件，您需要在脚本主体中做一些额外的工作，特别是在`tail`命令之后。

```
tail -n +$SCRIPT_END $0 | base64 -d >"$WORKDIR/bundle.zip"

```

当然，您不必存储该文件。你可以把它输入另一个程序。例如，tar 存档可能有这样一行:

```
tail -n +$SCRIPT_END $0 | base64 -d | tar xf
```

自然，您的脚本可以做任何您需要做的准备工作，然后可能在您解包后处理文件。比方说，你可以安装一个库或字体，或者将一个补丁合并到系统的现有文件中。

您甚至可以在一个脚本中嵌入一个可执行文件——甚至是另一个脚本——然后执行该脚本，这可能会解包另一个脚本。它令人困惑。请记住，并不是每个系统都允许可执行文件驻留在/tmp 或一些挂载的文件系统上，所以要做好相应的计划。

## 脚本医生

虽然 bash 脚本经常被恶意中伤，但它非常灵活和强大，正如本例所示。在脚本中嵌入文件非常容易，这为分发复杂的文件设置和应用程序提供了很多灵活的选择。

如果您正在编写严肃的 bash 脚本，我们建议您[仔细编写它们](https://hackaday.com/2017/07/21/linux-fu-better-bash-scripting/)。你甚至可以找到一个“ [lint](https://hackaday.com/2017/03/29/lint-for-shell-scripters/) 程序，它可以为你测试错误。