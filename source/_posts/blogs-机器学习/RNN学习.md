---
title: RNN学习
author: birdlegend
date: 2018-05-04 14:38:08
categories:
- machine learning
- deep learning
tags:
- machine learning
- deep learning
- RNN
---

## 参考文献
- [7.循环神经网络(RNN) 基础讲解](https://www.jianshu.com/p/9f155515bdf0)

## 简介
> RNNs之所以称为循环神经网路，即一个序列当前的输出与前面的输出也有关。具体的表现形式为网络会对前面的信息进行记忆并应用于当前输出的计算中，即隐藏层之间的节点不再无连接而是有连接的，并且隐藏层的输入不仅包括输入层的输出还包括上一时刻隐藏层的输出。理论上，RNNs能够对任何长度的序列数据进行处理。

作者：_木豆_
链接：https://www.jianshu.com/p/9f155515bdf0
來源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。


## RNN的基本结构
> RNNs包含输入单元(Input units)，输入集标记为{x0,x1,...,xt,xt+1,...}，而输出单元(Output units)的输出集则被标记为{y0,y1,...,yt,yt+1.,..}。RNNs还包含隐藏单元(Hidden units)，我们将其输出集标记为{h0,h1,...,ht,ht+1,...}，这些隐藏单元完成了最为主要的工作。  
作者：_木豆_
链接：https://www.jianshu.com/p/9f155515bdf0
來源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

![RNN主要公式](https://upload-images.jianshu.io/upload_images/6162555-c241b388d93c7a3c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/554)

![一个RNN的小例子](一个RNN的小例子.png)

## RNN确定
#### 梯度消失问题(gradient vanish)
- 采用 LSTM 解决梯度消失

## LSTM神经网络输入输出究竟是怎样的？
https://www.zhihu.com/question/41949741?sort=created