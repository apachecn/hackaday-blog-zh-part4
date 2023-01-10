# 用于无刷电机的可堆叠 3D 打印齿轮箱

> 原文：<https://hackaday.com/2022/07/24/stackable-3d-printed-gearbox-for-brushless-motor/>

经济实惠的无刷电机非常适合各种运动应用，但通常需要变速箱来控制速度。[Michael Rechtin]决定尝试为无刷电机设计一个[可堆叠行星齿轮箱](https://www.youtube.com/watch?v=G0DcM60lWSw)，允许他添加或删除阶段以改变传动比。

变速箱是围绕亚马逊的一个便宜的 5010 尺寸、360 [KV](https://www.rotordronepro.com/understanding-kv-ratings/) 无传感器电机设计的。每一级由一个 1:4 的行星齿轮组组成，该齿轮组可以连接到另一级或输出轮毂上。这意味着每增加一级，输出速度就会降低四分之一。由于高压角、直切齿和相当宽松的间隙，变速箱噪音很大。

为了测量扭矩，[迈克尔]将电机-变速箱组合安装到一块铝挤压件上，并添加了一个 100 毫米的力臂，以向测压元件施加力。第一次测试居然把力矩臂弄坏了，于是设计打印了一个加强版。电机能够通过变速箱施加大约 9.5 牛米的扭矩。这个数字可能不准确，因为像这样的无传感器电机不能在低速时提供平稳的输出力。正如[Michael]所建议的，增加一个传感器和编码器将允许更好的测试和低速应用。休息后看看视频。

我们以前展示过一些[迈克尔]的项目，包括一个[袋子跟踪玉米洞板](https://hackaday.com/2020/07/09/robotic-cornhole-board-does-the-electric-slide/)，和一个 [3D 打印线性致动器](https://hackaday.com/2022/05/18/3d-printed-linear-actuator-is-cheap-and-strong/)。

 [https://www.youtube.com/embed/G0DcM60lWSw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G0DcM60lWSw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

