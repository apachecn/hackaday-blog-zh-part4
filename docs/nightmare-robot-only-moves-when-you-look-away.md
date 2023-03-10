# 噩梦机器人只有在你看向别处的时候才会动

> 原文：<https://hackaday.com/2020/10/29/nightmare-robot-only-moves-when-you-look-away/>

还有什么比鬼魂、妖精或小丑更可怕的呢？在你卧室的地板上放一堆不成形的恐惧怎么样，它只会在你不看它的时候动。这就是[【science sh】的噩梦机器人](https://www.youtube.com/watch?v=HtD9XxNFDxI)背后的想法，它潜伏在休息之后。《我的世界》蜘蛛装只是万圣节服装。

在这种情况下，“看着它”等同于你用手电筒照着它，试图找出衣服堆下面有什么。但问题是——当光线照在它身上时，它不会动。它很快就能判断出光源的方向，并伺机而动。当你放弃并关掉手电筒后，它会转到有光的地方，并开始向那个方向移动。

这个操作的大脑是一个 Arduino Uno，四个光敏电阻，和一点点三角学来寻找光源的方向。机器人本身使用两个步进器和印刷的人字齿轮来移动。它的底盘上有孔，可以接受细丝或电线来制作一个有两个目的的笼子——它使机器人在衣服下变成更多的无定形团块，并有助于防止衣服在轮子中缠绕。休息后看看演示并制作视频，因为这东西很快，完全令人毛骨悚然。

虽然我们通常会在每个万圣节看到一两台糖果分发机，但今年更多的是远程递送系统。不要把装满有趣大小的糖果的三明治袋子放在你的门廊上，而是建造一个糖果大炮或者 T2 一个怪异的滑梯。

 [https://www.youtube.com/embed/HtD9XxNFDxI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HtD9XxNFDxI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



通过 [r/duino](https://www.reddit.com/r/arduino/comments/jhtf1a/i_made_a_robot_that_can_sense_the_angle_of_a/)