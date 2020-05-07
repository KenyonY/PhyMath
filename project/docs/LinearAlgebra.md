# REVIEW 

一个向量$\mathbf{A}$可以用一个单列矩阵 $\mathbf{a}$ 来表示，它的元素是A的分量:
$$
\mathbf{A} \Longrightarrow \mathbf{a}=\left(\begin{array}{l}
A_{1} \\
A_{2} \\
A_{3}
\end{array}\right) \notag
$$
表示向量$\mathbf{A}$的矩阵的转置是一个单行矩阵，称为行向量:
$$
\mathbf{a}^{T}=\left(A_{1} \quad A_{2} \quad A_{3}\right) \notag
$$

### 点积(Dot Product)  [ 内积(Inner  Product)]：

$\mathbf{A} \cdot \mathbf{B}$ 可由$\mathbf{a}^{T} \mathbf{b}$ 表示，或者若 $\mathbf{a}$ 和$\mathbf{b}$ 都为实，有$\mathbf{a}^†\mathbf{b}$。此外，$\mathbf{a}^ T \mathbf{b} = \mathbf{b}^ T \mathbf{a}$。
$$
\begin{equation}
\begin{aligned}
\mathbf{A} \cdot \mathbf{B}&=\mathbf{a}^{T} \mathbf{b}=\left(\begin{array}{lll}
A_{1} & A_{2} & A_{3}
\end{array}\right)\left(\begin{array}{l}
B_{1} \\
B_{2} \\
B_{3}
\end{array}\right)\\
&=A_{1} B_{1}+A_{2} B_{2}+A_{3} B_{3}\\
&=\sum_{i}A_i B_i \\
\end{aligned}
\end{equation}
$$

在此，给出一个之后将用到的简单示例:

对于
$$
\begin{equation}
A=\left(\begin{array}{l}
1 \\
2 \\
3
\end{array}\right), \quad B=\left(\begin{array}{lll}
4 & 5 & 6
\end{array}\right)
\notag
\end{equation}
$$
给出矩阵内积 $AB $ 以及 $B A$
$$
\begin{equation}
\label{example1}
A B=\left(\begin{array}{rrr}
4 & 5 & 6 \\
8 & 10 & 12 \\
12 & 15 & 18
\end{array}\right), \quad B A=(4 \times 1+5 \times 2+6 \times 3)=(32)\end{equation}
$$




### 叉积( Cross Product)  [ 外积(Outer Product)]：

$\mathbf{A} \times \mathbf{B}$  定义：
$$
\mathbf{C}=\mathbf{A} \times \mathbf{B}=(A B \sin \theta) \hat{\mathbf{e}}_{c}
$$
满足反交换律：
$$
\mathbf{B} \times \mathbf{A}=-\mathbf{A} \times \mathbf{B}
$$
也满足分配律：
$$
\mathbf{A} \times(\mathbf{B}+\mathbf{C})=\mathbf{A} \times \mathbf{B}+\mathbf{A} \times \mathbf{C}, \quad k(\mathbf{A} \times \mathbf{B})=(k \mathbf{A}) \times \mathbf{B}
$$
引入 Levi-Civita 符号  $\varepsilon_{i j k}$ 
$$
\begin{equation}
\hat{\mathbf{e}}_{i} \times \hat{\mathbf{e}}_{j}=\sum_{k} \varepsilon_{i j k} \hat{\mathbf{e}}_{k}
\end{equation}
$$
该符号表示，如 
$$
\hat{\mathbf{e}}_{x} \times \hat{\mathbf{e}}_{x}=0 ,\quad
\hat{\mathbf{e}}_{x} \times \hat{\mathbf{e}}_{y}=\hat{\mathbf{e}}_{z} ,\quad
\hat{\mathbf{e}}_{y} \times \hat{\mathbf{e}}_{x}=-\hat{\mathbf{e}}_{z}
$$


