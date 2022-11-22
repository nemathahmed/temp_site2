---
layout: paper
categories: papers
permalink: papers/skelevision
id: skelevision
title: "SkeleVision: Towards Adversarial Resiliency of Person Tracking with Multi-Task Learning"
authors:
  - Nilaksh Das
  - ShengYun Peng
  - Duen Horng Chau
venue: ECCV Workshop (AROW)
year: 2022
url: /papers/skelevision
pdf: /papers/22_eccv_skelevision.pdf
type: paper
figure: /images/papers/22_eccv_skelevision.png
feature-title: SkeleVision&#58; Towards Adversarial Resiliency of Person Tracking with Multi-Task Learning
feature-description: "Multi-task learning improves tracker robustness"
image: /images/featured/22_eccv_skelevision.png
featured: true
feature-order: 5
selected: true
type: workshop
doi: 
bibtex: |-

  @article{das2022skelevision,
    title={SkeleVision: Towards Adversarial Resiliency of Person Tracking with Multi-Task Learning},
    author={Das, Nilaksh and Peng, Sheng-Yun and Chau, Duen Horng},
    journal={arXiv preprint arXiv:2204.00734},
    year={2022}
  }
---

Person tracking using computer vision techniques has wide
ranging applications such as autonomous driving, home security and
sports analytics. However, the growing threat of adversarial attacks raises
serious concerns regarding the security and reliability of such techniques.
In this work, we study the impact of multi-task learning (MTL) on
the adversarial robustness of the widely used SiamRPN tracker, in the
context of person tracking. Specifically, we investigate the effect of jointly
learning with semantically analogous tasks of person tracking and human
keypoint detection. We conduct extensive experiments with more powerful
adversarial attacks that can be physically realizable, demonstrating the
practical value of our approach. Our empirical study with simulated as
well as real-world datasets reveals that training with MTL consistently
makes it harder to attack the SiamRPN tracker, compared to typically
training only on the single task of person tracking.
