# 不要睡在草坪上，这里有一个人工智能驱动的喷火器机器人

> 原文：<https://hackaday.com/2021/09/11/dont-sleep-on-the-lawn-theres-an-ai-powered-flamethrower-wielding-robot-about/>

你知道这是怎么回事，你只是在院子里闲逛，一天中没有足够的时间，而且给草坪除草是如此的乏味。然后一个想法突然出现在你的脑海里。我们将一个气体动力喷火器连接到机器人手臂上，在坦克履带机器人基地上驾驶它，并让它通过人工智能大脑自主操作，怎么样？是的，听起来是个好主意。就这么办吧。因此，[戴夫·尼温斯基]用他的终极除草机器人做到了这一点。

你认为机器人霸主可能会采取更微妙的方式，一次一台咖啡机地接管世界？不，那就直奔全自动喷火器吧。

这个建筑使用了一个 [Kinova 机器人第三代](https://www.kinovarobotics.com/en)六轴臂，安装在一个[敏捷 X 机器人](https://indrorobotics.ca/ground-2/)掩体基座上。控制是通过一个 [Connect Tech Rudi-NX box](https://connecttech.com/product/rudi-nx-embedded-system-nvidia-jetson-xavier-nx/) 进行的，其中包含一个 Nvidia Jetson Xavier NX Edge AI 计算引擎。哇，那是一口！

从控制器到基座的连接是通过 [CAN 总线](https://en.wikipedia.org/wiki/CAN_bus)实现的，但是，遗憾的是没有提到机械臂控制器是如何连接的。至少这个特殊的型号配备了一个效应器安装的摄像机系统，它可以直接进入喷气发动机，在某种程度上简化了制造。

为了开始软件方面的事情，[戴夫]在他的草坪上散步时用他的手机拍了一段视频。接下来，他使用 [RoboFlow](https://roboflow.com/) 来突出显示包含杂草的图像静止图像，这些图像静止图像又被用来帮助训练视觉人工智能系统。实际的人工智能训练是使用[谷歌合作实验室](https://colab.research.google.com/notebooks/intro.ipynb)用 Python 编写的，它本身基于令人敬畏的 [Jupyter 笔记本](https://hackaday.com/2019/02/22/drops-of-jupyter-notebooks-how-to-keep-notes-in-the-information-age/)(参见主站点上的 [Jupyter 实验室)。如果你还没有尝试过，如果你做了任何数据科学，你会后悔没有这样做！)Collaboratory 本身并不那么有用，除非它通过云给你直接、免费的 GPU 访问，所以你可以用它来处理人工智能工作负载，而不需要在你的桌子上有花哨的(目前很难得到的)GPU 硬件。](https://jupyter.org/)

硬件的细节可能有点稀疏，但至少所需的软件可以在 [WeedBot GitHub](https://github.com/davesarmoury/WeedBot) 上找到。反正我们大多数人都不会有这种硬件。为了更完整的描述这个可怕的装置，休息后查看视频。

 [https://www.youtube.com/embed/fG6LRElZra0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fG6LRElZra0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

