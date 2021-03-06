---
published: true
title: Efficientnet classifier interpretation using GradCAM - part 3 of 3
collection: cv
layout: single
author_profile: true
read_time: true
categories: [projects]
header :
    teaser : /assets/images/2020-07-26-xray-classif-gradcam/gradcam_1.png
comments : true
toc: true
toc_sticky: true
sidebar:
    nav: sidebar-sample
---

In the previous article, we managed to build a binary classifier to detect if patient had a pneumothorax or not. Neural networks commonly suffer from a lack of explainability. In this project, we will use a method called [Grad-CAM (Gradient-weighted Class Activation Mapping)](https://arxiv.org/abs/1610.02391) to visualize heatmaps on xray corresponding to the most important zones of the image for our classifier.

# What is Grad-CAM ?

