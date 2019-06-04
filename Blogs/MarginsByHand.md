> 作者：高娜娜（中南财经政法大学）
#### 交乘项 (调节效应\中介效应)

- [Stata: 交叉项\交乘项该这么分析！](http://www.jianshu.com/p/b5ea12da7f36)
- [Stata：交乘项该如何使用？](http://www.jianshu.com/p/f7222672fe89)
- [Stata：边际效应分析](http://www.jianshu.com/p/012d8a6159cf)
- [Stata：图示连续变量的边际效应(交乘项)](http://www.jianshu.com/p/7af58033dc24)
- [Stata：图示交互效应\调节效应](http://www.jianshu.com/p/fa6778828354)
- [加入交乘项后符号变了!?](http://www.jianshu.com/p/953f30f39195)

在建立模型时，我们往往会根据一定的经济理论加入一些交乘项，在 Stata 里，用 `margins` 命令可以直接得到相关变量的边际效应。然而，理解边际效应的原理很重要，它能够帮助我们理解模型所反映的经济学含义。因此，本文就来介绍一下如何手动计算交乘项的边际效应。

## 1. 边际效应计算原理

### 1.1 两个变量的交乘项

在线性模型中，假设 $X$ 和 $z$ 之间相互作用，模型的基本形式如下所示：

$$
Y=\beta_{0}+\beta_{1} X+\beta_{2} Z+\beta_{3} X Z + u
$$

以 $X$ 为例， $X$ 的边际效应是 $X$ 每增加 1 单位 $Y$ 的变化。因此，对 $Y$ 求 $X$ 的偏导便得到 $X$ 对 $Y$ 的边际效应，如下所示：

$$
\frac{\partial Y}{\partial X}=\beta_{1}+\beta_{3} Z
$$


由上式可以看出， $X$ 的边际效应并不是恒定不变的，它会随着 $Z$ 的变化而变化。结合估计出来的 $\beta_{1}$ 和 $\beta_{3}$，我们可以计算出在给定 $Z$ 的特定取值时 $X$ 对 $Y$ 的边际影响。比如在 $Z$ 取均值或四分位点时 $X$ 的边际效应。

在该模型中，$X$ 对 $Y$ 的边际效应的标准误，即 ${\partial Y}/{\partial X}$ 的标准误也与 $Z$ 的取值有关：

$$
 \operatorname{Var}({\partial Y}/{\partial X}) = \sqrt{\operatorname{Var}\left(\beta_{1}\right)+Z^{2} \operatorname{Var}\left(\beta_{3}\right)+2 Z \operatorname{Cov}\left(\beta_{1} \beta_{3}\right)}
$$

利用模型估计得到的 $\beta_{1}$ 的方差、$\beta_{3}$  的方差、$\beta_{1}$ 和 $\beta_{3}$ 的协方差以及给定的 $Z$ 值，可以得到 $X$ 的标准误。计算标准误有助于在绘制边际效应图时附加上置信区间。

### 1.2 三个变量的交乘项

对于含有三个变量交乘项的模型（如下模型），也可以用上述原理来手动计算变量的边际效应。

$$
Y=\beta_{0}+\beta_{1} X+\beta_{2} Z+\beta_{3} W+\beta_{4} X Z+\beta_{5} XW+\beta_{6} Z W+\beta_{7} XZW+u
$$

该模型中 X 的边际效应和 ∂y/∂x 的方差的表达式如下所示：

$$
\begin{aligned} \frac{\partial Y}{\partial X}=\beta_{1}+\beta_{4} Z+\beta_{5} W +\beta_{7} Z W \end{aligned}
$$

$$
\begin{align}
 \operatorname{Var}({\partial Y}/{\partial X}) &=\operatorname{Var}\left(\beta_{1}\right)+Z^{2} \operatorname{Var}\left(\beta_{4}\right)+W^{2} 2 \operatorname{Var}\left(\beta_{5}\right)  +Z^{2} W^{2} \operatorname{Var}\left(\beta_{7}\right)  \\ 
&+2 Z \operatorname{cov}\left(\beta_{1} \beta_{4}\right) +2 W \operatorname{cov}\left(\beta_{1} \beta_{5}\right)  +2 Z W \operatorname{cov}\left(\beta_{1} \beta_{7}\right) \\
&+2 Z W \operatorname{cov}\left(\beta_{4} \beta_{5}\right) +2 W Z^{2} \operatorname{cov}\left(\beta_{4} \beta_{7}\right)  +2 Z W^{2} \operatorname{cov}\left(\beta_{5} \beta_{7}\right)
\end{align}
$$

特别地，一种特殊的情况是，在三个变量中有一个是 0-1 变量，比如下面模型中的 $D$ 变量。

$$
Y=\beta_{0}+\beta_{1} X+\beta_{2} W+\beta_{3} D+\beta_{4} XW+\beta_{5} XD+\beta_{6} WD+\beta_{7} XWD+u
$$

在这种情况下，我们可以根据 $D$ 将样本分成两个样本组，即 **G1 组** ($D=1$) 和 **G2 组** ($D=0$) ，使每个组中只包含一个交乘项，然后对两个样本组分别进行回归分析并求得 $X$ 的边际效应。

$$
Y=\beta_{0}+\beta_{1g} X+\beta_{2g} W+\beta_{3g} XW+u, \ \ g=1,2
$$


当我们把该模型拆成两个含有两个交乘项的模型时，变量 $X$ 的边际效应和 ${\partial Y}/{\partial X}$ 的标准误的表达式与含有两个变量交乘项的模型一致，此处不再赘述。

## 2. Stata 实现

下面我们使用 Stata 自带的 **nlsw88.dta** 数据为例，手动计算交乘项的边际效应。

### 2.1 两个变量的交乘项

$$
wage=\beta_{0}+\beta_{1} grade+\beta_{2} ttl_{-} exp +\beta_{3} grade_{-}ttl+u
$$

其中， `wage` 表示个体的工资水平， `grade` 表示已完成受教育的年限， `ttl_exp` 表示个体的工作时间，而 `grade_ttl` 是 `grade` 与 `ttl_exp` 的乘积。

- **计算边际效应**

在上述模型表示，已完成受教育年限会影响工资水平，而个体的工作经验又充当了调节变量，我们要计算的是已完成受教育年限对工资的边际效应。

首先，对上述模型进行估计。

```stata
sysuse "nlsw88.dta", clear
gen grade_ttl=grade*ttl_exp
reg wage grade ttl_exp grade_ttl 
```

```stata
------------------------------------------------------------------------------
        wage |      Coef.   Std. Err.      t    P>|t|     [95% Conf. Interval]
-------------+----------------------------------------------------------------
       grade |   .2515455   .1315367     1.91   0.056    -.0064011    .5094921
     ttl_exp |   -.143543   .1284932    -1.12   0.264    -.3955211    .1084352
   grade_ttl |    .032074   .0099813     3.21   0.001     .0125005    .0516475
       _cons |    .933757   1.657647     0.56   0.573    -2.316929    4.184443
------------------------------------------------------------------------------
```

模型中变量的系数，以及系数的方差协方差存储在矩阵 `b` 和矩阵 `V` 中。

```stata
ereturn list
```

```stata
matrices:
                  e(b) :  1 x 4
                  e(V) :  4 x 4
```

然后，从矩阵中提取我们需要的 `β1`、`β3`、`var(β1)`、`var(β3)`、`cov(β1 β3)`，分别赋给标量`b1`、`b3`、`varb1`、`varb3`、`covb1b3`。

```stata
matrix b=e(b)
matrix V=e(V)
scalar b1=b[1,1]
scalar b3=b[1,3]
scalar varb1=V[1,1]
scalar varb3=V[3,3]
scalar covb1b3=V[1,3]
```

最后，计算边际效应。如果我们要计算在 `ttl_exp` 的均值下 `grade` 的边际效应，我们需要找到 `ttl_exp` 的均值，然后带入到边际效应的计算公式里即可。当然，我们也可以带入其他的 `ttl_exp` 值来得到 `grade` 的边际效应。

```stata
sum ttl_exp
scalar ttl_mean=r(mean)
dis "Margins：" b1+b3*ttl_mean
dis "Std.Err：" sqrt(varb1+varb3*(ttl_mean^2)+2*covb1b3*ttl_mean)
```

```stata
Margins：.65359238
Std.Err：.04536131
```

- **绘制边际效应图**

为了绘制 `grade` 的边际效应图，我们需要知道 `grade` 的边际效应如何随着 `ttl_exp` 变化。

首先，我们需要得到一系列连续变化的 `ttl_exp` 值，在数据中，`ttl_exp` 的最小值是 0.16，最大值是 28.9，用以下命令得到以 0.01 为间隔从 0.16 变化到 28.9 的序列。

```stata
set obs 2875
generate MVZ=(_n+15)/100
```

然后，分别计算每一个 `MVZ` 上 X 的边际效应 `conbx`、标准误 `consx`、5%置信区间的上界 `upperx`和下界 `lowerx`。

```stata
gen conbx=b1+b3*MVZ 
gen consx=sqrt(varb1+varb3*(MVZ^2)+2*covb1b3*MVZ)
gen ax=1.96*consx
gen upperx=conbx+ax
gen lowerx=conbx-ax
```

为了图形的美观，我们构建了一些辅助值。这些辅助值产生的效果可以参见后文绘制的图形。

```stata
gen where=-0.045
gen pipe = "|"
gen yline=0
```

```stata
graph twoway hist ttl_exp, width(0.5) percent color(gs14) yaxis(2)        ///
        ||   scatter where ttl_exp , plotr(m(b 4)) ms(none) mlabcolor(gs5) mlabel(pipe) mlabpos(6) legend(off)   ///
        ||   line conbx  MVZ,clpattern(solid) clwidth(medium) clcolor(black) yaxis(1)  ///
        ||   line upperx MVZ,clpattern(dash)  clwidth(thin)   clcolor(black)  ///
        ||   line lowerx MVZ,clpattern(dash)  clwidth(thin)   clcolor(black)  ///
        ||   line yline  MVZ,clpattern(solid) clwidth(thin)   clcolor(black)   ///
        ||   ,    ///
             xlabel( 0 5 10 15 20 25 30, nogrid labsize(2))  ///
             ylabel(-.2 0 .2 .4 .6 0.8 1 1.2 1.4 1.6 , axis(1) nogrid labsize(2))  ///
             ylabel(0 1 2 3 4 5, axis(2) nogrid labsize(2))  ///
             yscale(noline alt)  ///
             yscale(noline alt axis(2))  ///	
             xscale(noline)  ///
             legend(off)  ///
             xtitle("" , size(2.5))  ///
             ytitle("" , axis(2) size(2.5))  ///
             xsca(titlegap(2))  ///
             ysca(titlegap(2))  ///
             scheme(s2mono) graphregion(fcolor(white) ilcolor(white) lcolor(white))

```

![image.png](https://images.gitee.com/uploads/images/2019/0511/203228_1fe2e87f_4770163.png)

##### （2）含有三个变量的交乘项

$$
\begin{align}
wage &= \beta_{0}+\beta_{1} grade +\beta_{2} ttl_{-}exp +\beta_{3}  union +\beta_{4} grade_{-}ttl \\ 
&+\beta_{5}  grade_{-}union +\beta_{6}  ttl_{-}union +\beta_{7}  grade_{-}ttl_{-}union + u
\end{align}
$$

其中，`wage`、`grade`、`ttl_exp`、`grade_ttl` 的含义同模型一。此外，该模型中加入了 `union` 变量，该变量表示该妇女是否参加工会，1表示参加，0表示未参加。并加入 了`grade` 和 `union`、`ttl_exp` 和 `union` 的交乘项 `grade_union` 、`ttl_union`，以及 `grade`、`ttl_exp` 和 `union` 三个变量的交乘项 `grade_ttl_union`。

在该模型中，`union` 是 0-1 变量，我们根据 `union` 将模型二改写成如下形式：

$$
wage=\beta_{0}+\beta_{1g} grade+\beta_{2g} ttl_{-} \exp +\beta_{3g}  grade _{-} ttl+ u
$$

$$
\text { if } union=1, g=1 ; \text { if }union=0, g=2
$$

我们需要分别估计 `union=1` 和 `union=0` 时的模型，并分别计算 `grade` 边际效应。方法同模型一，此处直接附上代码和图形。

```stata
**计算边际效应：union==1**
reg wage grade ttl_exp grade_ttl if union==1
matrix b_1=e(b)
matrix V_1=e(V)
scalar b1_1=b_1[1,1]
scalar b3_1=b_1[1,3]
scalar varb1_1=V_1[1,1]
scalar varb3_1=V_1[3,3]
scalar covb1b3_1=V_1[1,3]

sum ttl_exp if union==1
scalar ttl_mean_1=r(mean)
dis "Margins_1：" b1_1+b3_1*ttl_mean_1
dis "Std.Err_1：" sqrt(varb1_1+varb3_1*(ttl_mean_1^2)+2*covb1b3_1*ttl_mean_1) 

gen conbx_1=b1_1+b3_1*MVZ 
gen consx_1=sqrt(varb1_1+varb3_1*(MVZ^2)+2*covb1b3_1*MVZ)
gen ax_1=1.96*consx_1
gen upperx_1=conbx_1+ax_1
gen lowerx_1=conbx_1-ax_1

**计算边际效应：union==0**
reg wage grade ttl_exp grade_ttl if union==0
matrix b_0=e(b)
matrix V_0=e(V)
scalar b1_0=b_0[1,1]
scalar b3_0=b_0[1,3]
scalar varb1_0=V_0[1,1]
scalar varb3_0=V_0[3,3]
scalar covb1b3_0=V_0[1,3]

sum ttl_exp if union==0
scalar ttl_mean_0=r(mean)
dis "Margins_0：" b1_0+b3_0*ttl_mean_0
dis "Std.Err_0：" sqrt(varb1_0+varb3_0*(ttl_mean_0^2)+2*covb1b3_0*ttl_mean_0) 

gen conbx_0=b1_0+b3_0*MVZ 
gen consx_0=sqrt(varb1_0+varb3_0*(MVZ^2)+2*covb1b3_0*MVZ)
gen ax_0=1.96*consx_0
gen upperx_0=conbx_0+ax_0
gen lowerx_0=conbx_0-ax_0

**绘图**
graph twoway line conbx_1  MVZ, clpattern(solid) clwidth(medium) clcolor(blue)  ///
        ||   line upperx_1 MVZ, clpattern(dash)  clwidth(thin)   clcolor(blue)  ///
        ||   line lowerx_1 MVZ, clpattern(dash)  clwidth(thin)   clcolor(blue)  ///
        ||   line conbx_0  MVZ, clpattern(solid) clwidth(medium) clcolor(red)   ///
        ||   line upperx_0 MVZ, clpattern(dash)  clwidth(thin)   clcolor(red)   ///
        ||   line lowerx_0 MVZ, clpattern(dash)  clwidth(thin)   clcolor(red)   ///
        ||   line yline    MVZ, clpattern(solid) clwidth(thin)   clcolor(black)    ///
        ||   ,    ///
             xlabel( 0 5 10 15 20 25 30, nogrid labsize(2))  ///
             ylabel(-.2 0 .2 .4 .6 0.8 1 1.2 1.4 1.6 , nogrid labsize(2))  ///
             xscale(noline) ///
             legend(off)  ///
             xtitle("" , size(2.5))  ///
             xsca(titlegap(2))  ///
             ysca(titlegap(2))  ///
             scheme(s2mono) graphregion(fcolor(white) ilcolor(white) lcolor(white))
```

![image.png](https://images.gitee.com/uploads/images/2019/0603/162137_410e0de7_4770163.png)


>**参考资料**：[Marginal Effect Plot for X: An Interaction Between X and Z](http://mattgolder.com/files/interactions/interaction1.pdf)


