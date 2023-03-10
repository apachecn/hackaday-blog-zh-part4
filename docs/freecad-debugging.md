# FreeCAD 调试

> 原文：<https://hackaday.com/2020/11/16/freecad-debugging/>

强大的软件程序通常有你可以使用的宏编程语言，如果你知道如何编程，你可能会欣赏它们。然而，有时程序的内置调试工具是缺乏的，甚至是不存在的。如果只是语言，那就不是问题了，但是你不能只是从微软 Word 中抓取一个 VBA 宏，然后在普通的 Basic 解释器中运行它。您的程序将依赖于 Word 及其支持库提供的各种工具。[CrazyRobMiles]在尝试调试运行在 FreeCAD 中的 Python 时感到沮丧，所以他决定[对此做点什么](https://github.com/CrazyRobMiles/FreeCADSimulator)。

[Rob 的]简单的库 FakeFreeCad 提供了足够的支持，可以在普通的 Python 开发环境中运行 FreeCad 脚本。它只提供了您正在绘制的内容的粗略视图，但是它允许您探索宏的流程、检查变量等等。

您可以在 GitHub 页面上阅读更多相关内容，但本质上，您将 Python 代码包装到一个函数中，导入 FakeFreeCAD，然后添加一点样板代码并调用该函数。下面是一个测试函数的部分示例:

```

from FakeFreeCad import *

### code from FreeCad starts here
### Make it into a function that can be called to make the part

def makePlate():

   plate = Part.makeBox(800,600,100)
   hole = Part.makeCylinder(200,200,Base.Vector(400,300,0))
   plate = plate.cut(hole)

   Part.show(plate)
   Gui.SendMsgToActiveView(&quot;ViewFit&quot;)
   Gui.activeDocument().activeView().viewAxometric()

### End of the FreeCad code

```

您必须仔细研究代码，看看有多少东西是受支持的，但是添加任何缺少的东西可能很容易。当然，在 FreeCAD 中有调试支持会更好，但是这是一个非常方便的方法。

FreeCAD 在最近几年变得更好了。我们已经看到了很多关于它的参数化能力的讨论。如果你想要[的基础教程](https://hackaday.com/2014/02/05/3d-printering-making-a-thing-in-freecad-part-i/)，我们也有。