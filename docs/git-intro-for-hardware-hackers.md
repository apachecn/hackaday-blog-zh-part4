# 硬件黑客 Git 简介

> 原文：<https://hackaday.com/2022/09/12/git-intro-for-hardware-hackers/>

Git 是一个很棒的工具，它可以成倍增加你的项目的影响，或者使你的项目更容易管理。我们中的一些黑客还不知道如何使用命令行 Git，但是一个相关的例子来说明为什么某种工具会有用可能是一个好的开始。今天，我想给大家上一堂 Git 速成课——向大家展示为什么以及如何将 KiCad PCB 放入 Git 存储库，稍后与全世界分享。

KiCad 与 Git 配合得非常好。KiCad 的原理图和 PCB 文件是人类可读的，尤其是与其他 PCB 文件格式相比。KiCad 为不同的目的创建不同的文件，每个文件都有明确定义的角色，您可以理解项目文件夹中的每个文件。更重要的是，您甚至可以在文本编辑器中修改 KiCad 文件！这正是 Git 非常适合的那种用例。

## 不仅仅是软件开发人员

那你在干什么？从根本上来说， [Git](https://git-scm.com) 是一个帮助你跟踪项目中代码变化的工具，并且互相分享这些变化。它的第一个目标是 Linux 内核开发，这就是它的设计目的，但是它的灵活性远远超出了软件项目。我们硬件黑客可以以各种方式利用它——我们可以存储 PCB 和其他设计软件文件、博客文章、项目文档、个人笔记、配置文件以及任何其他甚至与 Git 操作方式不太相符的东西。

![A screenshot of a file explorer, showing KiCad PCB files of a Jolly Wrencher (Hackaday symbol).](img/91c9e73e56a0aaed7aecc4593c6d1b37.png)

Naturally, it’s important that these files are stored in a safe and failproof manner.

使用 Git 的第一个好处是项目的备份。事实上，如果你上传你的 git 修改到某个地方，你会得到你的项目的两个额外的副本——一个存储在你的本地`.git`文件夹，一个上传到 GitHub 或 GitLab。事实上，一个存储在 Git 中带有在线镜像的项目自动符合[3-2-1 备份原则](https://www.uschamber.com/co/run/technology/3-2-1-backup-rule)。此外，历史备份触手可及。你是否早就重新设计了你的 PCB，现在急需参考更早的版本？只要您一直在 Git 中保存您的更改，它们就在一个命令之外。

许多人也在 Git 中存储配置文件——你可能听说过这种做法被称为[点文件。](https://wiki.archlinux.org/title/Dotfiles)这样做有助于跟踪您所做的所有配置更改。如果你曾经通过重新组合配置文件中的参数调试过一个复杂的软件(比如说一个 web 服务器)，你就会知道当你忘记一个曾经有效的更改时有多痛苦——而丢失一个精心定制的配置文件是完全不同层次的痛苦。有了几个 Git 命令，您就可以避免以前不知道可以避免的痛苦。

通常，我们黑客需要彼此的帮助——对于这种情况，Git 的协作能力是首屈一指的。比方说，你发现自己和一个来自世界各地的黑客伙伴一起做一个 PCB 项目。有了 Git，您只需要一个命令来上传您的最新更改，而您的同事只需要一个命令来下载它们。如果你们都以冲突的方式进行了变更(比如，以不同的方式编辑了相同的足迹)，Git 有一个丰富的变更集冲突解决工具包，释放了宝贵的时间，你们可以将这些时间花在争论高级设计问题上。

## 黑客，见见 Git–Git，见见黑客

首先，你有一个 PCB 项目，并且你已经在你选择的操作系统上安装了一个 Git shell 。我还假设你知道你的终端的基本知识——从一个目录移动到另一个目录和打开文件，我们不需要更多。在开始之前，Git 需要配置一些小的变量——让我们把这些整理出来，并利用这个机会在您选择的控制台中测试`git`功能。

为了跟踪你的变化，Git 想知道你的名字和电子邮件——这些不必是真实的。如果您将您的更改推送到 GitHub/GitLab/etc，任何人都可以从您上传它们的地方下载存储库内容，也就是说，通常是任何人。我使用我的昵称和我的旧的面向公众的电子邮件地址，用于合作和“就这个项目联系我”——你也可以这样做，或者如果你永远不会上传，就使用 John Doe 的默认设置。下面是您应该运行的命令，[摘自这里](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration):

`git config --global user.name "John Doe"
git config --global user.email johndoe@example.com`

作为`--global`，这些改变只需要在每台用于 Git 工作的机器上做一次。除了这两个之外，让 Git 知道您更喜欢哪个文本编辑器来进行快速更改也很有帮助——这些编辑器会经常被调用。在 Linux 上，您可能会发现 git commit 的默认编辑器已经设置为 Vi——如果您不知道`:wq!`代表什么，可以运行运行`git config --global core.editor nano`来获得更友好的选项。在 Windows 上，你会希望[做一些不同的事情。](https://stackoverflow.com/questions/10564/how-can-i-set-up-an-editor-to-work-with-git-on-windows)

现在，你可以开始了。在您的终端中，移动到存储 PCB 项目的文件夹。键入`git init`并按回车键。就这样——您的项目文件夹现在是一个 Git 存储库了！

## 添加您的更改

![](img/8bfb14125d898593328498853db0e18a.png)从这里开始，Git 还没有跟踪你的项目文件。运行`git status`，看到一堆标记为“未跟踪”的文件。`git status`告诉您如何开始跟踪他们——事实上，这个命令为 Git 新手提供了相当多的帮助，您可以从输出中看到这一点。让我们添加我们关心的文件——即除了`.kicad_prl`文件和`-backups/`目录之外的所有文件！

```
$ git add jolly_wrencher.svg
$ git add jolly_wrencher.kicad_mod
$ git add jolly_wrencher_pcb.kicad_pro
$ git add jolly_wrencher_pcb.kicad_pcb
$ git add jolly_wrencher_pcb.kicad_sch
$ git status
```

![](img/e6578f67c8c30900503806eb5b3e450d.png)这些文件已经被添加到 Git 正在关注的列表中，但是它们还没有以一种重要的方式融入到项目的 Git 历史中。为此，我们需要提交，它注册了一组文件更改。像这样启动一个存储库，您通常会做一个“初始”提交——为此，您可以运行`git commit -m "Initial commit"`,这里的`-m`参数是一个人类可读的消息，描述了变化的含义。你也可以做`git commit`，在一个单独的编辑器中写消息——看看哪个对你来说更舒服。由于这些文件不是以前提交的，它们将被完整地存储。

## 一点承诺

提交是一种“工作单元”,一种逻辑分组变更的方式。您可以在项目开发的不同阶段在项目历史中的提交之间导航，将一些包含提交的调整分离到不同的分支中，以便您可以无缝地共存多个不同版本的项目，在存储库之间传输提交，导出并通过电子邮件发送它们，等等。

在不同的提交中保存逻辑上不同的更改是有意义的。比方说，您改进了 PCB 上的丝网印刷，还添加了一个许可证文件。首先，您添加您的`.kicad_pcb`文件，并提交“丝印:添加引出线”消息；然后，添加您的`LICENSE.txt`文件，并将其提交为“添加的许可证”。这有助于您概述项目的历史，追踪错误，以及其他许多事情。

如果您运行`git log`，您将看到提交列表。使用它们的散列，当您需要项目的旧版本时，您可以在提交之间移动。为此，do `git checkout HASHCHARS`，其中“HASHCHARS”至少是 7 个前字符(可以更多！)的提交散列。要回到项目的最新状态，请执行`git checkout HEAD`。

## 不需要跟踪一切

`git status`仍然向我们显示了`.kicad_prl`和我们不需要跟踪的备份目录——这两个目录不包含有意义的更改。为了忽略这两种文件，在项目的主目录中创建一个`.gitignore`文件(名称以点开始),并将这两个条目放入其中:

```
*.kicad_prl
*-backups/
```

如你所见，你可以在那里做一些非常简单的模式匹配，但是你也可以输入实际的项目文件名——我不想把它们打出来，如果你想复制粘贴，更通用的版本会很方便。`git status`将不再显示这些文件，当您添加并提交`.gitignore`文件时，这两个条目将会保留。想要一个特定于 KiCad 的 gitignore 文件来涵盖您将遇到的大多数情况吗？ [GitHub 提供一个](https://github.com/github/gitignore/blob/main/KiCad.gitignore)。

![](img/e61d16233c2fd5716a2b1e0f7fb03243.png)

Tracking binary files in Git makes your project folder grow in a way you might not expect

Git 不理解二进制文件——它是为以有意义的方式改变的人类可读的文本文件而设计的。KiCad PCB 文件符合这一标准，而许多其他文件则不符合。事实是，二进制文件的每个版本都将无限期地作为副本保留在您的`.git`文件夹中，在您用新版本更新二进制文件之后很长一段时间。您不希望在项目的 git 存储库中存储一个频繁变化的`.zip`,也不希望在那里存储 gerber 文件。只是占用了额外的空间和时间。

## 免费的额外功能

git 的版本控制功能在 PCB 开发中非常方便，并且有许多细节使它使用起来更加舒适。例如，如果您想更快地在项目版本之间移动，您可以为提交附加标签。你开发了一个版本 2 的 PCB，但是仍然需要参考版本 1 的文件来获得客户支持吗？Do `git tag v2`将当前提交标记为“v2 ”, do`git tag commit v1 HASHCHARS`指向一个提交，其中 PCB 仍然在 v1。现在，你可以根据需要通过`git checkout v1`和`git checkout v2`在不同版本之间切换。

假设你提交了一个`README.md`文件——这是一个很好的实践(请随意使用[我的 PCB 自述文件模板！](https://raw.githubusercontent.com/CRImier/MyKiCad/master/TEMPLATE.md))。为了便于讨论，我们还假设您刚刚将一些图像添加到项目目录中，并将它们链接到自述文件中。比方说，您还编辑了自述文件，添加了一些完全不相关的更改，这些更改属于一个单独的提交，也许您已经更改了 PCB 上的一个连接器，并在自述文件中反映出来。你如何将你对同一个文件所做的逻辑上不同的更改分开呢？使用`git add --patch README.md`交互选择添加文件的哪些部分。

提交了一些东西，想修改最后一次提交的消息吗？使用`git commit --amend`。需要在最后一次提交时添加/删除/调整文件吗？添加您的更改和`commit --amend`。对文件做了一些更改，并希望删除它们而不是添加？使用`git checkout path/to/file`–你将丢失这些更改，因为文件将恢复到当前跟踪的版本。哦，你也可以使用`--patch`和`git checkout`来部分还原更改。

Git 有大量有用的子命令。如果您想在控制台中查看项目文件的当前更改，请使用`git diff`。你是否已经添加了一些更改，但它们不会显示出来？使用`git diff --cached`。这两个命令都接受文件名，以便进行更有针对性的概述。Git 能够处理很多复杂的问题，是一种适用于最大规模分布式软件开发工作的工具。如果你不想使用，你实际上也不需要使用任何花哨的功能。

## 下一步:上传

正如你所看到的，我还没有谈到上传到一个在线存储库或者与他人合作；这些是带有相当多重要警告的主题。我还想介绍 GitLab 和 GitHub，这样你就不会被局限在一个单一的生态系统中。我也没有讨论分支——一个典型的 PCB 项目不需要这样做，但是我们可能会在以后的文章中讨论这个问题。不过，你可以边走边学。现在，您已经准备好使用 Git 进行简单的项目了！