# Raspberry Pi 仅使用默认的 Linux 工具播放音乐

> 原文：<https://hackaday.com/2019/05/02/raspberry-pi-streams-music-using-only-the-default-linux-tools/>

启动家庭音乐流媒体系统通常是一项简单的任务。在苹果设备上使用 Airplay 让这项任务变得很简单，但是如果你是一个像[Connor]这样运行 Linux 机器的纯粹计算主义者，并且希望在额外的软件包上保持轻量级，这项任务会很快变得复杂。他的目标是[将音频流带到所有 Linux 平台，而不需要安装大量额外的软件](http://connor-brooks.com/play_stdin.sh.html)。这种方法对于像他在概念验证中使用的 Raspberry Pi 这样的轻型设备来说是友好的。

[Connor]创建了一组[脚本](https://github.com/connor-brooks/play_stdin.sh),允许从任何 UNIX(或类 UNIX)机器上流式传输，只使用典型操作系统安装已经拥有的依赖关系。他的 Raspberry Pi 是基站，并传输到他的笔记本电脑，但他指出，这几乎可以在任何 UNIX 或 Linux 机器上工作。唯一的限制是 FFmpeg 能不能播放什么。

我们肯定能够欣赏对软件及其使用的原则性方法，尽管看起来大多数人并没有把这个问题放在他们头脑的最前面。这导致许多软件体积庞大，很难维护、使用，甚至不知道它是做什么的，也让我们这些不想使用这类软件的人更难找到其他问题的解决方案。[康纳]能够在不牺牲任何原则的情况下创造一些东西，这很高尚。