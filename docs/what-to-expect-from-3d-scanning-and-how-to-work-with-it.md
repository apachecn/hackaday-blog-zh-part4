# 对 3D 扫描有什么期望，以及如何使用它

> 原文：<https://hackaday.com/2021/04/20/what-to-expect-from-3d-scanning-and-how-to-work-with-it/>

3D 扫描和 3D 打印听起来似乎是天生的一对，但它们并不总是像人们希望的那样容易和完美地结合在一起。我将通过强调普通黑客会遇到的三个用例，以及它们工作得(或不工作)有多好，来解释人们可以期待什么。这样，您将更好地了解 3D 扫描如何满足您的零件设计和 3D 打印需求。

## 有些东西(不)工作得多好

大多数 3D 打印爱好者迟早会对 3D 扫描是否能让他们的生活和项目变得更容易感兴趣。这里是 3D 扫描、3D 打印和 CAD 的三个不同的交叉领域，并简单介绍了每个领域的工作情况。

| 目标 | 示例和细节 | 有用吗？ |
| --- | --- | --- |
| 使用扫描制作对象的副本。 | 

*   Scan something in 3D, and then print a copy in 3D.
*   Objects may be functional things, such as fixtures or appliance parts, or artistic objects, such as sculptures.

 | 大部分是，但取决于对象 |
| 从源对象制作 CAD 模型。 | 

*   The target is a 1:1 model, which is used for parts engineering purposes.
*   3D scanning instead of creating objects in CAD.

 | 不见得 |
| 数字化不方便或麻烦的形状。 | 

*   Get accurate models of complex shapes that cannot be easily measured or modeled in any other way.
*   Examples: dashboard, sculpture, large objects, objects attached to other things or unable to move easily, body parts such as head or face, objects with many curves.
*   Helps ensure that 3D printed objects will fit in or on other things.
*   Creating CAD models of parts for engineering purposes is not the goal.

 | 是的，但这要看情况 |

在所有这些情况下，人们想要一个物体的 3D 模型，而这正是 3D 扫描所创造的，那么问题是什么呢？问题是，并不是所有的 3D 模型都是相似的，对同样的事情都有用。

## 3D 扫描制作网格，而不是 CAD 模型

概括地说，有两种 3D 模型:CAD 模型和网格。这些可以被认为分别用于工程目的和艺术目的。一些读者可能会认为这是一种令人反感的过于简化，但它有助于说明 3D 扫描、3D 打印和 CAD 工作如何协同工作。

设计零件的黑客通常对 CAD 模型最感兴趣，因为这些模型代表了根据真实世界的测量值进行修改的真实世界的对象。但是 3D 扫描不会创建 CAD 模型；它将创建一个网格。

