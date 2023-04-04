---
title: General Adversarial Nets summary
feed: hide
date : 2022-12-22
time : 08:30:16
tags : [summary]
format: list
comments: true
---

![](/attachments/General_Adversarial_Nets_paper.jpeg)

Goodfellow 등은 생성 모델과 판별 모델을 사용하여 새로운 이미지를 생성할 수 있는 General Adversarial Network(GAN)을 제안하고, 이를 사용하여 이미지 생성, 영상 변환 등의 다양한 응용 분야에서 좋은 결과를 보였다.

# <특징>
- GAN은 **생성자(generator)** 와 **판별자(discriminator)** 라는 두 개의 신경망으로 이루어져 있으며, 이들을 **경쟁**시켜가며 이미지 생성 및 변환 작업을 수행한다.
    - *생성자는 실제 데이터와 유사한 가짜 데이터를 생성*하려고 노력하고, *판별자는 생성자가 생성한 데이터를 실제 데이터와 구별*하려고 노력한다.
    - GAN은 *생성자와 판별자가 경쟁*하면서 점점 더 좋은 성능을 내는 방식으로 학습된다.
- GAN은 **진짜 이미지와 생성된 가짜 이미지를 잘 구분할 수 있는 능력**을 갖춘다.
- GAN을 사용하면 **이미지 생성**, 영상 변환, 데이터 증강 등의 다양한 응용 분야에서 좋은 성능을 보여준다.

# <관련 논문>
- Radford, A., Metz, L., & Chintala, S. (2016). Unsupervised representation learning with deep convolutional generative adversarial networks. arXiv preprint arXiv:1511.06434.
- Isola, P., Zhu, J. Y., Zhou, T., & Efros, A. A. (2017). Image-to-image translation with conditional adversarial networks. In Proceedings of the IEEE conference on computer vision and pattern recognition (pp. 1125-1134).
- Karras, T., Aila, T., Laine, S., & Lehtinen, J. (2018). Progressive growing of GANs for improved quality, stability, and variation. arXiv preprint arXiv:1710.10196.
- Zhu, J. Y., Park, T., Isola, P., & Efros, A. A. (2017). Unpaired image-to-image translation using cycle-consistent adversarial networks. In Proceedings of the IEEE international conference on computer vision (pp. 2223-2232).
- Wang, T. C., Xu, M., Zhu, J. Y., Liu, K., Huang, S., & Metaxas, D. N. (2018). Video-to-video synthesis. In Advances in neural information processing systems (pp. 118-128).


_끝_
