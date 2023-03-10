# 一个简单的基于网络的线束工具

> 原文：<https://hackaday.com/2022/07/15/a-simple-web-based-wiring-harness-tool/>

当构建电子组件时，经常需要构建定制电缆来连接东西。如果你是手工制作原型，或者只是制作一两件东西，这都没问题，但如果你是在外部帮助下完成的，那么你需要确保电缆描述非常准确。[Christian Nimako-Boateng Jr.]为我们展示了第一个版本的 [wirely，一个线束工具](https://androidcircuitsolver.com/wirely)。这是一个基于网络的工具，允许用户描述电缆末端及其之间的连接，生成方便的图形，并以易于理解的格式导出到 excel。

基于在基于[烧瓶](https://flask.palletsprojects.com/en/2.1.x/)的后端上运行的 [wireviz Python 库](https://pypi.org/project/wireviz-web/#:~:text=WireViz%20is%20a%20tool%20for,a%20lot%20of%20extra%20features.)，图像数据被发送到 web 组件前端，并使用 OpenGL 进行渲染。配置文件可以作为 JSON 导入和导出，如果需要，可以很容易地链接到其他工具。有益的是，该工具似乎还支持某种版本控制，尽管我们还没有尝试过。该过程非常简单，只需定义几个组(这些组与组件中的单个 PCB 或其他浮动项目相关)，每个组包含一个或多个连接器。首先，在定义显示哪些信号和物理引脚连接在一起的连接(导线)列表之前，用零件号和线规数据描述连接器。没有比这更复杂的了。我们认为该工具还可以管理更多的功能，例如屏蔽和保护细节、双绞线定义和其他一些功能，但对于第一次使用，wirely 看起来非常方便。

如果你想要一个更重量级的选项，使用 [IEC 60617 符号](https://std.iec.ch/iec60617)来描述线束，那么[只需要看看 QElectroTech](https://hackaday.com/2018/05/09/qelectrotech-an-open-source-wiring-diagram-tool/) 就可以了，是的，我们在之前已经有了[覆盖的 wireviz，只是为了那些想要省去中间人，直接用 Python 描述他们的电缆的人。](https://hackaday.com/2020/06/23/an-open-source-tool-to-document-your-wiring/)