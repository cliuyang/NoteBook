<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>

# 概率论与数理统计

## 第一章 概率论基础

定义：

1. 随机试验的一切可能的基本结果组成的集合称为**样本空间**，记为$\Omega = \{\omega\}$，其中$\omega$表示基本结果，又称**样本点**。
2. 随机试验的若干个基本结果组成的集合称为**随机事件**，简称**事件**，只含有一个基本结果的事件称为**基本事件**。
3. 设$E$为任一随机试验，$A$为其中任一事件，在相同的条件下，把$E$独立地重复做$n$次，$n_a$表示事件$A$在这$n$次试验中发生的次数，称为**频数**，比值$f_a(A) = \frac{n_A}{n}$称为事件$A$发生的**频率**。
   性质：
   1. 对于任一事件$A$，有$0 \leq f_n(A) \leq 1$；
   2. 对于必然事件$\Omega$，有$f_n(\Omega) = 1$；
   3. 对于互不相容的事件$A$，$B$，有 $$f_n(A \cup B) = f_n(A) + f_n(B)$$

4. 设有随机试验$E$，若当实验的次数$n$充分大时，事件$A$发生的频率$f_n(A)$稳定在某数$p$附近，则称数$p$为事件$A$发生的**概率**，记位$P(A) = p$。
5. 设$\Omega$是一随机试验的样本空间，对于该随机试验的每一个事件$A$赋予一个驶数，记位$P(A)$，称事件发生的**概率**，如果函数$P(\cdot)$满足以下公理：
   1. 非负性：对于每一个事件$A$，有$P(A) \geqslant 0$；
   2. 规范性：对于必然事件$\Omega$，有$P(\Omega) = 1$；
   3. 可列可加性：设$A_1, A_2, \cdots$是两两互不相容的事件，即对于$i \neq j, A_iA_j = \varnothing, i,j = 1, 2, \cdots$，则有 $$P(A_1 \cup A_2 \cup \cdots) = P(A_1) + P(A_2) + \cdots$$

   性质：
   1. $P(\varnothing) = 0$
   2. （有限可加性）若$A_1, A_2, \cdots, A_n$是两两互不相容的事件，则有 $$P(A_1 \cup A_2 \cup \cdots \cup A_n) = P(A_1) + P(A_2) + \cdots + P(A_n)$$
   3. 对任一事件$A$有 $$P(\overline{A}) = 1 - P(A)$$
   4. 对任意两个事件$A$，$B$有 $$P(A - B) = P(A) - P(AB)$$
   5. （加法公式）对于任意两事件$A$，$B$有 $$P(A \cup B) = P(A) + P(B) - P(AB)$$

6. 设$A$与$B$是同一样本空间中的两个事件，若$P(A) > 0$，则称 $$P(B \vert A) = \frac{P(AB)}{P(A)}$$ 为在事件$A$发生下的事件$B$发生的**条件概率**。
7. 设$A$，$B$是两个事件，如果$P(AB) = P(A)P(B)$，则称$A$与$B$**相互独立**。
8. 设$A$，$B$，$C$为三个事件，如果等式 $$P(AB) = P(A)P(B)$$ $$P(BC) = P(B)P(C)$$ $$P(AC) = P(A)P(C)$$ $$P(ABC) = P(A)P(B)P(C)$$ 都成立，则称事件$A$，$B$，$C$**相互独立**。
9. 如果第一次实验的任一结果，第二次实验的任一结果，……，第$n$次实验的任一结果都是相互独立的事件，则称这$n$次**实验相互独立**。如果这$n$次独立实验还是相同的，则称 **$n$重独立重复实验**。如果在$n$重独立重复试验中，每次试验的可能结果为两个：$A$或$\overline{A}$，则称这种实验为 **$n$重伯努利试验**。

定理

1. 设$A$与$B$是同一样本空间的两个事件，如果$P(A) > 0$，则 $$P(AB) = P(A)P(B \vert A)$$ 如果$P(B) > 0$，则 $$P(AB) = P(B)P(A \vert B)$$ 上面两式均称为事件概率的**乘法公式**。
2. 设试验$E$的样本空间为$\Omega$，$A_1, A_2, \cdots, A_n$为E的一组事件，且满足：
   1. $A_1, A_2, \cdots, A_n$两两互不相容，$P(A_i) > 0, i = 1, 2, \cdots, n$；
   2. $\bigcup\limits_{i = 1}^{n} = \Omega$

   称满足这两条件的事件组$A_1, A_2, \cdots, A_n$为**完备事件组**或**样本空间的一个划分**。
   则对任一事件$B$，有 $$P(B) = \sum\limits_{i=1}^{n}P(A_i)P(B \vert A_i)$$ 称之为**全概率公式**。

3. 设试验$E$的样本空间为$\Omega$，$B$为$E$的事件，$A_1, A_2, \cdots, A_n$为完备事件组，且$P(B) > 0, P(A_i) > 0, i = 1, 2, \cdots, n$，则 $$P(A_i \vert B) = \frac{P(A_i)P(B \vert A_i)}{\sum\limits_{j=1}^{n}P(A_j)P(B \vert A_j)}, i = 1, 2, \cdots, n,$$ 式称为**贝叶斯公式**。
