# 你下一个项目中的自然语言 AI？这比你想象的要容易

> 原文：<https://hackaday.com/2022/05/18/natural-language-ai-in-your-next-project-its-easier-than-you-think/>

想让你的下一个项目变成废话吗？把无聊的日志消息动态改写成科幻的 technobabble？愉快地(或勉强地)回答问题？OpenAI 的 GPT-3 可以完成这类事情以及更多事情，这是一个自然语言预测模型，其 API 可能比你想象的更容易使用。

事实上，如果你有基本的 Python 编码技能，或者甚至只是有能力编写一个`curl`语句，你就拥有了将这种能力添加到你的下一个项目中所需要的一切。从长远来看，它不是免费的，虽然注册时初始使用是免费的，但对于个人项目来说，成本将非常小。

## 基本概念

OpenAI 有一个 API，可以提供对 GPT-3 的访问，这是一个机器学习模型，能够执行任何涉及理解或生成自然语言的任务。

OpenAI 提供了一些优秀的文档和一个网络工具，人们可以通过它进行交互式实验。然而，首先必须创建一个帐户并接收一个 API 密钥。完成后，门是开着的。

创建一个账户也给了一个人一些免费的积分，可以用来试验想法。一旦免费试用用完或过期，使用 API 就要花钱。多少钱？坦白说，不是很多。发送到(和从)API 接收的所有东西都被分解成令牌，并且[定价](https://openai.com/api/pricing/)是每一千个令牌从 0.0008 美元到 0.06 美元。一千个代币大概是 750 个字，所以小项目真的不是一个大的财务承诺。我的免费试用有 18 美元的积分，到目前为止我只花了其中的 5%。

让我们仔细看看它是如何工作的，以及可以用它做些什么！

## 它是如何工作的

[![](img/7d020e0d3863dfeb32ce1632f8205ddf.png)](https://hackaday.com/wp-content/uploads/2022/05/hackaday-OpenAI-prompt.png)API 接受请求的方式多种多样，如果你能精心制作一个`curl`语句，使用命令行，或者编写一些简单的 Python(或者 node.js)代码，那真是好消息！你已经拥有了开始尝试创意所需的一切！

我将描述以最基本的方式使用 API，即**完成**。这意味着向 API 呈现一个*提示*，从这里它将提供一个文本*完成*，试图匹配提示。所有这些都是完全在文本中完成的，并被格式化为自然语言。

以这种方式使用 API 可以被认为是实现了一种高性能的自动完成功能。引擎本身可以被认为是一种非常复杂的状态机，同时它也不完全像其他任何东西。

## 什么样的东西是可能的？

这里有一个非常简单的例子:

| 提示(发送到 API) | 完成(来自 API 的响应) |
| --- | --- |
| 写一个机智的电池电量低的错误信息。 | “你跑空了！” |

*提示*也是一个人如何“编程”模型，设计一个好的提示是获得好结果的一个重要部分。

因为该模型能够理解语言结构和意图，所以一个*提示*可以被表述为好像一个人在给一个中学生布置写作任务。

下面是一个稍微复杂一点的例子:

| 提示 | 完成 |
| --- | --- |
| Provide excited commentary for an event in a tabletop game about trains.事件:一个叫 Rob 的玩家卖掉了一家公司。
解说: | “罗布已经决定卖掉他们的公司。这是一个重大举措，将对游戏产生重大影响。谁将收购这家公司？他们会用它做什么？只有时间会证明一切。” |

在上面的例子中有一些事情需要指出。提示符的第一行描述了要做的事情。接下来的两行(“Event:”和“commentation:”设置了如何完成语句的模型。请注意，提示中的“注释:”行是空白的；该模型将完成已开始的工作。

精心制作有效提示的实践被称为[提示设计](https://beta.openai.com/docs/guides/completion/prompt-design)，它是从 API 获得各种有用和不同响应的关键。让我们仔细看看即时设计是如何影响结果的。

## 获得更好的回应

如果一个人很难让模型以一种有用的方式做出响应，那么在提示本身中包含多个所需内容的示例会有所帮助，从而让模型更好地了解预期内容。

API 文档[很好地展示了这一想法](https://beta.openai.com/docs/quickstart/start-with-an-instruction)，我将在下面简要重申一下:

| 提示(发送到 API) | 完成(来自 API 的响应) |
| --- | --- |
| 给一匹超级英雄马起三个名字。 | 超人，蝙蝠侠，蜘蛛侠 |

这个结果并不是我们真正想要的。但是，在提示中包含一些例子会产生明显更好的结果:

| 提示(发送到 API) | 完成(来自 API 的响应) |
| --- | --- |
| Suggest three names for an animal that is a superhero.动物:猫
姓名:夏普克劳队长、弗布探员、神奇猫
动物:狗
姓名:保护者拉夫、神奇犬、汪汪先生
动物:马
姓名: | 骏马，烈马，雷蹄 |

这样做会增加成本——回想一下，无论是在提示中还是在输出中，每个令牌都要付费——但是在提示中提供多个示例在某些情况下可能是获得最佳结果的关键，因为它让模型更清楚地知道请求的是什么，以及应该如何格式化。

同样，把这个提示看作是中学生的写作作业是有帮助的；一个中学生，反过来，他可以被认为是一个极其复杂和有点易变的状态机。

## 相同的提示，不同的完成

对于相同的提示，API 不一定返回相同的结果。虽然提示的性质和模型被训练的数据会发挥作用，但是响应的多样性也会受到请求中的`temperature`设置的影响。

温度是一个介于 0 和 1 之间的值，它表示在对有效的完成进行预测时，模型应该有多确定。温度为 0 意味着每次提交相同的提示都会得到相同(或非常相似)的响应。零度以上的温度每次都会产生不同的完井。

换句话说，较低的温度意味着模型承担的风险较小，从而导致完井更具确定性。这在需要可以准确预测的完成时是有用的，例如实际的响应。另一方面，提高温度——0.7 是典型的默认值——会使完井更加多样化。

## 微调模型

API 背后的自然语言模型是预先训练好的，但是仍然可以使用为特定应用程序定制的单独数据集来定制模型。

这个被称为[微调](https://beta.openai.com/docs/guides/fine-tuning/fine-tuning)的功能允许用户有效地为模型提供比每个提示中实际包含的更多的例子。事实上，一旦提供了微调数据集，就不再需要在提示本身中包含示例。请求也会得到更快的处理。

除了狭窄的应用程序之外，这可能不需要，但是如果您发现为您的项目获得可靠的结果依赖于大的提示，并且您希望它更有效，[微调](https://beta.openai.com/docs/guides/fine-tuning/fine-tuning)是您需要考虑的地方。如果你需要的话，OpenAI 提供的工具可以让这个过程尽可能的简单。

## 代码是什么样子的？

有一个交互式的网络工具( [playground](https://beta.openai.com/playground) ,需要一个帐户),在这个工具中，人们可以使用模型来测试想法，而不必编写代码，但它也有一个方便的功能，可以根据请求生成代码片段，便于复制和粘贴到项目中。

这是本文中的第一个例子，格式为一个简单的`curl`请求:

```
curl https://api.openai.com/v1/engines/text-davinci-002/completions \
  -H &quot;Content-Type: application/json&quot; \
  -H &quot;Authorization: Bearer $OPENAI_API_KEY&quot; \
  -d '{
  &quot;prompt&quot;: &quot;Write a witty error message for a low battery condition.&quot;,
  &quot;temperature&quot;: 0.7,
  &quot;max_tokens&quot;: 256,
  &quot;top_p&quot;: 1,
  &quot;frequency_penalty&quot;: 0,
  &quot;presence_penalty&quot;: 0
}'

```

同样的，这次是用 Python:

```

import os
import openai

openai.api_key = os.getenv(&quot;OPENAI_API_KEY&quot;)

response = openai.Completion.create(
engine=&quot;text-davinci-002&quot;,
prompt=&quot;Write a witty error message for a low battery condition.&quot;,
temperature=0.7,
max_tokens=256,
top_p=1,
frequency_penalty=0,
presence_penalty=0
)

```

安装 python 包的同时还会安装一个实用程序，可以从命令行直接使用该实用程序以获得最大的便利:

```

$ openai api completions.create -e text-davinci-002 -p &quot;Write a simple poem about daisies.&quot; --stream -M 128

```

(注意:`--stream`显示收到的结果，`-M 128`将回复限制为最多 128 个令牌。)

提示“写一首关于雏菊的简单诗”为我生成了以下文本，每次都不一样:

```

The daisy is a beautiful flower 
That grows in the meadow and in the pasture 
It has a yellow center and white petals 
That make it look like the sun 
The daisy is a symbol of innocence 
And purity and is loved by all

```

所有上面的例子都以同样的方式工作:它们向 OpenAI API 发出提示(使用一个人的 API 密钥进行访问，上面的例子假设它已经被设置为一个名为`OPENAI_API_KEY`的环境变量),并接收带有响应的回复。

## 负责任的使用

值得强调的是 OpenAI 对负责任使用的承诺，包括对应用的[安全最佳实践](https://beta.openai.com/docs/usage-guidelines/safety-best-practices)的指导。在该链接中有许多深思熟虑的信息，但简短的版本是要始终记住，这是一个工具:

1.  能够以**非常可信的方式**编造事情**，并且**
2.  能够与人交流。

不难看出，如果不负责任地使用，这种组合有潜在的危害。像大多数工具一样，人们应该小心误用，但是工具也可以是美好的东西。

## 你有想法了吗？

从长远来看，使用 API 不是免费的，但是创建一个帐户会给你一组免费的积分，可以用来玩一玩和尝试一些想法，并且为个人项目使用即使是最昂贵的引擎成本也很低。到目前为止，我所有的热情实验只使用了价值不到两美元的免费试用版。

需要一些灵感吗？我们已经介绍了几个在这个方向上涉水的项目。这款[机器人推球游戏使用自然语言人工智能生成垃圾话](https://hackaday.com/2022/04/09/amazing-connect-fore-robot-challenges-your-putting-practice/)，而[深度梦境播客](https://hackaday.com/2022/03/26/ai-generated-sleep-podcast-urges-you-to-imagine-pleasant-nonsense/)完全由机器生成的童话组成，作为睡眠辅助工具，并且是用 OpenAI API 创建的。

现在你知道了什么样的事情是可能的，它们有多简单，也许你已经有了一些想法？让我们在评论中了解他们吧！