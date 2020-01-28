# 【CM1】带分红寿险两种形式的复利bonus
$\def\angld#1{\overline{#1\,}\kern-3mu\lower-1mu\small|}$
在CM1的寿险精算部分（部分学校对应的课程名称为寿险1或寿险A）会出一道总保费（Gross Premium）和总保费准备金（Gross Premium Reserve, Gross Premium Policy Value）计算的大题。为适当增加题目难度，CM1常考察带分红（With-profit）的寿险，其保险金额（Sum Assured）会随着Bonus（红利）而增长（通常为单利或复利增长）。其中，对于保额复利增长（compound reversionary bonus）的情况，为方便考生查表（Tables）计算，利率（用字母$i$表示）和红利利率（用字母$b$表示）通常有以下两种组合：

- 组合1: 利率为6%，compound bonus为1.92308%
- 组合2: 利率为$x$%，compound bonus也为$x$%

我们以CT5的两道真题为例，对两种组合的解法逐一说明。
## 利率为6%，compound bonus为1.92308%
Exercise 1: CT5 April 2008 Q11
![EX1](https://qiniu.mdnice.com/af91ff18b727e2097c5e6c127e1387c3.jpeg)
考察复利bonus的生死两全保险的未来法总保费和总保费准备金的计算。其中利率为6%，compound bonus为1.92308%.
我们看第一问。这里有增长的部分只是保额，所以要处理的部分在EPV of death benefits. 我们需要将survival benefits和death benefits分拆开来计算，原因是死亡时立即给付的生死两全保险在近似为死亡年度末的EPV时需要分拆。记$b=1.92308\%$:

$$
\begin{array}{ll}
{\text{EPV of benefits}} & {} \\
{=\frac{75000}{(1+b)}\times (1.06)^{0.5}({_{}q}_{[50]}(1+b)v+{_{1|}q}_{[50]}(1+b)^{2}v^{2}}& {} \\
{\quad +\cdots+ {_{9|}q}_{[50]}(1+b)^{10}v^{10})+75000{_{10}p}_{[50]}(1+b)^{10}v^{10}} & {\mbox{令} v_{j}=v(1+b)} \\
{=\frac{75000}{(1+b)}\times (1.06)^{0.5}A_{[50]:\angld{10}@j}^1+75000{_{10}p}_{[50]}\times \frac{1}{(1+j)^{10}}} & {\mbox{其中}j=\frac{1.06}{(1+b)}-1=0.04}
\end{array}
$$
接下来查表就好。利率为6%，compound bonus为1.92308%的组合妙就妙在组合出新的利率$j=0.04$，刚好可以查4%的AM92表。
## 利率为$x$%，compound bonus也为$x$%
Exercise 2: CT5 April 2011 Q12
![EX2](https://qiniu.mdnice.com/f026304442a4d1a44ed0667f20d93d91.jpeg)
考察保额复利增长的定期寿险的未来法总保费和总保费准备金的计算。其中利率为4%，保额增长率也为4%.

看第一小问。我们用和上题相同的方法，记$b=4\%$：
$$
\begin{array}{ll}
{\text{EPV of benefits}} & {} \\
{=75000({_{}q}_{[40]}v^{0.5}+{_{1|}q}_{[40]}(1+b)v^{1.5}+\cdots+ {_{24|}q}_{[40]}(1+b)^{24}v^{24.5} )}& {} \\
{=\frac{75000\times (1+i)^{0.5}}{(1+b)}\times A_{[40]:\angld{25}@j}^1} & {\mbox{其中}j=\frac{1.04}{(1+b)}-1=0\%} \\
{=\frac{75000\times (1+i)^{0.5}}{(1+b)}\times(_{}A_{[40]}-{_{25}p}_{[40]}v^{25}_{}A_{65})@j} & {}\\
{=\frac{75000}{(1.04)^{0.5}}\times(1-\frac{8821.2612}{9854.3036}\times1\times1)} & {} 
\end{array}
$$

这里新计算出的$j=0\%$, 没法对$A_{[40]:\angld{25}}^1$直接查表，所以我们先转化为终身寿险的保险金EPV，根据原始定义可以发现：
$$
_{}A_{x}=\sum_{k=0}^{\infty}v^{k+1}{_{k|}q}_{x}=\sum_{k=0}^{\infty}{_{k|}q}_{x}=1
$$

这道题的Renewal expenses也是4%的增长率，所以：
$$
\begin{array}{ll}
{\text{EPV of renewal expenses}} & {} \\
{=75(\ddot{a}_{[40]:\angld{25}@j} -1 )}& {\mbox{其中}j=\frac{1.04}{(1+b)}-1=0\%} \\
{=75 \frac{1}{l_{[40]}}\left(l_{[40]+1}+\ldots+l_{64}\right)} & {} \\
{=e_{[40]}-\frac{l_{64}}{l_{[40]}}e_{64}}& {\mbox{因为}e_{x}=E[K_{x}]=\sum_{k=0}^{\infty}k \cdot P(K_{x}=k)=\sum_{k=1}^{\infty}{_{k}p}_{x}=\sum_{k=1}^{\infty}\frac{l_{x+k}}{l_x}} 
\end{array}
$$

接下来查表即可。

最后附上两道真题的完整答案：

Solution 1: CT5 April 2008 Q11
![S1](https://qiniu.mdnice.com/e51d98fb067c620a2868a9251224a8d8.jpeg)
Solution 2: CT5 April 2011 Q12
![1](https://qiniu.mdnice.com/e30b554f7cf15300737a2304cea9792a.jpeg)
![2](https://qiniu.mdnice.com/8314ae72f87abade302a32328a1ce9a0.jpeg)
![3](https://qiniu.mdnice.com/5dcd43ee57affe69768fc790f462dddc.jpeg)
