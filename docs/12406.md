# 生产 PCB 和弹簧针产生一个聪明的测试夹具

> 原文：<https://hackaday.com/2022/01/07/production-pcb-and-pogo-pins-produce-a-clever-test-jig/>

[Hans Summers]在 qrp-labs.com 经营一个站点，销售主要用于无线电设备和 GPS 应用的自组装套件，并且他的 QCX-迷你 QRP 收发器套件存在一些生产问题。在疫情期间，他们使用的装配车间的一个分包商出现了一些问题，更换服务的质量略低于预期水平，导致大量 SMT 组装电路板无法正常工作。显然，他们不想将这些作为调试问题传递给客户，所以他们着手于内部 QA 测试夹具，以给他们再次发布套件的信心。[产生的功能测试夹具](https://www.youtube.com/watch?v=xb_ZmPx7Py4)(视频，嵌入在下面)采用了一种相当有趣的方法。[跳过视频到 9:00](https://youtu.be/xb_ZmPx7Py4?t=548) 了解测试夹具的描述和详细的测试描述。

通过采用现有的已知良好的 PCB，剥离所有 SMT 部件，并将通孔元件移到 PCB 背面，pogo 引脚可以焊接到关键位置。将组件构建到一个由锯成的原始覆铜板制成的基本外壳中，弹簧朝上，顶部有一个简单的夹具，允许被测 PCB(从现在开始称之为 [UUT](https://en.wikipedia.org/wiki/Device_under_test) )被定位并夹紧到位。这压缩了弹簧以形成牢固的电接触。一块用 dremel 处理过的 MDF 起到了压板的作用，SMT 元件区域周围有切口，以实现所需的均匀电路板压力，并使压力远离脆弱的焊接部件。所有这些意味着，如果 UUT 通过弹簧针连接到只有通孔的测试 PCB，当且仅当 UUT 完全正常工作时，整个电路才完整，这意味着无缺陷焊接和无缺陷元件。

接下来，固件被重写以履行测试控制器的职责，当通电时，它将逐步完成一系列测试场景和测量，将结果记录到有机发光二极管显示器和串行接口。该设备经受住了 1，000 次 SMT 测试，没有出现故障，这让[Hans]有信心推出新套件，并提供 datalog 结果数据库作为备份，以防客户在最终组装过程中出现问题。在没有定制测试夹具 PCB 的情况下，这是一个解决难题的聪明主意！

多年来，这些页面被许多基于 pogo 的测试平台增色不少。这里有一个[开始](https://hackaday.com/2020/05/31/building-one-test-fixture-to-rule-them-all/)，如果你有一个方便的激光切割机和一些废木头，制作一个精确的[测试台也不麻烦](https://hackaday.com/2019/06/25/laser-cutting-wooden-pogo-pin-test-jigs/)。

 [https://www.youtube.com/embed/xb_ZmPx7Py4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xb_ZmPx7Py4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[Paul]的提示！