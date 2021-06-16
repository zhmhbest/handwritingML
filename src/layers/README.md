# Layer

[TOC]

## Softmax

把一个序列，变成概率。Softmax是一种非常明显的**马太效应**（强的更强，弱的更弱）。但是这种方法非常的不稳定。因为要算指数，只要输入稍微大一点，则在计算上一定会溢出。

$$
\mathrm{Softmax}\left(
    \left[\begin{array}{c}
        a_1 \\ a_2 \\ \vdots \\ a_n
    \end{array}\right]
\right) = \left[\begin{array}{c}
        \dfrac{e^{a_1}}{\sum_{i=1}^{n}e^{a_i}}
    &   \dfrac{e^{a_2}}{\sum_{i=1}^{n}e^{a_i}}
    &   \cdots
    &   \dfrac{e^{a_n}}{\sum_{i=1}^{n}e^{a_i}}
\end{array}\right]^T
$$