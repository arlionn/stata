> 微信推文说明：自己制作一个符合国内期刊风格的模板，然后发布命令，并在 github 中发布代码，供大家下载使用。

## 私人定制！ 用 `brewsheme` 定制我的 stata 绘图模板


[toc]


![](http://y0.ifengimg.com/news_spider/dci_2012/03/4697e06983ec9e5f83fd63756cceae33.jpg)
&emsp; &emsp; 
私人定制的迫击炮

---

### 1. 简明效果对比

![](http://wbuchanan.github.io/brewscheme/img/brewscheme_onecolorex2.png)

![](http://wbuchanan.github.io/brewscheme/img/brewscheme_manycolorex1.png)

> [Sourece: wbuchanan.github.io](http://wbuchanan.github.io/brewscheme/help/brewscheme/)


---
> #### 对比1：散点图


```stata
*- Load the auto data set
sysuse auto, clear

*- Create a new scheme file for all graph types
brewscheme, scheme(test) allstyle(dark2) allcolor(7)

*- Make a simple graph using Stata defaults
tw scatter mpg length || lfit mpg length, name(stata, replace)

*- Make the same graph using the scheme file you just created
tw scatter mpg length || lfit mpg length, scheme(test) name(brewscheme, replace)
```
![](https://www.statalist.org/forums/filedata/fetch?id=1304036&d=1438109219&type=full "Stata 官方命令效果")

![](https://www.statalist.org/forums/filedata/fetch?id=1304037&d=1438109231&type=full "brewscheme 效果")


---
> #### 对比2：箱型图

```stata
*-Create a new scheme file with different palettes
* and #s of color per palette for different graph types
brewscheme, barst(paired) barc(12) dotstyle(prgn)  ///
            dotc(7) scatstyle(set1) scatc(9)       ///   
            linest(dark2) linec(8) somec(8)        ///
            somestyle(accent) areast(dark2)        ///   
            areac(8) scheme(test2)

*- Make a simple graph using Stata defaults
gr box price, over(rep78) name(stata, replace) 

*- Make the same graph using 
*  the scheme file you just created
gr box price, over(rep78) asyvars  ///
   scheme(test2) name(brewscheme, replace)
```

![](https://www.statalist.org/forums/filedata/fetch?id=1304038&d=1438110150&type=full "Stata 官方命令效果")

![](https://www.statalist.org/forums/filedata/fetch?id=1304039&d=1438110167&type=full "brewscheme 效果")



---

### 2. 说明文档
> [statalist post][2]，[brewscheme][2a] 以及 [PDF介绍][3]

---
### 3. 安装

>```
>install brewscheme, replace
>```
或
>```
>net inst brewscheme, from("http://www.paces-consulting.org/stata")
>```


---
### 4. 在线帮助和范例

- [brewscheme](http://wbuchanan.github.io/brewscheme/help/brewscheme/)

- [brewtheme](http://wbuchanan.github.io/brewscheme/help/brewtheme/)

- [brewcbsim](http://wbuchanan.github.io/brewscheme/help/brewcbsim/)

- [brewcolordb](http://wbuchanan.github.io/brewscheme/help/brewcolordb/)

- [brewcolors](http://wbuchanan.github.io/brewscheme/help/brewcolors/)

- [brewextra](http://wbuchanan.github.io/brewscheme/help/brewextra/)

- [brewmeta](http://wbuchanan.github.io/brewscheme/help/brewmeta/)

- [brewproof](http://wbuchanan.github.io/brewscheme/help/brewproof/)

- [brewsearch](http://wbuchanan.github.io/brewscheme/help/brewsearch/)

- [brewterpolate](http://wbuchanan.github.io/brewscheme/help/brewterpolate/)

- [brewviewer](http://wbuchanan.github.io/brewscheme/help/brewviewer/)

- [libbrewscheme](http://wbuchanan.github.io/brewscheme/help/libbrewscheme/)

- [filesys](http://wbuchanan.github.io/brewscheme/help/filesys/)

- [hextorgb](http://wbuchanan.github.io/brewscheme/help/hextorgb/)


[2]:https://www.statalist.org/forums/forum/general-stata-discussion/general/1304035-new-package-on-ssc-brewscheme "new package on SSC: brewscheme"
[2a]:http://www.paces-consulting.org/blog/brewscheme-1-0/
[3]:http://www.stata.com/meeting/columbus15/abstracts/materials/columbus15_buchanan.pdf



---
 ![Stata连享会二维码](http://wx1.sinaimg.cn/mw690/8abf9554gy1fj9p14l9lkj20m30d50u3.jpg "扫码关注 Stata 连享会")



