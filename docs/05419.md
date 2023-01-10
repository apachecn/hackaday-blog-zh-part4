# Scorigami 机器人图表 NFL 的历史在制作中

> 原文：<https://hackaday.com/2020/01/22/scorigami-bot-charts-nfl-history-in-the-making/>

对于那些生活在美国大陆边界之外的人来说，NFL 足球是一项奇怪的运动。它的规则又多又复杂，它的计分系统是建立在奥术魔法之上的。这个系统意味着有许多*种可能的*场比赛最终比分实际上从未发生过。对于渴望听到任何第一时间比分的粉丝来说， [Scorigami bot](https://twitter.com/nfl_scorigami?lang=en) 在这里提供帮助。

[对这些进行制图和研究是 Scorigami](https://nflscorigami.com/) 的做法，这个想法首先由乔恩·博伊斯[提出，并在这个 SB Nation 视频中进行了探讨。](https://youtu.be/9l5C8cGMueY)它涵盖了 NFL 中许多*不可能的*比分，如 1-0 和 1-1，以及*可能但极不可能的*，如 6-1。跟踪斯科拉里的状态意味着跟踪每场 NFL 比赛的每一分。“机器人”使这变得更容易；用一些漂亮的 Javascript 抓取 NFL livescores 页面，它跟踪每场比赛的直播，寻找潜在的首次得分；最近一次是酋长队以 51-31 击败德克萨斯队。不仅如此，这个机器人还会估计正在进行的比赛中最有可能出现的比分，让球迷们一直提心吊胆，直到终场哨声吹响。还是 NFL 里的警笛？好奇的头脑需要知道。

如果你想独立审计 Twitter feed，自然可以在 Github 上找到代码；显然，scorigami 结果的神圣性是绝对重要的，确保这一点是社区的责任。我们以前见过其他现场评分项目，[像这个发光的超级碗足球。](https://hackaday.com/2015/02/04/super-bowl-football-lamp-keeps-you-informed/)