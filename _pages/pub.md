---
layout: archive
permalink: /pub/
author_profile: true
title: "论文"
---


## Improving Barely Supervised Learning by Discriminating Unlabeled Samples with Super-Class
[[PDF]](https://openreview.net/pdf?id=Nlsr4DepNt) [[Poster]](https://nips.cc/media/PosterPDFs/NeurIPS%202022/54238.png)

### Published in Neural Information Processing Systems (NeurIPS), 2022

**Abstract** In semi-supervised learning (SSL),  a common practice is to learn consistent information from unlabeled data and discriminative information from labeled data to ensure both the immutability and the separability of the classification model.  Existing SSL methods  suffer from failures in barely-supervised learning (BSL), where only one or two labels per class are available, as the insufficient labels cause the discriminative information being difficult or even infeasible to learn. To bridge this gap, we investigate a simple yet effective way to leverage unlabeled samples for discriminative learning, and propose a novel discriminative information learning module to benefit model training. Specifically, we formulate the learning objective of discriminative information at the super-class level and dynamically assign different classes into different super-classes based on  model performance improvement. On top of this on-the-fly process, we further propose a distribution-based loss to learn discriminative information by utilizing the similarity relationship between samples and super-classes. It encourages the  unlabeled samples to stay closer to the distribution of their corresponding super-class than those of others. Such a constraint is softer than the direct assignment of pseudo labels, while the latter could be very noisy in BSL. We compare our method with state-of-the-art SSL and BSL methods through extensive experiments on standard SSL benchmarks. Our method can achieve superior results, \eg, an average accuracy of 76.76% on CIFAR-10 with merely 1 label per class.


## Enhancing Sample Utilization through Sample Adaptive Augmentation in Semi-Supervised Learning

### Published in Neural International Conference on Computer Vision (ICCV), 2023
[[PDF]](https://arxiv.org/abs/2309.03598)
**Abstract** In semi-supervised learning, unlabeled samples can be utilized through augmentation and consistency regularization. 
However, we observed certain samples, even undergoing strong augmentation, are still correctly classified with high confidence, resulting in a loss close to zero. 
It indicates that these samples have been already learned well and do not provide any additional optimization benefits to the model. We refer to these samples as ``naive samples".
Unfortunately, existing SSL models overlook the characteristics of naive samples, and they just apply the same learning strategy to all samples. 
To further optimize the SSL model, we emphasize the importance of giving attention to naive samples and augmenting them in a more diverse manner.
Sample adaptive augmentation (SAA) is proposed for this stated purpose and consists of two modules: 1) sample selection module; 2) sample augmentation module. 
Specifically, the sample selection module picks out {naive samples} based on historical training information at each epoch, then the naive samples will be augmented in a more diverse manner in the sample augmentation module.
Thanks to the extreme ease of implementation of the above modules, SAA is advantageous for being simple and lightweight. We add SAA on top of FixMatch and FlexMatch respectively, and experiments demonstrate SAA can significantly improve the models.
For example, SAA helped improve the accuracy of FixMatch from 92.50\% to 94.76\% and that of FlexMatch from 95.01\% to 95.31\% on CIFAR-10 with 40 labels. The code can be downloaded in supplementary materials.

