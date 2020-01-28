# 【CM1】第4章 Time value of money
## 4.1 利率

债是最古老和最根本的金融活动。我们的社会本质上就是形形色色的债务关系的总和。维持庞大复杂的债务网络的核心，是债务的成本要均衡、稳定和可持续，而债务的成本，就是利率。费雪把利率定义为“现在消费和将来消费进行交换的价格”——资金有时间价值，所以让渡一部分的现在消费，就需要利息作为补偿或报酬。

我们对利息(率)（interest）给出如下定义：

利息(率)（interest）是货币在一定时期内的使用费，指货币持有者 (债权人, lender) 因贷出货币或货币资本（capital）而从借款人 (债务人, borrower) 手中获得的报酬。包括存款利息、贷款利息和各种债券发生的利息。


### 4.1.1 利率

- 利率的基本概念
  - Principal；Capital：本金.业务开始时投资的金额.
  - Accumulated value：积累值.业务结束时收回的总金额.
  - Interest：利息(率).积累值和本金之差.

- 单利 Simple interest
    假定本金为$C$，利率为$i$，则$n$年后的积累值为：$C\left(1 + n i\right)$
- 复利 Compound (effective) interest
    假定本金为$C$，利率为$i$，则$n$年后的积累值为：$C\left(1+i\right)^n$

练习4.1：
Calculate the length of time it will take £ 800 to accumulate to £1000 at a simple rate of interest of 4% pa.

解答：
The length of time can be found from the equation:
$$\begin {align*}
 &800(1+0.04t)=1000\\
  &\Rightarrow n=6.25years
 \end{align*}$$

### 4.1.2 积累因子

定义积累因子(Accumulation factor)$A(t_{1},t_{2})$为$t_{1}$时刻单位1的投资在$t_{2}$时刻的积累值. $A(0,n)$可以简写为$A(n)$.
- 单利的情况，在时间区间$(0,n)$上的积累因子：$A(n)=1+ni$
- 复利的情况,在时间区间$(0,n)$上的积累因子：$A(n)=(1+i)^{n}$

### 4.1.3 现值

$n$时刻的存款$C$在0时刻的现值(Present value):
$$
PV=\frac{C}{(1+i)^n}
$$

- 为便于书写， 定义函数$v=\tfrac{1}{1+i}$. 则现值的表达式可进一步简写为 $PV=Cv^{n}$
- $v^n$ 的值可以查 “Formulae and Tables for Examination”(**Tables**).

注意，题目中要求的四舍五入有两种表述：
$$
\left\{
\begin{array}{cc}
{\mbox{Significant figures}}&{\mbox{保留几位有效数字}}\\
{\mbox{Decimal places}}&{\mbox{保留几位小数}}
\end{array}
\right.
$$
## 4.2 贴现率
### 4.2.1 贴现率
- 单贴现率 Simple discount}
假定$n$时刻的存款为$C$，贴现率为$d$，0时刻的现值为：$C\left(1-nd\right)$
- 复贴现率 Compound (effective) discount}
假定$n$时刻的存款为$C$，贴现率为$d$，0时刻的现值为：$C\left(1-d\right)^n$

### 4.2.2 贴现因子

定义贴现因子(Discount factors) $v(n)$为$t$时刻1单位的积累值在0时刻的现值.则：
$$
v(n)=\frac{1}{A(n)}
$$

## 4.3 实际利率和实际贴现率
### 4.3.1 实际利率
记第$n$期（$n-1$时刻至$n$时刻）的实际利率为$i_{n}$ ，则：
$$
i_{n}=\frac{A(n)-A(n-1)}{A(n-1)}
$$
### 4.3.2 实际贴现率
记第$n$期（$n-1$时刻至$n$时刻）的实际贴现率为$d_{n}$ ，则：
$$
d_{n}=\frac{A(n)-A(n-1)}{A(n)}
$$
## 4.4 等价率
等价率(Equivalent rates)研究的是$i,d,v$三者之间的关系：
$$
C(1+i)^{-n}=Cv^{n}=C(1-d)^{n}
$$
$$
v=1-d
$$

$$
d=1-v=1-\frac{1}{1+i}=\frac{i}{1+i}=iv
$$

## 题型 4.1. 等价率
等价率问题：已知$i$,求出等价的$d$，或已知$d$,求出等价的$i$。

对待此类问题，直接列式：
$$
\mbox{积累因子}=\frac{1}{\mbox{贴现因子}}
$$
其中：
$$
\mbox{积累因子}=\left\{
\begin{array}{cc}
{1+ni} & {\mbox{单利}}\\
{(1+i)^n} & {\mbox{复利}}
\end{array}
\right.
$$
$$
\mbox{贴现因子}=\left\{\begin{array}{cc}
{1-nd} & {\mbox{单贴现率}}\\
{(1-d)^n} & {\mbox{复贴现率}}
\end{array}
\right.
$$

### 例题 4.1 (CT1 September 2011 Q1)

A 91-day treasury bill is issued by the government at a simple rate of discount of 8% per annum.

Calculate the annual effective rate of return obtained by an investor who purchases the bill at issue.

### 思路

  根据题意，直接列式：
$$
  1-nd=(1+i)^{-n}
$$
  其中，期限$n=\tfrac{91}{365}$, 单贴现率$d=8\%$. 求等价的复利$i$.

### 解

$$
\begin{align*}
 &\left(1-\frac{91}{365} \times 0.08\right)=(1+i)^{-\frac{91}{365}} \\
  &0.980055=(1+i)^{-\frac{91}{365}} \\
  &1+i=1.08416 \Rightarrow i=8.416\%
 \end{align*}
$$

## 第4章 习题
### Exercise 2: CT1 September 2018 Q1

An investor is considering two investments. One investment is a 91-day bond issued by a bank which pays a rate of interest of 4% per annum effective. The second is a 91-day treasury bill which pays out €100.

- (i) Calculate the price of the treasury bill and the annual simple rate of discount from the treasury bill if both investments are to provide the same effective rate of return. [3]
- (ii) Suggest one factor, other than the rate of return, which might determine which investment is chosen. [1] [Total 4]