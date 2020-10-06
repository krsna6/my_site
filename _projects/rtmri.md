---
layout: project
title: 'Tracking vocal tract in real-time MRI'
caption: Neural networks for semantic edge detection.
description: >
  Convolutional encoder-decoder models to track articulators of human vocal tract in real-time MRI.
date: '08-01-2017'
image: 
  path: assets/img/projects/rtmri.svg
links:
  - title: code
    url: https://github.com/krsna6/rtmri-segnet
  - title: dataset
    url: https://sail.usc.edu/span/test-retest
  - title: poper
    url: http://sipi.usc.edu/~toutios/pdfs/somandepalli2017semantic.pdf
accent_color: '#4fb1ba'
accent_image:
  background: '#193747'
theme_color: '#193747'

sitemap: false
---

Real-time MRI can help understand human speech product processes. Automatic segmentation of articulators (e.g., tongue, lips) is vital for study of vocal tract dynamics in rtMRI.
The overall methodology and examples are shown below. For more details, see the [paper](http://sipi.usc.edu/~toutios/pdfs/somandepalli2017semantic.pdf)

Inspired by semantic segmentation work, we propose a full convolutional encoder-decoder network to predict articulatory boundaries (colored lines shown on the MRI image in Fig. 2). The model performance was further improve by adding a penalty to the loss function to peanalize heavily when articulator pixels are confused with that of air vs. tissue. This helped reinforce the tissue boundary segmentation with a higher confidence.

![](/assets/img/projects/rtmri_all.png)

<!-- **hy-drawer** is a touch-enabled drawer component for the modern web. It focuses on providing a fun, natural feel in both the Android and iOS stock browser, while being performant and easy to use. It is the perfect companion for mobile-first web pages and progressive web apps.

> A touch-enabled drawer component for the modern web.
{:.lead}

**hy-drawer** is used by hundreds of sites as part of the [Hydejack] Jekyll theme.

[hydejack]: ../README.md -->
