---
title: Host load prediction with long short-term memory in cloud computing
author: birdlegend
date: 2018-05-13 16:53:13
categories:
- 论文
- 负载预测
tags:
- 论文
- 负载预测
---

## 文献信息
JCR 四区

#### 期刊
 Journal of Supercomputing

Source: Journal of Supercomputing, p 1-15, April 27, 2017;  ISSN: 09208542,  E-ISSN: 15730484;  DOI: 10.1007/s11227-017-2044-4; Publisher: Springer New York LLC

## 总结
In this paper, we propose a concise method based on the long short-term memory model for host load prediction. It can predict the mean load over consecutive future time intervals as well as the actual load over a long-term single interval due to the powerful ability of learning long-term dependencies. Two real-world load traces including the traditional grid system and cloud environment were used to evaluated our proposed method. According to previous experiment results, traditional methods may perform well in the grid while degrading when applied to a cloud. However, the LSTM model shows a well-adaptive capability and achieves start-of-the-art results in both datasets. Our future work is to improve the method into a real-time model which will benefit a lot when applied to real-world host load prediction.


## 摘抄

#### ReLUs
> we use the rectified linear units (ReLUs) function which is also a nonlinear activation function but can be trained several times faster [13]


- KrizhevskyA,SutskeverI,HintonGE(2012)Imagenetclassificationwithdeepconvolutionalneural
networks. In: Advances in neural information processing systems, pp 1097–1105

#### Mean load prediction
> The mean segment squared error (MSSE) defined as follows was applied to quantify the performance of mean load prediction:
More details are presented in [4].

- DiS,KondoD,CirneW(2012)HostloadpredictioninaGooglecomputecloudwithaBayesianmodel. In: Proceedings of the International Conference on High Performance Computing, Networking, Storage and Analysis. IEEE Computer Society Press, p 21