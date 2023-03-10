# 优化从煤灰和海水中开采铀

> 原文：<https://hackaday.com/2022/08/23/optimizing-the-mining-of-uranium-from-coal-ash-and-seawater/>

在构成地壳的所有元素中，[铀](https://en.wikipedia.org/wiki/Uranium)相对而言[丰富](https://en.wikipedia.org/wiki/Abundance_of_elements_in_Earth%27s_crust)，排在第 49 位，领先于锡、钨和银等元素。自从人类开始利用铀在能源生产中的裂变特性以来，这种丰富也转化为广泛的[采矿](https://world-nuclear.org/information-library/nuclear-fuel-cycle/mining-of-uranium/uranium-mining-overview.aspx)。截至 2019 年，哈萨克斯坦、加拿大和澳大利亚组成了世界主要生产国，约占产量的 68%。

考虑到铀在核裂变反应堆中用作燃料时的巨大能量密度，对铀的需求相对较低，特别是与商用反应堆的长(平均两年)换料周期相结合。其结果是，即使是效率非常低的直流燃料循环——只利用了铀燃料潜在能量的一小部分——铀市场价格仍然相对较低且稳定，即使在地缘政治危机中也是如此。

尽管如此，铀市场价格的逐渐上涨(2003 年为 10 美元/磅，2022 年为 49 美元/磅)，以及新反应堆的快速建设正在推动新的勘探。在这方面，最近的创新可能会使铀燃料更容易为所有国家所用，这是通过释放在普通海水中发现的数十亿吨铀以及燃煤电厂每天产生的数吨飞灰实现的。

## 这是经济，傻瓜

[![Effect of uranium price on fuel cost (source: World Nuclear Association)](img/fd8a6555d1fe7136ec7dea94a94a76ba.png)](https://hackaday.com/wp-content/uploads/2022/08/effect_of_uranium_price_1.png.png)

Effect of uranium price on fuel cost (source: World Nuclear Association)

大多数核电厂运营商选择只使用一小部分可裂变铀 235 的单程燃料循环的主要原因是，核电厂的燃料成本低得令人难以置信。虽然一个新的 GW 级核电厂的前期成本相当可观，但其 40-100 年寿命的运营成本非常低，这就是后处理乏燃料以去除新形成的锕系元素和超铀元素的额外成本几乎没有[经济意义](https://world-nuclear.org/information-library/economic-aspects/economics-of-nuclear-power.aspx)。

这种经济角度也是导致发展[快中子反应堆](https://hackaday.com/2019/10/08/the-long-history-of-fast-reactors-and-the-promise-of-a-closed-fuel-cycle/) (FNRs)缺乏吸引力的因素之一。虽然这些 fnr 可以通过中子俘获从肥沃的同位素中培育出自己的燃料，但它们比轻水反应堆更复杂、更昂贵——实际上是今天运行的所有商业核电站。这些因素都在某些铀资源从地下或其他来源提取是否经济的问题上发挥作用，同时也很明显为什么以前从粉煤灰和海水中提取铀不经济。

尽管地球的海洋中估计含有 46 亿吨铀，但将其稀释到这些广阔的水域中意味着你必须过滤掉一种十亿分之几个分子的物质。同样，对于粉煤灰，必须以一种足以与现有采矿方法竞争的有效方式将铀与粉煤灰中的其他成分分离，如原地浸出( [ISL](https://en.wikipedia.org/wiki/In_situ_leach) )。

然而，从海水和粉煤灰中提取铀的另一个潜在好处是，它可以完全避免传统采矿对环境的影响，同时可能有助于解决粉煤灰造成的环境危害。

## 煤炭浪费问题

[![](img/e412d7f48dde667c96c1798543ca61f4.png)](https://hackaday.com/wp-content/uploads/2021/04/kingston_Aerial_view_of_ash_slide_site_Dec_23_2008_TVA.gov_123002.jpg)

Aerial photograph of the Kingston Fossil Plant coal fly ash spill.

[煤灰](https://en.wikipedia.org/wiki/Fly_ash)由留在锅炉底部的灰和细灰或飞灰组成，细灰或飞灰由安装在燃煤电厂烟囱内或附近的静电除尘器或类似设备收集。它含有一些剩余的碳，以及大量的二氧化硅、氧化铝和氧化钙。此外，它还含有许多重金属和类似问题物质的微量元素，包括砷、镉、六价铬、铅和汞。

寻找一种回收或处理粉煤灰的方法已经成为一个越来越成问题的话题，特别是现在粉煤灰通常不再释放到大气中，而是储存在巨大的煤灰池中。这些池塘形成了一个潜在的危险，正如 2008 年金斯敦化石燃料厂泥浆泄漏事件所示，420 万立方米(11 亿美国加仑)的粉煤灰与水混合进入邻近的埃默里河。随后的清理工作导致大约 40 名工人因接触有害化学物质而丧生。

虽然粉煤灰越来越多地被混合到从混凝土到柏油路面和牙膏的所有东西中，但产生的数量意味着仅在美国，每年由燃煤电厂产生的大约 34.7×10 ⁶ 吨粉煤灰中的很大一部分最终被填埋。开采飞灰中的铀等有用元素可能有助于减少其总体积，同时可能使剩余材料的利用更容易。

[![Yellowcake, also called urania.](img/772fc5cf708d0f661b6b91030bfce585.png)](https://hackaday.com/wp-content/uploads/2022/08/Yellowcake.jpg)

Yellowcake, also called urania.

早在 2007 年，加拿大 Sparton Resources】就报道过用中国一家燃煤电厂的飞灰生产[黄饼](https://en.wikipedia.org/wiki/Yellowcake)(主要是 U [3] O [8] )。铀含量约为 160 ppm，相当于一吨灰烬中约 0.2 千克的黄饼。正如《经济学人》在 2010 年的一篇文章中指出的，相比之下，铀矿石中的含量为 1,000 ppm 或更多。使用硫酸和盐酸的过程类似于原地浸出，然后铀和其他溶解的元素被过滤掉，并用碳酸铵沉淀。

在 2010 年的那个时候，Sparton 声称能够以 77 美元的价格提取一公斤铀，而当时铀现货市场的价格是 90 美元。关于这个话题的大部分 R&D 似乎发生在中国，在那里它被认为是铀燃料的一个可行来源，特别是考虑到中国已经计划或正在建造的一百多个新的核反应堆，以及它对自力更生的关注。

[孙等(2016)](https://www.sciencedirect.com/science/article/pii/S1878029616000979) 描述了从底灰中提取铀，以及高含锗煤燃烧后剩余的底灰中铀的高浓度(374 mg/kg)。虽然从 CFA 中开采的铀还不是一个大产业，但正在进行的研究和所述的小规模试验表明了这种方法的可行性。

## 开采海洋

将铀从海水中过滤出来的概念很简单:本质上就是将尽可能多的水通过过滤系统，保留我们感兴趣的元素，之后铀酰分子可以进一步加工成反应堆燃料。事情变得棘手的地方是，虽然海洋中含有比陆地多几百倍的容易获得的铀，但十亿分之几个粒子(ppb)的低密度使得有一种高效的过滤方法至关重要。

正如[在 2017 年斯坦福大学的一篇文章中指出的](https://engineering.stanford.edu/magazine/article/how-extract-uranium-seawater-nuclear-power)，当时使用的方法包括将含有一种叫做[偕胺肟](https://en.wikipedia.org/wiki/Oxime)的化合物的塑料纤维粘在水中，等待纤维被铀酰饱和，然后可以进行处理。2018 年，PNNL [报道](https://www.pnnl.gov/news/release.aspx?id=4514)用这种方法从海水中回收了整整一克黄饼。

在去年发表在*《自然》*、[杨等人(2021)](https://www.nature.com/articles/s41893-021-00792-6) 的一项研究中，展示了一种替代方法，其中海水被引导通过分级多孔膜，这与肺或血管的分支网络没有什么不同。通过用偕胺肟涂覆这样形成的通道的内部，并迫使含铀的水通过它们，他们证明了比以前的尝试显著提高的提取率，这主要是由于表面积的大幅增加，以及穿过偕胺肟涂覆的材料的水流量的增加。

一旦达到饱和状态，铀就可以用盐酸溶解，按照通常的处理方法转化为反应堆的燃料。如此清洗过的膜可以重复使用多次，这使它成为一种潜在的经济选择，也是一种提取铀的方法，满足任何有海水或海水的国家的需求。

## 不会很快用完

随着许多最好的石油、煤炭和天然气田被开采到枯竭的程度，化石燃料的产量开始大幅下降。与化石燃料不同，仅使用铀作为燃料的裂变反应堆可以以目前的能源水平维持人类社会数千年，即使没有对乏燃料后处理或快中子反应堆的大量投资。也许更吸引人的是，它将清理燃煤电厂产生的有毒废物作为这一转变的一个特征。

除了从粉煤灰中提取铀，一些研究人员正试图确定稀土元素是否也能从这些粉煤灰中经济地回收。以这种方式，昨天的污染可能会以讽刺的方式帮助未来的发展。

横幅图片:[PNNL 的钱伟举着一小瓶从海水中回收的 5 克黄饼](https://www.pnnl.gov/news/release.aspx?id=4514)。