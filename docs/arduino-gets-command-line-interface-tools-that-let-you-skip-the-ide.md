# Arduino 拥有命令行界面工具，可以让你跳过 IDE

> 原文：<https://hackaday.com/2018/08/26/arduino-gets-command-line-interface-tools-that-let-you-skip-the-ide/>

Arduino 现在有了官方支持的命令行界面。该项目名为 arduino-cli，是官方工具链首次脱离基于 Java 的编辑器 Arduino IDE。下面可以看到官方公布的视频。

显然这不是一个新想法。[平台 IO](https://hackaday.com/2017/04/07/platformio-and-visual-studio-take-over-the-world/) 等命令行驱动工具存在。但是官方支持意味着，即使你不想自己使用命令行，这也应该开辟一条道路，将 Arduino 构建过程更容易地集成到其他 ide 中。

代码是开源的，但是他们在官方声明中提到你可以授权它用于商业用途。我们认为这意味着如果你想把它做成一个产品，而不仅仅是提供一个界面。这似乎是 Arduino 所期望的，因为许多命令行工具可以生成 json，这是一种将信息发送到另一个应用程序进行解析的公平方式。

命令行界面不只是构建一个草图。你可以做像安装和管理库这样的事情。例如，要创建新草图:

```
arduino-cli sketch new HackadayPgm
```

您可以更新已安装的平台，列出已连接的主板，并搜索主板支持:

```
arduino-cli core update-index

arduino-cli board list

arduino-cli core search mkr1000
```

如果您还没有主板支持，您可以安装它并验证它是否存在:

```
arduino-cli core install arduino:samd

arduino-cli core list
```

最后一步将为您提供核心的 FQBN 或唯一名称。因此，为了编译和上传，你有这样一口:

```
arduino-cli compile --fqbn arduino:samd:mkr1000 Arduino/HackadayPgm

arduino-cli upload -p /dev/ttyACM0 -fqbn arduino:samd:mkr1000 Arduino/HackadayPgm

```

与 PlatformIO 不同，这显然更适合构建成一个工具，即使它是一个 makefile。我们希望看到一个. build.json 文件，或者允许你在一个工作目录中发出简短的命令来做正确的事情。当然，您可以用一点 shell 脚本来构建它。嗯…

很高兴看到一个官方方法的发布，我们希望这将导致更多的编辑能够无缝地处理 Arduino。

 [https://www.youtube.com/embed/3vtIisvxewc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3vtIisvxewc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

