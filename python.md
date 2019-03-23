# 连享会-Python爬虫与文本分析专题研讨班


![连享会-Python爬虫与文本分析专题.jpg](https://upload-images.jianshu.io/upload_images/7692714-16f9d7747595bfe2.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 "连享会-Python爬虫与文本分析现场班，山西大学 2019.5.17-19")

[toc]

---
## 1. 课程概览
- **时间：** 2019 年 5 月 17-19 日 (周五-周日)
- **时段：** 上午 9:00-12:00；下午 14:00-17:00，答疑：17:00-17:30
- **地点：** 山西大学-学术交流中心 ([百度地图](https://j.map.baidu.com/78RqP) | [谷歌地图](https://goo.gl/maps/BGjN3mVZi4L2))
- **主讲嘉宾：** 司继春 (第1-3讲)；刘老师 (第 4-6 讲)
- **授课内容：** 爬虫与文本分析 (Python)
  - **课程要点：** 本课程主要介绍 Python 的基础知识，并使用 Python 进行数据处理、数值计算、网络爬虫等不同任务的处理；介绍机器学习算法的原理，并使用 Python Step by Step 实现各类算法。
  - **主要方法：** Python, Scipy, Numpy, Pandas, Matplotlib, BeautifulSoup, Scrapy, httplib2, Selenium, Scikit-learn
- **软件\语言：** Python

&emsp;


---
## 2. 嘉宾简介
![司继春老师](https://upload-images.jianshu.io/upload_images/14991370-0e640cea0f10e179.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**司继春**，上海对外经贸大学统计与信息学院讲师，主要研究领域为微观计量经济学、产业组织理论。在 Journal of Business and Economic Statistics、《财经研究》等学术刊物上发表多篇论文，[[主页]](http://www.suibe.edu.cn/txxy/b1/2d/c5782a45357/page.htm)。 &emsp;     其实，大家更熟悉的是知乎上大名鼎鼎的 [[慧航]](https://www.zhihu.com/people/sijichun/columns)，拥有 219,753 个关注者，获得过 110,578 次赞同，他就是司继春老师 —— [[知乎-慧航]](https://www.zhihu.com/people/sijichun/columns)。

**刘老师**，于 2014 年获中国科学院大学博士学位，研究方向：自然语言理解、机器学习、知识获取。在 ACM Transactions on
Asian and Low-Resource Language Information Processing 、Journal of Integrative Agriculture、中文信息学报、计算机科学等杂志发表十余篇论文、授权专利十余项。

&emsp;

---
## 3. 授课内容

### 3.1 课程介绍

&emsp;

>- 为什么要学爬虫和文本分析？
>- 为什么要学机器学习算法？
>- 为什么要学 Python 语言？
>- 我们将学到什么？


&emsp;

>#### 为什么要学爬虫和文本分析？

在大数据时代，大量有价值的信息以文本等非结构化、异构型的数据格式存储于互联网网页中。从 Web 上快速、有效地提取这些信息对人文社会科学的深度研究尤为重要。

那么，如何获取这些信息呢？一个利器就是：**网络爬虫**。它能为我们提供高质量的分析文本，分析质量远高于传统工具。

事实上，无论是在管理学、经济学、金融学、会计学，还是人文社会科学的其他领域，基于网络爬虫的文本分析类研究都得到了高度的关注。其火热程度可以从相关论文的 Google 学术引用次数窥豹一斑。

例如，在金融和会计领域，Loughran and McDonald (2011) 发表于 **Journal of Finance** 上的有关文本分析技术的综述性文章，短短 8 年时间，引用率已经超过 1000。二人于 2016 年发表于 **Journal of Accounting Research** 的另一篇介绍文本分析在会计和金融领域应用的综述性文章目前已被引用 300 余次。

此外，在政治学领域，Grimmer and Stewart (2013) 的 “Text as data: The promise and pitfalls of automatic content analysis methods for political texts”，被引用 1200 余次；经济学领域，Hoberg and Phillips (2016, JPE) 被引用 500 余次。

利用 [Google 学术](https://scholar.google.com/) 顺藤摸瓜，可以发现，各个领域文本分析的来源非常丰富，包括：[历史典籍](http://www.cnki.com.cn/Article/CJFDTotal-WPCL201701006.htm)、报纸新闻、明清房契、[刑科题本](http://www.cnki.com.cn/Article/CJFDTotal-JJXU201901012.htm)、公司公告、明星微博等等，从而使研究的主题也得到了极大的扩展。

下面是一些我们摘录的一些论文信息：

**经济学领域**：  
- Hoberg, Gerard, and Gordon Phillips. 2016, Text-based network industries and endogenous product differentiation, ***Journal of Political Economy*** 124, 1423-1465\. Google 引用率超过 500 次。[[PDF]](http://faculty.tuck.dartmouth.edu/images/uploads/faculty/gordon-phillips/FinalJPE.pdf)

**金融和会计领域:**
- Loughran, Tim, and Bill McDonald. 2011\. When is a liability not a liability? Textual analysis, dictionaries, and 10‐ks, ***Journal of Finance*** , 66, 35-65. 该文是**金融和会计领域**颇具影响力的一篇文章，2011 年发表，短短几年的时间，Google 引用率已经超过 1000 次。[[PDF]](https://www.uts.edu.au/sites/default/files/ADG_Cons2015_Loughran%20McDonald%20JE%202011.pdf)
- Loughran, T., and B. Mcdonald. 2016, Textual analysis in accounting and finance: A survey, *Journal of Accounting Research* 54, 1187-1230. [[PDF]](https://onlinelibrary.wiley.com/doi/pdf/10.1111/1475-679X.12123)。发表仅 2 年的时间，Google 学术引用率已经飙升到接近 300 次。[[PDF]](http://sslab.nwpu.edu.cn/uploads/1478091993-5819e4d959012.pdf)
- Jegadeesh, Narasimhan, and Di Wu. 2013. Word power: A new approach for content analysis, *Journal of Financial Economics* 110, 712-729\. Goolge 学术引用率 207 次。[[PDF]](https://www.sciencedirect.com/science/article/pii/S0304405X13002328) [[PDF2]](https://www.sci-hub.shop/https://doi.org/10.1016/j.jfineco.2013.08.018)
- Neuendorf, Kimberly A, 2017\. The content analysis guidebook (Sage). 自 2002 年第一版以来，目前引用率已经达到 10000 余次。

**社会学领域**：
- Fairclough, Norman. 2003\. Analysing discourse: Textual analysis for social research (Psychology Press). 被引用次数：12678

**政治学领域**：
- Grimmer, Justin, and Brandon M Stewart. 2013, Text as data: The promise and pitfalls of automatic content analysis methods for political texts, ***Political analysis*** 21, 267-297\. Google 引用率超过 1200 次。[[PDF]](https://5harad.com/mse231/papers/grimmer_stewart_2013.pdf)


&emsp;


>#### 为什么要学机器学习算法？

机器学习 (Machine Learning, ML) 是一门多领域交叉学科，涉及概率论、统计学、凸分析、算法复杂度理论等多门学科。专门研究计算机怎样模拟或实现人类的学习行为，以获取新的知识或技能，重新组织已有的知识结构使之不断改善自身的性能。

机器学习是人工智能的核心，是使计算机具有智能的根本途径，其应用涉及人工智能的各个领域，它主要使用归纳、综合而不是演绎。机器学习已经有了十分广泛的应用，例如：数据挖掘、计算机视觉、自然语言处理、生物特征识别、搜索引擎、医学诊断、检测信用卡欺诈、证券市场分析、DNA序列测序、语音和手写识别等。

对于经济、金融、管理等人文社会科学领域而言，就目前而言，机器学习至少在如下几个方面具有重要作用：
- 解决可信度和数据异常值的问题：传统统计模型通常需要假设数据是如何创建的，数据的背后的过程以及数据的可信度。然而，机器学习通过使用高度灵活的算法来消除这些限制性的假设，这些算法不会给予比它应得的更多的可信度。
- 支持现代计算机和海量数据集：与手工流程不同，机器学习不假设世界充满了直线。相反，它会自动调整方程式以查明最佳模式，并测试哪些算法和模式最适合独立验证数据（而不是仅测试所训练的数据）。
- 利用缺少的值预测未来：高级机器学习不是要求数小时的数据清理，而是可以构建一个蓝图，优化特定算法的数据，自动检测缺失值，确定哪些算法不适用缺失值，寻找取代缺失值的最佳值，并使用缺失值的存在来预测不同的结果。


&emsp;

>#### 为什么要学 Python 语言？   

相信有不少老师和同学一直在使用 Stata, Eviews 和 R 等软件，而且只使用其中的一种，因为这已经能够应对多数实证分析工作的要求了。

然而，当某一天你看到「爬虫」、「文本分析」、「机器学习」、「数据挖掘」等名词出现在自己所在领域的 Top 期刊上，而自己却心生畏怯时，就会冒出一个自我质疑来：**我要不要再多学一个编程语言或软件？**

这不禁让人想起 **“狐狸与刺猬”** 的故事。二者的区别，据说最早是公元前七世纪的古希腊诗人阿尔奇洛克斯提出来的，他说：“狐狸知道很多事，刺猬则只知道一桩大事。”当受到威胁时，狐狸会随机应变，想出很多好点子；而刺猬则总是用同一种方法来应对：把自己卷成一个球。这两种动物，一个聪明狡猾，灵活善变；另一个恪守成式，以不变应万变。

正如哲学家柏林所说，两者的本质差异在于：刺猬坚持一种普遍原则，万事万物都用一种理念来解释；而狐狸则从多个维度出发，抓住那些常常看似不相干甚至矛盾的线索，发现实际是有关联的。

我们身边有很多 “伟大的刺猬”，也有很多 “伟大的狐狸”。

在尚未修炼到能参透 **“一桩大事”** 之前，不妨多效仿狐狸，多学习不同的思想、不同的方法，尽量都去尝试一下，最后再决定什么是最适合自己的。

至于 Python 是什么？Python 能干什么？相信大家都很容易了解到，你可以访问 [[python官网]](https://www.python.org/)。下面列举一点与本次课程相关的 Python 介绍：

「Python 是一种面向对象的解释型计算机程序设计语言，具有丰富和强大的库，已经成为继 JAVA，C++ 之后的第三大语言，它代码简洁，功能强大，非常适合爬虫，可以帮助我们有效地获取、统计和分析网络文本数据。」


&emsp;

>#### 我们将学到什么？

课程关注的重点在于 Python 的实际运用，我们将利用经典文献与案例进行演示，并讲解常见的、基本的语句结构，以便学员能够自行编写出所需的程序。在三天的课程中，你将学到：

- **Python：** 了解 Python 的基础知识、使用 Python 库进行数据分析、静态网页与动态网页的数据抓取
- **机器学习：** 掌握机器学习的基本概念，以及一些经典的机器学习算法及其实现，包括：决策树、多变量线性回归分析、Logistic 回归、Softmax 回归、正则化、神经网络等内容
- **实操：** 通过讲解经典论文与经典案例来向大家展示 Python 的实际操作和实现过程。



**各个专题的具体介绍如下：**

**第一讲：** 介绍 Python 语言的基础的入门知识与操作。其中，基本语法的讲授内容包括 Python 的处理数据类型、基本语法、函数功能等。

**第二讲：** 介绍在 Python 中使用特定类库对数据进行科学计算分析（Numpy+Scipy）、数据管理（Pandas）、作图（Matplotlib）、参数估计和假设检验等常用功能的操作。涉及的 Python 科学计算包： Numpy、Pandas、Matplotlib 等。

**第三讲：** 介绍使用 Python 语言抓取网页中目标数据的基本操作，本讲的内容包括静态网页数据的抓取与动态网页数据抓取两部分。首先概括性介绍基础的 Http 协议、HTML 语言、JavaScript 语言等，在此基础之上介绍使用 Python 爬取静态网页（beautifulsoup）、动态网页（selenium+phantomjs）的所需数据，并使用数据库对其进行存储。

**第四讲：** 介绍使用 Python 进行机器学习的基础知识。主要讲解机器学习的基本知识，以及机器学习的数学基础；并讲解决策树算法、单变量线性回归算法及基于梯度下降的求解方法，并介绍如何使用 Python 来实现决策树与单变量线性回归算法。

**第五讲：** 介绍使用多种机器学习算法的原理与实现，主要包括多变量线性回归、Logistic 回归、Softmax 回归等；以及介绍解决过拟合的正则化等方法，并且应用具体的例子利用 Python 来实现各类机器学习算法。

**第六讲：** 分两部分介绍如何使用 Python 实现神经网络机器。第一部分介绍神经网络基础知识，包括神经网络基础知识、神经网络的架构等；第二部分是讲授如何编写基于反向传播算法的神经网络，并用其演示手写数字的识别。


&emsp;

---
### 3.2 课程大纲

>#### 第 1 讲 Python 基础（3小时）
  - 基本的数据类型（整数、浮点数、字符串、列表、元组、字典等）
  - 基本的控制语句（循环、条件）
  - 函数
  - 类
  - 包管理
>#### 第 2 讲 Python 进阶（3小时）
  - 文本文件
  - csv、json 数据格式
  - 基本的科学计算 Numpy+Scipy
  - 数据管理 Pandas
  - Matplotlib 作图
  - 参数估计和假设检验

>#### 第 3 讲 Python 实现爬虫（3小时）
  - 网页分析：html、css 基本概念
  - beautifulsoup 解析 html
  - http 协议基础知识
  - 静态网页爬取：电影相关数据爬取、房产价格数据爬取、新闻页面爬取
  - 使用selenium爬取动态网页：网上商城价格的爬取
  - 数据的存储：SQL 语言与数据库

>#### 第 4 讲 机器学习初步（3小时）
  - 机器学习简介
    - 什么是机器学习？机器学习的要素
    - 监督学习与无监督学习
  - 机器学习的数学基础
    - 线性代数：矩阵、向量、范数、特征分解、奇异值分解等
    - 概率：概率定义、分布、条件概率、贝叶斯定义、方差、常见分布等
    - 信息论：熵、联合熵、条件熵、相对熵、互信息等
  - 决策树及其 Python 实现
    - 分类的基本概念
    - 决策树概念与示例、学习与实现
    - 决策树python示例分析——用户行为分析

>#### 第 5 讲 机器学习算法（3小时）
- 多元线性回归
  - 单变量线性回归的模型表示、代价函数、梯度下降算法
  - 介绍多元线性回归的概念与模型
  - Python 实例：多特征房价预测
- Logistic 回归
  - Logistic 模型表示、决策边界、交叉熵代价函数
  - Python 实例：预测学生是否会被大学录取
- Sofmax 回归及其实现
  - Softmax 回归模型表示与求解
  - Python 实例：多物品自动识别分类
- 正则化
  - 训练误差与泛化误差的概念、欠拟合与过拟合的现象
  - 如何解决过拟合？——正则化

>#### 第 6 讲 神经网络机器实现（3小时）
- 神经网络基础
  - 神经网络介绍
  - 感知机与 S 型神经元
  - 神经网络的架构
  - 使用梯度下降算法进行学习
- 神经网络的 Python 实现——识别手写数字识别
  - 反向传播算法
  - Python 实现网络分类数字


&emsp;

---
## 4. 报名信息
- **主办方：** 太原君泉教育咨询有限公司
- **标准费用**(含报名费、材料费)，差旅及食宿费自理：

  - 全价：3200元/人
  - 预报名价 (5月5日前报名) 2900元/人
  - 团报价：2700元/人（三人及以上）
  - 学生价：2600元/人（报到时需提供学生证原件）

- **老学员优惠：**
   - 参加过一次主办方培训的老学员：2500元/人
   - 参加过两次主办方培训的老学员：2200元/人

- **友情高校感恩优惠：**  
  我们诚挚地感谢曾经团报的高校，来自以下高校的老师和学生可享受感恩价 2400 元/人：(按首字母拼音排序) **安徽财经大学、东北林业大学、河北大学、河北经贸大学、暨南大学、金陵科技学院、南开大学、山西财经大学、山西大学、太原科技大学、
运城学院、中南财经政法大学、中南大学、中山大学、中央财经大学**。
- **Note**：以上各项优惠不能叠加使用。
- **联系方式：**
    -  邮箱：[wjx004@sina.com](http://wjx004@sina.com/)
    -  电话 (微信同号)：王老师 18903405450 ；李老师 18636102467
    -  对公账户： 35117530000023891 (山西省太原市晋商银行南中环支行)

- **温馨提示：** 按报名顺序挑选\安排座位
- 长按/扫描二维码报名：


![连享会-Python爬虫-报名二维码.jpg](https://upload-images.jianshu.io/upload_images/7692714-c4f454e459a8a237.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 "连享会-山西大学-Python爬虫-文本分析报名二维码")

&emsp;

---
![Python爬虫与文本分析专题-海报.jpg](https://upload-images.jianshu.io/upload_images/7692714-e9ff58014f793e44.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240 "连享会-Python爬虫与文本分析现场班，山西大学 2019.5.17-19")

---
