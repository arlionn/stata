[![2019暑期论文班-连玉君-江艇主讲](https://images.gitee.com/uploads/images/2019/0622/181932_47e8ffd6_1522177.jpeg)](https://gitee.com/arlionn/Course/blob/master/2019Papers.md)


---
## 1. 课程概要

- **时间：** 2019 年 8 月 17-23 日    
- **地点：** 西安，西北工业大学国际会议中心  ([百度地图](https://j.map.baidu.com/yXIiP) | [搜狗地图](http://map.sogou.com/u/MvmiOn))
- **主讲嘉宾**：
  - 连玉君 (中山大学，8 月 17-19 日，专题 T1-T6)
  - 江艇 (中国人民大学，8 月 21-23 日，专题 T7-T12)
- **授课内容：** 实证研究方法与经典论文 (9 篇) 重现
  - **课程要点：** 研究设计、稳健性检验、内生性问题及论文的写作。
  - **主要方法：** IV 估计、匹配 (Matching)、倍分法 (DID)、Matching+DID、双向固定效应模型、动态面板数据模型等
- **授课方式：** 
  - PPT + 电子板书
  - 每天 6 小时 (9:00-12:00；14:00-17:00)+半小时答疑
  - 讲义电子版于开课前一周发送；纸质讲义由主办方统一印制
  - 软件：Stata 15

##### 课程特色

1. **渔非鱼。** 体系完整，注重模型设定思路、研究设计和结果的解释。第 1-3 讲介绍研究设计和主要回归方法；第 4-12 讲深度解构 9 篇发表于 Top 期刊的经典论文的实现过程。[[课程中涉及的论文一览]](https://gitee.com/arlionn/stata_training/tree/master/PDF)
2. **电子板书。** 全程电子板书，听课更专注，复习更高效；【**下载**】[连玉君-FE-板书](https://gitee.com/arlionn/stata_training/raw/master/Stata%E6%9D%BF%E4%B9%A6/Stata%E6%9D%BF%E4%B9%A6-FE-version2.pdf)
3. **可重现。** 我们会提供重现论文所需的全套课件，包括 Do-files、范例数据、自编程序，课程中的估计方法和代码都可以快速移植到自己的论文中。【**下载**】[A1_intro.do](https://gitee.com/arlionn/stata_training/raw/master/dofile-data/A1_intro.pdf),  [A6_DID.do](https://gitee.com/arlionn/stata_training/raw/master/dofile-data/A6_DID.pdf)
4. **注重方法的合理搭配。**  基于每篇文章的重现，重点讲解如下几个论文写作中普遍面临但又非常棘手的问题：
   - 研究设计如何开展？
   - 稳健性检验包括哪些内容？主要有哪些方法和途径？
   - 内生性问题如何确认和解决？
   - 如何解读和表述实证结果？


     
---
## 2. 嘉宾简介

---
### 连玉君
![连玉君](https://images.gitee.com/uploads/images/2019/0622/181932_e0ada233_1522177.jpeg)   
**[连玉君](http://lingnan.sysu.edu.cn/node/151)** ，经济学博士，副教授，博士生导师。2007年7月毕业于西安交通大学金禾经济研究中心，现任教于中山大学岭南学院金融系。主讲课程为“金融计量”、“计量分析与Stata应用”、“实证金融”等。已在《China Economic Review》、《经济研究》、《管理世界》、《经济学(季刊)》、《金融研究》、《统计研究》等期刊发表论文60余篇。连玉君副教授主持国家自然科学基金项目（2项）、教育部人文社科基金项目、广东自然科学基金项目等课题项目10余项。目前已完成 Panel VAR、Panel Threshold、Two-tier Stochastic Frontier 等计量模型的 Stata 实现程序，并编写过几十个小程序，如 `xtbalance`, `winsor2`, `bdiff`, `hausmanxt`, `ttable3`, `hhi5`, `ua`等。连玉君老师团队一直积极分享Stata应用中的点点滴滴，开设了 [[Stata连享会-简书]](https://www.jianshu.com/u/69a30474ef33)，[[Stata连享会-知乎]](https://www.zhihu.com/people/arlionn) 两个专栏，并定期在微信公众号 (**StataChina**) 中发布精彩推文。

---
### 江艇
![江艇](https://images.gitee.com/uploads/images/2019/0622/181932_827c5d93_1522177.png)   
**江艇**，香港科技大学商学院经济学博士，中国人民大学经济学院副教授，人大国家发展与战略研究院研究员，人大微观数据与实证方法研究中心副主任，美国哥伦比亚大学商学院访问学者。主要研究领域为经济增长与发展、城市经济学、新政治经济学，在*Economics Letters*、*Review of Development Economics*、《经济研究》、《管理世界》、《世界经济》等国内外著名学术刊物上发表多篇论文，曾应邀在多所高校讲授“应用微观计量经济学”短期前沿课程并广受好评。 

&emsp;

---
## 3. 课程介绍

### 3.1 课程导引

在过去十多年中，学界发生了一场激烈的争论。争论的焦点在于：如何看待计量经济学？如何看待实证分析？如何看待我们的计量经济学教学？

大家讨论的基本结果是，我们的计量经济学教学模式需要一场革命性的改变！

在传统的计量经济学教学中，我们把太多的精力放在了假设检验和统计推断上，尤其是对于某个统计量的小样本和大样本性质的证明上。然而，对于如何将这些工具有效组合起来，合理运用它们来展开实证分析，多数的课程都不曾涉及。

例如，对于内生性的问题，传统的教科书会花大量的篇幅来介绍工具变量法、两阶段最小二乘法，以及更为复杂的 GMM 估计。虽然这些方法在目前的实证分析文献中仍然被广泛使用，但有过实证分析经验的同仁应该都有共识：工具变量法虽然理论完美，但现实却很骨感——**想找到一个干净的工具变量，其难度不亚于证明法海从未嫉妒过许仙！**

然而，若从因果推断这一目的出发，我们有更多更为简洁有效的估计方法。例如，只需借助 OLS，通过合理的研究设计，就可以使用 **倍分法 (DID)** 或 **断点回归 (RDD)** 等方法来解决政策评价中普遍存在的自选择偏误和样本选择偏差 —— 这是导致内生性问题的主要来源。

为此，在近两年的面授班中，我们都尽力抛开枯燥的公式推导，将重点放在研究设计、以及计量模型的设定和结果的解读上。由于授课内容都源自我在实证分析过程中亲身经历的实例，大家的听课效率大幅提高，听课后最大的收获在于知道该如何设定模型，如何选取变量，如何进行稳健性检验，如何处理内生性问题，如何分析实证结果又和表述研究贡献。这让我甚是欣慰。

对于已经开始尝试独立开展研究工作的学员而言，大家明显地感觉到，研究设计是最棘手的问题。在之前有导师指导或带领的情况下，研究主题和研究内容都是预先给定的。此时，完成一篇论文相当于在做一个命题作文，而一旦开始独立门户，最大的挑战是找到合适的研究主题，做一个可靠的研究设计。这其实也是实证分析工作中最难的部分。

在本次的学术论文班中，我们从研究设计入手，在介绍一些常用的计量方法和模型的基础上，精心挑选了 10 余篇发表于顶尖期刊（包括 AER，QJE，JHR 等）上的代表性论文，详细讲解每篇论文的实证分析过程，剖析作者的研究思路、研究设计、内生性问题的处理、稳健性检验，以及对结果的详细剖析。我们会提供重现每篇论文所需的所有数据和程序文件，以便保证各位可以在听课后反刍，并将这些论文中的分析方法迁移到你的研究中去。

精讲并重现经典论文，有如下**两方面的好处**：

**一方面**，这些论文的研究设计都非常出色，我们可以借鉴并在博采众长的基础上，不断改进自己的研究设计思路和方法。只有去拆解和重现这些论文，才能够感受到作者的思考过程和写作意图，从而从实质上提高我们自身的分析和研究能力。

**另一方面**，这些论文涵盖了目前实证分析中的主流方法，更为重要的是，每一篇论文通常会综合使用多种分析方法，这对于我们理解和灵活应用初级班和高级班所学的计量方法大有裨益。

**开课前的话**

需要特别强调的是，虽然论文班的学习并不要求扎实的计量基础，但却希望大家要足够努力。最基本的要求是，在开课之前，要认真的研读每一篇论文，了解其研究背景、研究思路、计量方法和主要结论。上课过程中，我们会随机抽取学员来回答一些问题。同时，也建议大家在开课前务必掌握文献的检索方法，学会使用百度学术、谷歌学术和 **Endnote** 等文献管理软件，这助于追踪我们讲解的每篇论文的后续进展，以便发掘新的研究主题。

虽然这些论文的研究主题与诸位所在领域可能会有比较大的差异，但是，大道至简，从这些论文中主要是学习计量方法的合理应用和研究设计的思想。


&emsp;

### 3.2 课程主题

>#### T1：研究设计基础：模型设定和解释
- **专题简介：** 很多人会觉 OLS 过于简单。可是，为何 Top 期刊中使用最多的仍然是 OLS？因为它是实证分析的基础。文献中广泛使用的 **固定效应模型 (FE)**，**长差分 (Long Difference)**，**倍分法 (DID)**，**断点回归分析 (RDD)**，都是 OLS 家族中的直系成员或亲属。这些模型得以衍生的基础是虚拟变量和交乘项。这是本专题重点讲解的内容：虚拟变量的使用、交叉项的使用和解释、分组回归的合理设定和假设检验。
- **授课内容**
  - 如何合理设定模型？
  - 虚拟变量
  - 稳健性标准误：异方差、序列相关和聚类调整标准误
  - 交叉项、平方项、调节效应和边际效应
  - 分组回归和组间系数差异检验


>#### T2：分析工具：面板数据模型
- **专题简介：** 由于面板资料的获取越来越方便，目前多数研究中使用的都是面板数据。在讲解这些模型的基本思想和估计方法的过程中，我会将重点放在模型含义和应用范围上来。例如，对于同一笔数据而言，何时采用 OLS 进行估计，何时采用 FE 估计？不同的方法之间有何差异和关联？结果背后的经济含义如何解读？动态面面板模型重点在于分析变量的动态变化和调整行为，在经济增长、公司金融、国际贸易、劳动经济学等领域都得到了广泛应用。
- **授课内容**
  - 固定效应模型 (FE) 
  - POLS、FE、RE 有何区别？
  - Hausman 检验、聚类调整稳健性标准误 (Cameron, 2015, JHR, [[PDF]]())
  - 实证分析中的常见问题
  - 一阶差分 GMM 估计量（FD-GMM）
  - 序列相关检验
  - 过度识别检验（Sargan检验）
  - 应用范例（介绍 2 篇论文）
    - Huang B N, Hwang M J, Yang C W. Causal relationship between energy consumption and GDP growth revisited: a dynamic panel data approach[J]. Ecological economics, 2008, 67(1): 41-54. [[PDF]]()
    - Horioka C Y, Wan J. The determinants of household saving in China: a dynamic panel analysis of provincial data[J]. Journal of Money, Credit and Banking, 2007, 39(8): 2077-2096. [[PDF]]()


>#### T3：统计推断方法：自抽样 (Bootstrap) 和蒙特卡洛模拟分析 (Monte Carlo Simulation)
- **专题简介：** 在近十年中，以随机抽样和模拟分析为基础的统计推断方法得到了广泛的应用，对于克服异方差、序列相关，以及干扰项分布形式未知等情形下的稳健性统计推断很有帮助。在面板门槛模型、面板 VAR 等模型中都需要借助 BS 或 MC 进行统计推断。可以预见，在日后的实证分析中，这两种方法将得到越来越广泛的应用。
- **授课内容**
  - 常用分布函数和随机数的产生
  - Bootstrap 简介
  - Boostrap 应用：获取稳健性标准误、组间系数差异检验
  - Monte Carlo 模拟简介
  - Monte Carlo 模拟范例 1：内生性偏误的影响 (IV 的选择、弱工具变量问题)
  - Monte Carlo 模拟范例 2：动态面板各种估计方法对比 (POLS, FE, FD-GMM, SYS-GMM)
- **参考文献：**
  - Davidson, R., 2007, Bootstrapping econometric models. Quantile, (3), 13–36.  [[PDF]](https://gitee.com/arlionn/stata_training/raw/master/PDF/Davidson_2007_BS.pdf)
  - Guan, W., 2003, From the help desk: Bootstrapped standard errors, Stata Journal, 3 (1): 71-80. [[PDF]](https://gitee.com/arlionn/stata_training/raw/master/PDF/Guan_bs_SJ3-1.pdf)
  - MacKinnon, J. G., 2006, Bootstrap methods in econometrics, Economic Record, 82: S2-S18. [[PDF]](https://gitee.com/arlionn/stata_training/raw/master/PDF/MacKinnon_2006-Bootstrap.pdf)
  - Wehrens, R., H. Putter, L. Buydens, 2000, The bootstrap: A tutorial, Chemometrics and Intelligent Laboratory Systems, 54 (1): 35-52. [[PDF]](https://gitee.com/arlionn/stata_training/raw/master/PDF/Wehrens-2000-The%20bootstrap_%20a%20tut.pdf)

>#### T4：如何讲故事？人口老龄化、机器人与经济增长 | Acemoglu and Restrepo (2017)
-  Acemoglu, D., P. Restrepo, **2017**, Secular stagnation? The effect of aging on economic growth in the age of automation, ***American Economic Review***, 107 (5): 174-179. [[PDF](https://gitee.com/arlionn/stata_training/raw/master/PDF/Acemoglu_2017_AER.pdf)]
- **论文简介：** 作者先呈现出一些简单的散点图和时间趋势图，提出问题：人口老龄化与经济增长的关系不是负相关，而是恰恰相反！为了解释这个有悖常识的现象，作者先做了几个简单的回归分析，包括普通线性回归、固定效应模型、工具变量法、长差分 (long-difference) 等，进而使用一个理论模型进行了更为严谨的推理。从行文上来看，与我们平时看到的论文结构刚好相反，但读起来却很顺畅，因为作者引领你走入丛林，发现秘密！
- **方法:**
  - OLS
  - 双向固定效应模型
  - IV 估计：工具变量的选择; 过度识别检验
  - 长差分 (long-difference)
- **亮点：**
  - **如何讲一个好故事？** 告诉你如何讲述一个有趣的故事，并用简单的回归方法给出令人信服的证据。
  - **精妙的研究设计**：全文只有三张图形和两张表格，但逻辑严密，工具的使用恰到好处。

>#### T5：稳健性检验如何做？ Flannery and Rangan(2006)
- Flannery, M. J., K. P. Rangan, **2006**, Partial adjustment toward target capital structures, ***Journal of Financial Economics***, 79 (3): 469-506. [[PDF]](https://gitee.com/arlionn/stata_training/raw/master/PDF/Flannery_2006.pdf)
- **论文简介：** 资本结构的动态调整行为并不是一个新的研究话题，但他一直在持续被讨论。这篇论文以权衡理论为基础，在部分调整模型架构下研究了美国上市公司资本结构的动态调整行为。作者发现，若不考虑公司的个体效应，则调整速度会被严重低估，为此，他们使用了固定效应模型 (**FE**)，估得的调整速度约为前期文献的三倍，达到 0.38。问题在于，这一结果可信吗？如果使用更为合理的 **FD-GMM** 进行估计，结果又将如何呢？作者通过一系列稳健性检验来证实其结果的可信性。
- **方法：** 
  - 混合 OLS (Pooled OLS)
  - Fama-MacBeth 估计 (FM method)
  - 固定效应模型 (FE)
  - 动态面板模型 (Dynamic Panel data)
  - 各种稳健性检验设计
- **亮点：** 
  - 实证分析过程值得借鉴，非常严谨的研究设计
  - 对**衡量偏误**、**均值回复**、不同理论的对比检验、模型设定等棘手问题的处理很巧妙
  - 该文引发了后续多个方向的研究，我们将梳理几个主要的方向，探求论文的选题和研究方向问题。

>#### T6：计数模型的应用：论文引用率如何提高？
- Di Vaio, G., D. Waldenstrom J. Weisdorf, Citation Success: Evidence from Economic Histopry Journals, Explorations in Economic History, 49 (1): 92-104. [[PDF]](https://gitee.com/arlionn/stata_training/raw/master/PDF/Di_Vaio_2012.pdf), [[PPT]](https://gitee.com/arlionn/stata_training/blob/master/PDF/Di_Vaio_2012.ppt)
- **论文简介：** 越来越多的研究开始关注离散型被解释变量，例如，论文发表数量、专利个数、违规违法次数、恐怖袭击事件数等。该文使用了泊松回归和负二项回归等方法，探究发表于经济史期刊上的论文引用率的影响因素。除了一些在预期之内的结论文 (如全职教授、长篇和合著论文的引用率更高)，作者还发现论文的二次传播 (如工作论文的发表，以及会议和研讨会的报告) 也对引用率有重要影响。这主要通过设定交叉项和三重交叉项来实现。
- **方法：** 
  - 泊松回归 (Poisson regression)
  - 负二项回归 (Negative binomial regression)
  - 调节效应 (交叉项、三重交叉项)
- **亮点：** 计数模型


>#### T7: 交互项模型中的工具变量方法
- Rajan, Raghura- G, and Luigi Zingales, 1998, “Financial Dependence and Growth.” *American Economic Review* 88(3): 559-86\. [[PDF](https://gitee.com/arlionn/stata_training/raw/master/PDF/Rajan_Zingales_1998_AER.pdf)]
- **论文简介：** [Rajan and Zingales (1998)](https://gitee.com/arlionn/stata_training/raw/master/PDF/Rajan_Zingales_1998_AER.pdf)  是交互项模型的经典之作。该文讨论金融发展如何通过放松企业的外部融资约束而促进增长，并用法律起源作为金融发展水平的工具变量。文章的计量模型的设定非常简洁，但行文论证极其精彩。我们不但可以学到如何用**交叉表**直观展示研究结果、如何构造指标来传达结果的经济含义；而且可以学到为什么要使用外生的调节变量来讨论**因果关系的作用机制**；更可以感受到作者为了**排除各种竞争性假说**所做的巧妙努力。
- **授课要点：**
  - 如何展示和解释结果
  - 如何讨论因果关系的作用机制
  - 如何排除竞争性假说：混淆因素和反向因果


>#### T8: 工具变量法的必要性与效果
- Nunn, Nathan, and Leonard Wantchekon, 2011, “The Slave Trade and the Origins of Mistrust in Africa.” *American Economic Review*101(7): 3221-52\. [[PDF](https://gitee.com/arlionn/stata_training/raw/master/PDF/Nunn_Wantchekon_2011_AER.pdf)]
- **论文简介：** [Nunn and Wantchekon (2011)](https://gitee.com/arlionn/stata_training/raw/master/PDF/Nunn_Wantchekon_2011_AER.pdf) 的论文是展示 **工具变量方法各种技巧** 的洋洋大观之作。该文讨论历史上的非洲奴隶贸易如何型塑了今天人际间的不信任，并用种族到海岸线的距离作为奴隶贸易强度的工具变量。文章先使用了 OLS 方法，然后评估 OLS 估计结果在多大程度上受到选择性偏误的影响；接着使用了工具变量方法，并通过“无第一阶段”**证伪检验** 和“工具变量疑似内生”证伪检验来论证工具变量的合理性；最后展示了如何通过精妙的控制来讨论因果关系的作用渠道。
- **授课要点：**
  - 如何通过可观测变量的选择性评估不可观测变量的选择性
  - 如何进行工具变量的证伪检验
  - 如何讨论因果关系的作用渠道


>#### T9: 匹配方法原理
- Imbens, Guido W, 2015, “[Matching Methods in Practice](https://gitee.com/arlionn/stata_training/raw/master/PDF/Imbens_2015_JHR.pdf): Three Examples.” *Journal of Human Resources* 50(2): 373-419.
- **论文简介：** [Imbens (2015)](https://gitee.com/arlionn/stata_training/raw/master/PDF/Imbens_2015_JHR.pdf) 是由匹配方法的扛鼎人物 Imbens 所分享的关于如何正确使用匹配方法的最新指南。我们知道，匹配方法为数众多，而且可以灵活操纵的空间也很大，匹配变量的选择更是有很多讲究，这使得匹配估计的结果往往不太稳健。我们从匹配方法的工作原理讲起，深入剖析其与 OLS 的异同，向学员传达匹配方法的思想实质。然后根据 Imbens 的建议，从**样本平衡性检验**、**倾向得分估计**、样本删截、估计方法选择等各个环节逐一讲解匹配方法的操作细节。
- **授课要点：**
  - 如何从反事实框架理解匹配方法 
  - 匹配方法与OLS方法的异同
  - 逐步讲解匹配方法的操作细节


>#### T10: 截面数据中匹配方法与工具变量法的综合运用
- Aidt, Toke S, and Raphael Franck, 2015, “Democratization Under the Threat of Revolution: Evidence Fro- the Great Refor- Act of 1832.” *Econometrica* 83(2): 505-47\. [[PDF](https://gitee.com/arlionn/stata_training/raw/master/PDF/Aidt_-2015-Econometrica.pdf)]
- **论文简介：** [Aidt and Franck (2015)](https://gitee.com/arlionn/stata_training/raw/master/PDF/Aidt_-2015-Econometrica.pdf) 是一篇在截面数据中综合运用 OLS 方法、匹配方法和工具变量方法的顶刊文献。该文讨论 1830 年代英国各地区斯温暴动的激烈程度如何形成了可置信的革命威胁，推动了代表新兴阶级的辉格党在议会势力的壮大，最终促成了改革法案的通过。从这篇文章中我们不但能够回顾之前所学内容，而且还能学到**安慰剂检验**和**证伪检验**等新的论证技巧。
- **授课要点：**
  - 如何评估系数稳定性
  - 同时使用多种匹配估计方法
  - 安慰剂检验与证伪检验


>#### T11: 连续型处理与多期双重差分方法
- Nunn, N., and N. Qian, 2011, “The Potato's Contribution to Population and Urbanization: Evidence Fro- a Historical Experiment.” *Quarterly Journal of Economics* 126(2): 593–650\. [[PDF](https://gitee.com/arlionn/stata_training/raw/master/PDF/Nunn_2011_QJE.pdf)]
- **论文简介：**  [Nunn and Qian (2011)](https://gitee.com/arlionn/stata_training/raw/master/PDF/Nunn_2011_QJE.pdf) 是一篇典型的运用连续型处理与多期双重差分方法的经典文献。该文讨论土豆这一起源于新大陆的农作物在旧大陆的推广如何促进了人口增长和城市化。文章用一国种植土豆的适宜程度作为该国接受 **“政策干预”** 的强度，用土豆在旧大陆的大规模推广来确定“政策干预”的时点。这篇文章所运用的方法比离散型处理或两期问题更具一般性，而且 **基准估计**、**灵活估计**、**滚动估计**、**变动处理时点**、**变动处理组** 等实证手段也极具借鉴意义。
- **授课要点：**
  - 灵活的方程设定：平行趋势与动态效应
  - 作图展示估计结果
  - 变动处理时点与变动处理组



>#### T12: 双重差分方法与匹配方法的结合
- Fowlie, et al., 2012, “What Do Emissions Markets Deliver and to Whom? Evidence Fro- Southern California's NOx Trading Program.” *American Economic Review* 102(2): 965-93\. [[PDF](https://gitee.com/arlionn/stata_training/raw/master/PDF/Fowlie_2012_AER.pdf)]
- **论文简介：** [Fowlie et al. (2012)](https://gitee.com/arlionn/stata_training/raw/master/PDF/Fowlie_2012_AER.pdf) 是双重差分方法与匹配方法相结合（**PSM+DID**）的代表作。我们首先介绍双重差分方法与匹配方法相结合的两种模式，其一是将匹配方法视为数据预处理手段，构造匹配样本再进行双重差分估计，其二是将多期问题转换为两期问题，先构造差分结果，然后进行匹配估计。前者的重点在第3讲中已经涉及，本讲介绍的论文则是对后者的应用。文章的一大亮点是尝试对“**无溢出效应**”和“**无混淆性**”这两大基本识别假设进行了间接检验。
- **授课要点：**
  - 如何构造匹配样本进行双重差分估计
  - 如何对差分结果进行匹配估计
  - 如何对识别假设进行间接检验


&emsp;


---
## 4. 报名信息
- **主办方：** 太原君泉教育咨询有限公司
- **标准费用**(含报名费、材料费)，差旅及食宿费自理：
  - 全价：6800元/人
  - 预报名价 (8月5日前报名) 6600元/人
  - 团报价：6000元/人（三人及以上）
  - 学生价：5800元/人（报到时需提供学生证原件）
- **老学员优惠：**
  - 参加过一次主办方培训的老学员：5700元/人
  - 参加过两次及以上主办方培训的老学员：5300元/人
- **友情高校感恩优惠：**  
  我们诚挚地感谢曾经团报的高校，来自以下高校的老师和学生可享受感恩价 5500 元/人：(按首字母拼音排序) **安徽财经大学、东北林业大学、河北大学、河北经贸大学、河南财经政法大学、暨南大学、金陵科技学院、南开大学、清华大学、山西财经大学、山西大学、太原科技大学、西安建筑科技大学、西南财经大学、厦门大学、运城学院、中南财经政法大学、中南大学、中山大学、中央财经大学**。
- **Note：** 以上各项优惠不能叠加使用。

#### 联系方式
- **邮箱：** [wjx004@sina.com](wjx004@sina.com)
- **电话 (微信同号)：** 王老师 18903405450 ；李老师 ‭18636102467
- **对公账户：**
  - **户名：** 太原君泉教育咨询有限公司
  - **账号：** 35117530000023891 (山西省太原市晋商银行南中环支行)
 


>报名链接： https://www.wjx.top/jq/41753249.aspx     
或 长按/扫描二维码报名：   
![连享会-2019暑期学术论文专题](https://images.gitee.com/uploads/images/2019/0622/181932_89888137_1522177.png)
>
>**温馨提示：** 按报名顺序挑选\安排座位
&emsp;


&emsp;

### 5. 交通和住宿
- **校内宾馆：** [西安西工大正禾宾馆](http://62474.hotel.cthy.com/)
- **酒店地址：** 西安 莲湖区 友谊西路127号 [[百度地图]](https://j.map.baidu.com/K28HZ)
- 住宿小知士：
正禾宾馆位于西北工业大学校内，上课、午休方便快捷，住宿环境可以参考以下图片：

[![住宿和教室](https://images.gitee.com/uploads/images/2019/0622/181932_c891f36c_1522177.jpeg)](https://gitee.com/arlionn/Course/blob/master/2019Papers.md)




























