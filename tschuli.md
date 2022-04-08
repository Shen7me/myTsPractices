- 什么是截尾和拖尾？
  （1）p阶自回归模型 AR(P)
  AR(p)模型的偏自相关函数PACF在p阶之后应为零，称其具有截尾性；
  AR(p)模型的自相关函数ACF不能在某一步之后为零（截尾），而是按指数衰减（或成正弦波形式)，称其具有拖尾性。
  （2）q阶移动平均模型 MA(q)
  MA(q)模型的自相关函数ACF在q阶之后应为零，称其具有截尾性；
  MA(q)模型的偏自相关函数PACF不能在某一步之后为零（截尾），而是按指数衰减（或成正弦波形式)，称其具有拖尾性。

- 如何判断拖尾和截尾？
  （1）如果样本自相关系数（或偏自相关系数）在最初的d阶**明显大于2倍标准差范围**，而后几乎95%的样本自相关（偏自相关）系数**都落在2倍标准差范围以内**，而且由非零自相关（偏自相关）系数衰减为小值波动的过程非常突然，这时，通常视为自相关（偏自相关）系数截尾。
  （2）如果有超过5%的样本相关系数落在2倍标准差范围以外，或者是由显著非零的相关函数衰减为小值波动的过程**比较缓慢或者非常连续**，这时，通常视为相关系数**不截尾**。

  原文链接：https://blog.csdn.net/xianyuhenxian/article/details/60602828

  ---

  这里图1明显的拖尾，图2是PACF在点7截尾，所以应是AR(7)或者应该是AR(8)

  图中的蓝色阴影区域是显着性水平
  
  （蓝色可以不考虑，所以有5个是显著性滞后）

![img](https://img-blog.csdnimg.cn/20200930201616403.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MTAxMzMyMg==,size_16,color_FFFFFF,t_70#pic_center)

https://blog.csdn.net/weixin_41013322/article/details/108801516

---

![image-20220408181742757](C:\Users\shen7\AppData\Roaming\Typora\typora-user-images\image-20220408181742757.png)

![image-20220408174445087](C:\Users\shen7\AppData\Roaming\Typora\typora-user-images\image-20220408174445087.png)

由ACF和PACF判断p,q值！AR和MA容易判断。:apple:AR看PACF，MA看ACF

ARMA的ACF和PACF都呈现拖尾，我tm看不懂啊，ACF在点4之后可能全部落在两倍标准差里了,选q=4，PACF那个p=2真不知道咋看的。