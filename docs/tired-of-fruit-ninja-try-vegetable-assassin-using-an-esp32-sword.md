# 厌倦了水果忍者？尝试使用 ESP32 剑的蔬菜刺客

> 原文：<https://hackaday.com/2020/04/25/tired-of-fruit-ninja-try-vegetable-assassin-using-an-esp32-sword/>

在一个忍者不再统治社会等级的世界里，一个忍者崇拜者可以在哪里练习他们的剑术？在麻省理工学院广受欢迎的嵌入式系统入门课上，一组学生制作了他们自己版本的流行手机游戏水果忍者，并做了一些改动——你正在与你真正的敌人蔬菜作战。

[蔬菜刺客](http://vegetableassass.in/documentation/)允许单人或多人模式，玩家使用装有传感器的假剑在屏幕上切菜，传感器可以检测玩家的动作。基于网络的游戏允许剑通过与服务器的网络套接字连接向游戏会话传达它们的方位，游戏使用 3D 客户端 JavaScript 库生成和渲染。WebSocket 提供了最大的浏览器支持，而不是使用 MQTT，MQTT 也使用持久的 TCP 连接和较低的开销。

 [![vegetable-assassin-Front_of_Sword](img/b30210a1fb3ad379001a3e45dce50d29.png "vegetable-assassin-Front_of_Sword")](https://hackaday.com/2020/04/25/tired-of-fruit-ninja-try-vegetable-assassin-using-an-esp32-sword/vegetable-assassin-front_of_sword-2/)  [![singleplayer-vegetable-assassin](img/36bb077286d5350c114139a2c7290aed.png "singleplayer-vegetable-assassin")](https://hackaday.com/2020/04/25/tired-of-fruit-ninja-try-vegetable-assassin-using-an-esp32-sword/singleplayer-vegetable-assassin/) 

板载 ESP32 微控制器和 IMU 跟踪剑的运动。游戏从校准游戏区域内的剑的运动开始。使用 Madgwick 算法生成信息，这是一种 9 自由度算法，使用来自剑的陀螺仪、加速度计和磁力计的 3 轴数据，并输出剑的绝对方向。

剑和浏览器都通过 WebSocket 连接连接到服务器上的同一个通道，由会话 ID 标识，类似于网络聊天室的实现方式。统计服务器管理会话 id 和其他持久游戏数据的分配，以跟踪高分。

至于图形，Three.js WebGL 库创建场景和摄像机，将游戏加载到浏览器的动画帧中。其他脚本加载游戏中水果和蔬菜的 3D 模型，根据 Cannon.js 提供的物理引擎更新它们的位置，并在游戏中渲染 UI 元素。

好奇？项目网站有[微控制器代码](http://vegetableassass.in/microcontroller/)来建造你自己的剑，你可以用它来[玩演示](http://vegetableassass.in/#intro)。如果你手边没有 ESP32 和加速度计，你可以用[在你的浏览器里玩蔬菜杀手来代替](https://johnnybui.com/vegetable-assassin/)。