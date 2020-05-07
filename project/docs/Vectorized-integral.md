
## 一维积分

$$
\begin{equation}
\begin{aligned}
I(f) 
&= \int_{x_1}^{x_n}f(x)dx \\
&= \sum_{i=1}^{n} w_{i} f\left(x_{i}\right)+ R(n) \\
&\approx  \sum_{i=1}^{n} w_{i} f\left(x_{i}\right) 
\end{aligned}
\end{equation}
$$



不同的数值积分方法就是上面的$w_i$不同， 最简单的矩形积分法如下：
$$
\begin{equation}
\begin{aligned}
\int_{x_0}^{x_n}f(x)dx  
&\approx \sum_{i=1}^{n} f(x_i) \Delta x = \Delta x \sum_{i=1}^{n} f(x_i)\\
&= \frac{x_n - x_1}{n}\sum_{i=1}^{n} f(x_i)
\end{aligned}
\end{equation}
$$

复合一维积分：
$$
\begin{equation}
\begin{aligned}
\label{eq: integ1d}
I(f) &=\int_{x_1}^{x_n}f(x)g(x)dx
\approx \sum_{i=1}^{n} f(x_i)g(x_i) \Delta x = \Delta x \sum_{i=1}^{n} f(x_i)g(x_i)\\
&= \frac{x_n - x_1}{n} \vec{f(x)} \cdot \vec{g(x)}
\end{aligned}
\end{equation}
$$





##  二维积分

对于两个变量的积分的表达式，比如x和y，可以写成两种积分符号：
$$
\begin{equation}
\iint f(x, y) d x d y \text { 或者 } \, \int_{x_{1}}^{x_{2}} d x \int_{y_{1}(x)}^{y_{2}(x)} d y\ f(x, y) \label{integ2d}
\end{equation}
$$


其中，右边的形式可以更具体地表示积分界限，并给出了一个明确的指示，即y积分应该首先执行，或者使用单个积分符号，如
$$
\int_{S} f(x, y) d A
$$
其中S(如果显式显示)为二维积分区域，$dA$为“area” (在笛卡尔坐标系中，等于$dxdy$)

OK，这不是重点。

对于公式$(\ref{integ2d})$ ，将其中的$f(x,y)$变量分离为 $f_1(x)f_2(y)$ ，将得到：
$$
\label{sepa_value}
\int_{x_1}^{x_2} f_1(x)dx \int_{y_1(x)}^{y_2(x)} f_2(y)dy\\
$$

当然， 这可能不是我要的形式， 我希望的是：
$$
\begin{equation}
\begin{aligned}
&\int_{x_1}^{x_2} dx \int_{y_1(x)}^{y_2(x)}dy \ f_1(x)f_2(y)\\
&\approx  \Delta x \Delta y \sum_{i}^{N}\sum_{j}^{M}\ f_1(x_i)f_2(y_j) \\
&=\frac{x_2 - x_1}{N} \frac{y_2(x) - y_1(x)}{M} \sum \vec{f_1(x)} \otimes \vec{f_2(y)}
\end{aligned}
\end{equation}
$$






计算

一维：

$$
\pi = I(f) =\int_{0}^{1}\frac{4}{1+x^2}dx
$$

二维：
$$
\begin{equation}
I(f(x, y))=\int_{1}^{2} \int_{1}^{x} x y d x d y
\end{equation}
$$

$$
\begin{equation}
\begin{aligned}
\iint x y \, \mathrm{d} \sigma &=\int_{1}^{2}\left[\int_{1}^{x} x y \mathrm{d} y\right] \mathrm{d} x=\int_{1}^{2}\left[x \cdot \frac{y^{2}}{2}\right]_{1}^{x} \mathrm{d} x \\
&=\int_{1}^{2}\left(\frac{x^{3}}{2}-\frac{x}{2}\right) \mathrm{d} x=\left[\frac{x^{4}}{8}-\frac{x^{2}}{4}\right]_{1}^{2}=\frac{9}{8}
\end{aligned}
\end{equation}
$$



<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=1357887419&auto=1&height=66"></iframe>

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//m701.music.126.net/20200420224318/19165a21a4c14b56c4c68ebc426a4895/jdymusic/obj/w5zDlMODwrDDiGjCn8Ky/1725475066/3331/2c9c/071e/8e263c1b9f85e79330f40868a68ce22a.mp3"></iframe>




<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=7625249&auto=1&height=66"></iframe>
