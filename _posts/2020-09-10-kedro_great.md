---
published: false
title: Kedro + Great Expectations - how to test your data flow and detect data drift 
collection: cv
layout: single
author_profile: true
read_time: true
categories: [projects]
header :
    teaser : /assets/images/kedro_mlflow.png
comments : true
toc: true
toc_sticky: true
sidebar:
    nav: sidebar-sample
---

In the previous article, we managed to build a binary classifier to detect if patient had a pneumothorax or not. Neural networks commonly suffer from a lack of explainability. In this project, we will use a method called [Grad-CAM (Gradient-weighted Class Activation Mapping)](https://arxiv.org/abs/1610.02391) to visualize heatmaps on xray corresponding to the most important zones of the image for our classifier.

# What is Grad-CAM ?

