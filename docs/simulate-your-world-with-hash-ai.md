# 用 Hash.ai 模拟你的世界

> 原文：<https://hackaday.com/2020/06/21/simulate-your-world-with-hash-ai/>

我们承认，我们经常将真实世界的软件模拟放在一起，但我们也承认它们通常很快而且很脏，只是将我们可能在电子表格中或使用 GNUPlot 绘制的文本转储出来。但是有了 [Hash.ai](https://hash.ai/) ，你可以快速轻松地生成几乎任何东西的模拟。模拟也将有漂亮的可视化和图表。该工具支持 JavaScript 或 Python，您不必浪费时间编写不变的部分。

这个基于网络的工具基于代理的思想。每个代理都有一个或多个在每个时间步运行的行为。在模拟森林野火的示例中，代理名为 forest，尽管它实际上模拟的是一棵虚拟的树。还有一种行为叫做森林，它根据附近的树木和闪电来控制树木的生长速度和燃烧的几率。其他行为模拟燃烧的树以及树燃烧后会发生什么——灰烬——它可能会也可能不会再长回来。

在这个特定的模拟中，对`create_scatters`的调用填充了大量的森林代理。之后，模拟会一直运行，直到您停止它。除了设置颜色和尺寸，可视化不需要你做太多的工作。例如，下面是一个灰烬的代码:

```

/**
* This behavior causes the agent to change from an ember
* back to a growing tree.
*/
function behavior(state, context) {
const { emberColor, emberHeight, regrowthChance } = context.globals();

// Get neighbors that are "trees";
const forestNeighbors = context.neighbors()
.filter(({behaviors}) => behaviors.includes("forest.js"));
// Turn back into a tree, with a linear increase
// in likelihood with # of neighbors
const modRegrowthChance = regrowthChance * (forestNeighbors.length + 1);
if (modRegrowthChance > Math.random()) {
let behaviors = state.get("behaviors");

// Replace the ember behavior with forest behavior
const index = behaviors.indexOf("ember.js");
behaviors[index] = "forest.js";

state.set("behaviors", behaviors)
}

// Set other needed properties for an &quot;ember&quot;
state.set("color", emberColor);
state.set("height", emberHeight);
state.set("age", 0);

return state;
};

```

你可以看到，如果附近有健康的树木，树木更有可能重新生长。你唯一需要为模拟设置的是颜色和高度。剩下的都是和你的问题域相关的状态逻辑。

还有其他例子，从蚂蚁觅食到降雨。然而，看起来你可以做任何数量的模拟，只要你能以离散的时间步骤描述代理和他们的状态。

这可以在很多应用中取代 Jupyter。我们想知道你是否可以在本地提取代码，并将其与 [LTSpice](https://hackaday.com/2019/11/30/circuit-simulation-in-python/) 集成，以进行一些电子模拟计算。