[![](img/48c028aad67ed910764a25ac0171efeb.png)](https://hackaday.com/2021/04/20/what-to-expect-from-3d-scanning-and-how-to-work-with-it/small-cad-model-editing-anim/)

Typical CAD model editing example, showing a model as a solid object, altered in terms of geometric features and real-world measurements.

[![](img/a66e9a189881350128efcb884bf045e7.png)](https://hackaday.com/2021/04/20/what-to-expect-from-3d-scanning-and-how-to-work-with-it/small-mesh-model-editing-anim/)

A typical mesh editing operation. The object is a network of points connected into a mesh, which can be manipulated and deformed.

网格*可以用于工程目的——`.stl`文件毕竟是网格，实际上与 3D 打印同义——但是网格不能像 CAD 文件那样被修改。使用网格时，不会将面挤出特定的毫米数，也不会将拐角圆角化到特定的半径。网格是绝对可以修改的，只是工具和流程不同。*

 *综上所述:3D 扫描从现实世界的物体中制作 3D 模型，但是在没有额外工作的情况下，扫描过程中得到的模型不一定适合工程目的。

## 家庭黑客的选择

在本文的开始，我选择了 3D 扫描、3D 打印和 CAD 工作的三个典型交叉点来说明它们之间的各种不完美匹配。现在，我将更详细地介绍这三个用例，并为普通黑客提供使用 3D 扫描来简化项目的方法。

### 使用 3D 扫描创建副本

摄影测量是一种创建 3D 模型的便捷方式，有免费和付费两种选择。通常，对象越小越复杂，就越难获得保留所有特征和细节的结果。

摄影测量使用从各种不同角度拍摄的物体的多张照片，软件解释这些照片以创建表示物体表面的点云。然后可以生成表示物体的网格 3D 模型。通常需要对模型进行一些清理或后处理，具体取决于方法和软件。

### 从 3D 扫描创建 CAD 模型

由于 3D 扫描不会生成 CAD 模型，因此它不是在 CAD 中设计零件的直接替代方法。大多数 CAD 程序都允许导入网格，但导入的网格仍然是网格，不能像其他 CAD 对象一样进行修改。然而，它可能对新设计有所帮助。

[![](img/676dbb3ddbb41b2d25e1a4020044edaa.png)](https://hackaday.com/wp-content/uploads/2021/04/Mesh-to-solid-anim-optimized.gif)

A mesh converted to a solid will become an object made up of collection of triangular faces, identical to the ones that made up the original mesh. This is rarely what a novice CAD modeler expects.

人们可能想知道是否有可能从一种格式转换成另一种格式。的确如此，但这种转变可能不是人们所期望的。将 CAD 模型转换成网格非常简单，但是将网格转换成 CAD 实体就不那么简单了。

如果一个网格不是太复杂，它可以被转换成一个实体([这里有一种方法可以通过使用 MeshLab 和 FreeCAD](https://hackaday.io/project/12043-convert-a-polygon-mesh-to-a-solid-body-for-free) )但是它仍然不是一个“普通的”CAD 对象，这里的图像演示了为什么。

如果您的目标是使用 3D 扫描使 CAD 模型的创建更容易，并且此处显示的转换结果不能达到目的，那么下一个最好的方法是使用 3D 扫描作为主扫描，并使用导入的网格作为指导，在其周围建模一个新的零件来匹配。使用这种方法的一个项目是[这个定制轨迹球是围绕一个模制的人体工程学原型](https://hackaday.com/2017/05/24/only-90s-kids-will-appreciate-this-prototype/)设计的。

一些专业软件套件能够导出到 CAD，但基本工作流程是相同的，扫描的网格被用作新设计的参考。

### 3D 扫描数字化不方便或麻烦的形状

[![](img/83bbf07086fafc320571b5ed0bea3e9a.png)](https://hackaday.com/wp-content/uploads/2021/04/Making-a-Control-Panel-Mount-for-my-Laser-Cutter-using-Photogrammetry-5-5-screenshot.png)

This scan of a laser cutter’s panel is obviously only part of the whole machine, but the important part is present.

有时需要形状的精确 3D 模型，而该形状不容易用手建模或测量。前面提到的摄影测量工具在这里也很有用，但是它们的目的不同。通常只需要对象的一部分，而不是从上到下对对象建模来制作精确的副本。

例如，模拟设备面板或仪表板的形状只需要成功扫描相关部分。一个人的头部可以被扫描，以确保头盔或面具的精确配合，没有必要对整个身体进行全面扫描。一般来说，需要的图片更少，后处理和模型清理更容易，因为感兴趣的区域更小。为了以后的缩放，必须以某种方式包括尺寸参考，因为大多数 3D 扫描本质上并不创建 1:1 的模型。

这种方法的一个很好的例子是[这个项目设计了一个定制的控制面板](https://hackaday.com/2019/12/26/custom-control-panels-with-photogrammetry/)用来安装现有的设备。不像扫描整个物体的目的是复制它，没有必要捕捉难以到达的地方，如底部或背部。这使得扫描和模型清理更加容易。

## 专业扫描

另一个选择是付费进行专业扫描。价值数千或数万美元、针对工程应用的花哨扫描仪和软件套件是存在的，尽管它们超出了一般黑客的能力范围，但花钱请一家公司做一两次扫描可能就不行了。

精度和分辨率可能超出摄影测量的能力，一些专业软件套件具有奇特的功能，如对齐多次扫描、精确的尺寸参考或根据扫描结果生成 CAD 模型的能力。

[![](img/a2774b0e727c51961d0c05781cac3b7b.png)](https://hackaday.com/wp-content/uploads/2021/04/P.08-Grip-3D-Scan-e1618202516271.png)

A 1:1 model from a professional 3D scanning tool, the product of aligning and merging multiple separate scans from different angles to get a complete model. It is still a mesh, but it accurately represents the original in both features and scale.

根据我的发票，这里显示的是我用 [Creaform HandySCAN Black 3D](https://www.creaform3d.com/en/portable-3d-scanner-handyscan-3d) 扫描仪专业扫描的零件模型。这是一把古董火器的旧木柄。扫描仍然创建了一个网格，但它是原物的精确 1:1 模型，我可以用它在 SLA 3D 打印机上打印替换物。

当获得专业 3D 扫描的报价时，一定要询问费用结构，并明确自己的需求。在我的案例中，在一次安装费用下扫描多个相似的物体是划算的。

## 了解 3D 扫描可以(和不可以)做什么

3D 扫描一直在变得越来越好，越来越容易获得，但它生成网格的事实意味着它并不总是能够顺利地适应 3D 打印和 CAD 零件设计工作流程。这并不意味着它没有用处，但它确实意味着了解其局限性以及它们将如何影响您的需求非常重要。

当然，人们总是可以找出卡尺并在 CAD 中手动建模一个零件，但并不是所有的零件和形状都容易测量或逆向工程。对于手工创建不切实际或容易出错的复杂现实世界对象，3D 扫描是一种很好的替代方法。

您是否成功地使用 3D 扫描来简化项目，或者有喜欢的方法或工具可以分享？我们很想知道所有的事情，所以请花点时间在评论中与我们分享。*