那么我们展开$\mathbf{A} \times \mathbf{B}$ ，得到：
$$
\begin{equation}
\begin{aligned}
\mathbf{C}=& \mathbf{A} \times \mathbf{B}=\left(A_{x} \hat{\mathbf{e}}_{x}+A_{y} \hat{\mathbf{e}}_{y}+A_{z} \hat{\mathbf{e}}_{z}\right) \times\left(B_{x} \hat{\mathbf{e}}_{x}+B_{y} \hat{\mathbf{e}}_{y}+B_{z} \hat{\mathbf{e}}_{z}\right) \\
=&\left(A_{x} B_{y}-A_{y} B_{x}\right)\left(\hat{\mathbf{e}}_{x} \times \hat{\mathbf{e}}_{y}\right)+\left(A_{x} B_{z}-A_{z} B_{x}\right)\left(\hat{\mathbf{e}}_{x} \times \hat{\mathbf{e}}_{z}\right) \\
&+\left(A_{y} B_{z}-A_{z} B_{y}\right)\left(\hat{\mathbf{e}}_{y} \times \hat{\mathbf{e}}_{z}\right) \\
=&\left(A_{x} B_{y}-A_{y} B_{x}\right) \hat{\mathbf{e}}_{z}+\left(A_{x} B_{z}-A_{z} B_{x}\right)\left(-\hat{\mathbf{e}}_{y}\right)+\left(A_{y} B_{z}-A_{z} B_{y}\right) \hat{\mathbf{e}}_{x} \\
\label{cross}
\end{aligned}
\end{equation}
$$
于是$\mathbf{C}$ 的各个分量为：
$$
C_{x}=A_{y} B_{z}-A_{z} B_{y}, \quad C_{y}=A_{z} B_{x}-A_{x} B_{z}, \quad C_{z}=A_{x} B_{y}-A_{y} B_{x} \notag
$$
即：
$$
\begin{equation}
C_{i}=\sum_{j k} \varepsilon_{i j k} A_{j} B_{k} \label{cross1}
\end{equation}
$$
当然，公式$(\ref{cross}) (\ref{cross1})$也可表示为行列式形式：
$$
\begin{equation}
\mathbf{C}=\left|\begin{array}{lll}
\hat{\mathbf{e}}_{x} & \hat{\mathbf{e}}_{y} & \hat{\mathbf{e}}_{z} \\
A_{x} & A_{y} & A_{z} \\
B_{x} & B_{y} & B_{z}
\end{array}\right| \label{lalal}
\end{equation}
$$

### 直积/ 克罗内克积（Direct Product/  Kronecker product）：

将$m×n$矩阵$\mathbf{A}$与$m'× n'$矩阵$\mathbf{B}$结合得到直积矩阵 $\mathrm{C}=\mathrm{A} \otimes \mathrm{B}$ ,其维度为$m m^{\prime} \times n n^{\prime}$ ，具体例子如下：

如果A和B都是2×2矩阵，我们可以这样写，先用符号形式，然后用完全展开的形式
$$
\begin{equation}\mathrm{A} \otimes \mathrm{B}=\left(\begin{array}{ll}
a_{11} \mathrm{B} & a_{12} \mathrm{B} \\
a_{21} \mathrm{B} & a_{22} \mathrm{B}
\end{array}\right)=\left(\begin{array}{llll}
a_{11} b_{11} & a_{11} b_{12} & a_{12} b_{11} & a_{12} b_{12} \\
a_{11} b_{21} & a_{11} b_{22} & a_{12} b_{21} & a_{12} b_{22} \\
a_{21} b_{11} & a_{21} b_{12} & a_{22} b_{11} & a_{22} b_{12} \\
a_{21} b_{21} & a_{21} b_{22} & a_{22} b_{21} & a_{22} b_{22}
\end{array}\right)\end{equation}
$$
另一个例子是两个两元列向量x和y的直接乘积，还是先写符号，然后扩展形式
$$
\begin{equation}\left(\begin{array}{l}
x_{1} \\
x_{2}
\end{array}\right) \otimes\left(\begin{array}{l}
y_{1} \\
y_{2}
\end{array}\right)=\left(\begin{array}{l}
x_{1} \mathbf{y} \\
x_{2} \mathbf{y}
\end{array}\right)=\left(\begin{array}{l}
x_{1} y_{1} \\
x_{1} y_{2} \\
x_{2} y_{1} \\
x_{2} y_{2}
\end{array}\right)\end{equation}
$$
第三个例子是来自例子等式$(\ref{example1})$ :

它是特殊情况下的一个实例(列向量乘以行向量)，其中直积和内积重合: $AB =A \otimes B$ 









<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=761323&auto=1&height=66"></iframe>