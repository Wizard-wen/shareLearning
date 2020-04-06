# Regression(回归)
> 回归模型中主要涉及的参数是θ（包含x的系数和截距），回归寻找的是θ值使得损失函数（或者成本函数，通常用均方误差MSE来表示）最小。方法有：
* 标准方程
> 通过数学方程求解出最优值，直接代入公式
```
import numpy as np
x = 2 * np.random.rand(100,1)
y = 4 + 3 * x + np.random.randn(100,1)# rand是标准正态分布，randn是0-1之间随机数
x_b = np.c_[np.ones((100,1)),x]# np_c是按行连接，列数会增多，add x0=1 to each instance
theta_best = np.linalg.inv(x_b.T.dot(x_b)).dot(x_b.T).dot(y)
theta_best

x_new = np.array([[0],[2]])
x_b_new = np.c_[np.ones((2,1)),x_new]
y_predict = x_b_new.dot(theta_best)
y_predict

import matplotlib.pyplot as plt
plt.plot(x_new,y_predict,"r-")
plt.plot(x,y,"b.")
plt.axis([0,2,0,15])# axis指定的是x轴的值域和y轴的值域
plt.show()
```
* 梯度下降寻找最优解
> 涉及到的概念有：随机初始值、参数学习率。梯度下降的原理是使得参数θ朝着损失函数变小的方向调整，直至损失函数最小（或者小到规定的范围）为止。

> 其中，批量梯度下降的每一步都是基于完整的训练集来计算得出的。在拥有几十万个特性的训练模型中，梯度下降比标准方程要快得多。
```
eta = 0.1 # learning rate
n_iterations = 1000
m = 100

theta = np.random.randn(2,1) # random initialization
for iteration in range(n_iterations):
    gradients = 2/m * x_b.T.dot(x_b.dot(theta)-y)
    theta = theta - eta * gradients
```
> 使用梯度下降得到的θ值与标准方程得出的一致。

> 使用随机梯度下降（待补充）

> 小批量梯度下降
