# 魔杖通过机器学习和 IMU 学习咒语

> 原文：<https://hackaday.com/2018/12/07/magic-wand-learns-spells-through-machine-learning-and-an-imu/>

詹妮弗·王喜欢打扮成角色扮演，她是哈利·波特迷。她的魔法技能是技术性的，而不是魔法性的，但对于不经意的观察者来说，她设法模糊了这些界限。她对不同的传感器有着丰富的经验，她决定将所有这些融合在一起，制成一根魔杖。该棒包含一个惯性测量单元(IMU)，因此它可以检测手势。[Jennifer]没有对所有东西进行硬编码，而是使用了机器学习，并在 Hackaday 超级会议上展示了她的成果。没去超级大陆吗？别担心，你可以观看下面[她关于构建基于 IMU 的手势识别](https://www.youtube.com/watch?v=EhxpWL65QFM)的演讲，并从 [GitHub](https://github.com/jewang/gesture-demo) 获取代码。

自然，我们喜欢看到她的项目的技术部分，这是将机器学习应用于传感器数据的绝佳入门。但是我们认为真正有见地的是关于整个设计生命周期的讨论。问一些问题来界定设计空间，比如你能花多少钱，谁会使用这个设备，你会在哪里使用它，这些问题通常是我们下意识回答但不会明确表达的事情。完全不回答这些问题会增加你的项目失败的风险，或者，至少，不会像预期的那样成功。

## 保持平衡

演讲的另一个主题是:设计行业。您必须在您想要的和其他项目现实(如速度、功耗和成本)之间进行平衡。在这种情况下，[Jennifer]指出，机器学习系统可以是精确的、内存高效的或低延迟的，她认为你只能选择两种。也就是说，小而快的模型可能不准确。快速的精确模型可能会使用大量内存，等等。

在需求和交易之间，她向你展示了她是如何设计出魔杖的体系结构，然后实际上就可以设计和建造了。例如，相机可以识别手势，但不能在黑暗中识别。最终设计包含 BNO055 IMU、Raspberry Pi Zero W、音频系统，当然还有电源。

接下来的交易涉及使用深度学习而不是更传统的方法。为了做出这个决定，她观察了每种技术会使什么变得更容易和会使什么变得更难。例如，深度学习不需要那么多领域知识，但更难调试，需要大量数据才能训练好。信号处理方法更容易调试，但需要更多的领域知识。

最后一种方法是收集大量数据，然后从这些数据中深度学习一个模型。这里的一个重要因素是覆盖率。也就是说，确保数据覆盖所有预期的用例。该模型的第一次迭代并不成功，但在第三次尝试后，事情开始变得有条不紊。

## 付诸实践

[![](img/c241467a1855a7da03e3083e6ce30d6e.png)](https://hackaday.com/wp-content/uploads/2018/12/potter.png) 软件的实用方面使用 Python 和一些数值库以及 [scikit-learn](https://scikit-learn.org) 来处理深度学习方面。Plot.ly 和 Jupyter Notebook 也提供了方便的工具。

虽然魔杖可能看起来不太实用，但演示的结尾谈到了该技术可能完成的其他事情，如地震检测或收集人口普查数据。它甚至可以检测到有人跌倒。

然而，真正的价值在于设计过程。正如她所指出的，那些相同的步骤——定义需求，完成设计交易——对每个项目都很重要。当然，有时候一个项目很小，以至于你会不假思索地去做。但是随着项目越来越大，有一个过程来确保你已经覆盖了你的需求，并且做出了与你的目标和约束一致的选择，这对于确保项目成功是一个很大的帮助。

 [https://www.youtube.com/embed/EhxpWL65QFM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EhxpWL65QFM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

