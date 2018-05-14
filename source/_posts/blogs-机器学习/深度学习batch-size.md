---
title: 深度学习
author: birdlegend
date: 2018-05-13 18:57:51
categories:
- machine learning
- deep learning
tags:
- machine learning
- deep learning
---

## 参数详解
### Batch_Size
batch size为一次训练使用样本数。

[训练神经网络时如何确定batch size？](https://zhuanlan.zhihu.com/p/27763696)

[谈谈深度学习中的 Batch_Size](https://blog.csdn.net/ycheng_sjtu/article/details/49804041)
[https://stats.stackexchange.com/questions/153531/what-is-batch-size-in-neural-network?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa](https://stats.stackexchange.com/questions/153531/what-is-batch-size-in-neural-network?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)


#### 举例
由此，最直观的超参数就是batch的大小——我们可以一次性将整个数据集喂给神经网络，让神经网络利用全部样本来计算迭代时的梯度（即传统的梯度下降法），也可以一次只喂一个样本（即随机梯度下降法，也称在线梯度下降法），也可以取个折中的方案，即每次喂一部分样本让其完成本轮迭代（即batch梯度下降法）。

数学基础不太好的初学者可能在这里犯迷糊——一次性喂500个样本并迭代一次，跟一次喂1个样本迭代500次相比，有区别吗？

其实这两个做法就相当于：

第一种：
total = 旧参下计算更新值1+旧参下计算更新值2+...+旧参下计算更新值500 ;
新参数 = 旧参数 + total

第二种：
新参数1 = 旧参数 + 旧参数下计算更新值1；
新参数2 = 新参数1 + 新参数1下计算更新值1；
新参数3 = 新参数2 + 新参数2下计算更新值1；
...
新参数500 =
新参数500 + 新参数500下计算更新值1；

也就是说，第一种是将参数一次性更新500个样本的量，第二种是迭代的更新500次参数。当然是不一样的啦。

那么问题来了，哪个更好呢？