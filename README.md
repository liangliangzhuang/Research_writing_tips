# 英语科研写作技巧笔记

## 简介

由于需要对新师弟师妹进行“培训”，所以趁这个机会，把一些科研写作中容易出现的坑一一整理出来！庄小编打算开个新的系列，打算整理下自己在科研写作方面的笔记。

> **注意**：这个庄小编的**科研写作笔记**，不是教程噢！我只是个科研新手，眼界比较低，说的不一定对，大家觉得对的拿去用，不对的看看就行了（好心人也欢迎来批评）～

该系列主要针对科研新手，使用 LaTeX 写英语科研论文。但是一些经验也不限于此。

> 如果你对 LaTeX 写作不了解并感兴趣的话，可参考这些教程： 。 

初步打算讲：1.格式问题；2. 英语问题（自己薄弱环节）；3. 写作逻辑问题；

第一部分来讲讲 LaTeX 中的**写作格式**可能出现的问题。

## 写作格式问题：

### 1. **符号问题**：

与中文不同，英语标点符号后面需要空格（, . : ）

![](https://files.mdnice.com/user/5000/fbba3527-27f7-452e-bcae-dffc5b4f516e.png)

### 2. **缩写问题**：

第一次出现需要全称 + 缩写（例如：accelerated life test (ALT)），之后都用缩写表示（例如：ALT is xxx）。

### 3. **公式问题**：

a. 末尾需要加入标点符号。

> **注意**：句号后面新的句子需要大写，逗号后面需要小写。
  
![句号后面新的句子需要大写](https://files.mdnice.com/user/5000/981cd77f-9893-4fac-a404-13f138b7912d.png)

      
![逗号后面需要小写](https://files.mdnice.com/user/5000/c494efba-3a32-4ce0-aa0a-a4225831f491.png)

        
b. 并列的公式需要对齐，使用 ``\begin{aligned} \end{aligned}``。
    

![](https://files.mdnice.com/user/5000/2be7e1d6-5773-4a40-aa7f-905f36207e1c.png)

    
c. 所有符号第一次出现都需要标明含义，或者有专门一节罗列并说明全文符号。


![](https://files.mdnice.com/user/5000/950e8ef5-e388-4de2-8a09-3c46ce25e783.png)

    
d. 公式中的括号需要使用 ``\left( \right)``，不要直接使用`()`。其他括号``{},[]``类似操作。


![错误示范](https://files.mdnice.com/user/5000/80b6d49b-8f60-47dc-824c-e3b1515aecee.png)


![正确示范](https://files.mdnice.com/user/5000/75679831-d7c7-42b3-8178-ff9dae4c7cac.png)

    
e. 公式中的文字需要使用 ``\text{}``，例如：`x \quad \text{and} \quad y`，并前后可以适当添加空格`\quad`。
    
f. 注意全文符号不要用重，太多符号的话，可以  ``\mathbb{}, \mathcal{}`` 等区分。
    
g. 推荐一个公式截图软件 [Mathpix Snipping Tool](https://mathpix.com/)，建议使用学校邮箱，每个月会有 100 次免费使用次数。小编以前写过相关介绍[推文](https://mp.weixin.qq.com/s/ScOf0CPD9fO_II92Q4CHlA)。
    
### 4. **参考文献问题：**

a. **搜索方式**：使用[谷粉学术](https://gfsoso.99lb.net/)搜索文章，点击引用，下载 BibTeX 格式，加入到 .bib 文件中。


![以谷歌学术为例](https://files.mdnice.com/user/5000/db7e4174-7099-4b53-be80-8f4d80c3d2f4.png)

b. 参考文献需要一致。

c. **注意细节**：

1). 论文名称特定大写，且不在首个字母，需要使用{}标注，例如 A {B}ayesian reliability。


![](https://files.mdnice.com/user/5000/fcfb9c58-0b9e-4904-af84-8e19ae066446.png)


2). & 符号前需要添加 \，例如：Reliability Engineering \& System Safety


![](https://files.mdnice.com/user/5000/be936f94-d573-408c-ae23-01224d91fbcc.png)


3). 不同期刊要求不同：有的需要添加月份；有的需要添加 doi。


4). 尽可能阅读和引用高质量文章（业内认可度高的期刊，不同方向分类讨论）

> 例如可靠性领域中：IEEE 系列(TR，TIE，TII等)、Technometics、JQT、RESS、IISE、EJOR、QTQM 等。
    
d. 近几年的文献需要追踪和引用，投稿期刊的文章需要引用多篇（3-4）近 2 年文献（个人观点，和 IF 有关）。
    
### 5. **图表问题**

a. 图表标题后需要添加符号。每个图表需要添加标签`\label{}`，索引时使用 ``\ref{}``。


b. 图表大小合适，使用`\scalebox{0.83}{}`缩放表格；使用 ``[width=16cm]`` 修改图片大小。例如：``\includegraphics[width=16cm]{figure/xx.pdf}``。



c. 最好将图片放到新的文件夹中（例如：figure，然后使用上述（`figure/xx.pdf`）加载图片）。

d. 图表最好放在文中的 top/bottom 位置，可以通过[tb]来修改，例如：``\begin{figure}[tb]  \end{figure}``。


![](https://files.mdnice.com/user/5000/d0ed2695-5624-48c1-97e8-c08b0a830587.png)


e. 小数点后保留位数同类型数据需要保持一致。不同表也应该相对一致。


![错误示范](https://files.mdnice.com/user/5000/fb75c8b2-a913-4d2b-ba0d-7e35f0ea8c4a.png)

表格加载示例代码：
```latex
\begin{table}[htbp]
	\centering
	\caption{The progressive censoring schemes for $k=3$.}
	\vskip 0mm \setlength{\tabcolsep}{4mm}
	\scalebox{0.93}{
	    \begin{tabular}{cllll}
	    \end{tabular}}
	\label{tab1}
\end{table}%
```

图片加载示例代码：
```latex
\begin{figure}[htbp]
	\centering
	\includegraphics[width=0.95\columnwidth]{figure/xxx.pdf}\\
	\caption{xxx.}
	\label{xxx}
\end{figure}
```
> 加载 2*2 的图片等排版情况可见： 。 

## 小编有话说

这些是目前小编能想到的一些小细节。如果读者有什么补充可文末留言，或者来我的 Github 提出 issue。 希望这个系列能够一直完善下去，为更多的科研新手造福。








