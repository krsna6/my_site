---
layout: project
title: 'Multimodal affect tracking'
caption: Multimodal Kalman filters tracking arousal and valence.
description: >
  Self supervised mining of face images for robust face clustering in movies.
date: 1 Dec 2016
image: 
  path: assets/img/projects/affect.jpg
links:
  - title: paper
    url: https://dl.acm.org/doi/abs/10.1145/2988257.2988259

accent_color: '#4fb1ba'
accent_image:
  background: '#193747'
theme_color: '#193747'
sitemap: false
featured: false
---

> **Dimensional affect representation**
While there are different ways of measuring affect dimensionally, two methods are predominantly used: (1) discrete classes of pre-determined emotion and (2) continuous dimensional scales of arousal, valence and dominance. The video below demonstrates one such application on movie videos (Courtesy: [Malandrakis et. al., 2011](https://sail.usc.edu/~malandra/files/papers/icassp2011.pdf))

<iframe width="420" height="315"
src="
https://www.youtube.com/embed/qZBUzD5i1yI
">
</iframe>

> **Dataset explored by our work**
We participated in the Multimodal Affect Recognition Sub-Challenge (MASC) of AVEC 2016. The AVEC 2016 challenge uses the REmote COLlaborative and Affective interactions ([RECOLA](https://diuf.unifr.ch/main/diva/recola/)) dataset for the Multimodal Affect Recognition Sub-Challenge (MASC). The RECOLA dataset consists of synchronized and continuous data from multiple modalities recorded during dyadic interactions in French on a video conference that requires completion of a collaborative task. It offers a good testbed for evaluating the tracking of arousal and valence using multimodal signals such as voice, facial expressions and physiological data in a relatively constrained setup.

> **Our approach**
We propose a continuous affective state tracking system based on linear dynamical models with Kalman filters. Our approach is inspired from the fact that arousal and valence are latent affective dimensions, thus making online state tracking systems such as Kalman filters a suitable choice. 
We modify the Kalman filtering scheme to incorporate the multimodal nature of this problem by accounting for the presence or absence of input modalities using a conditional framework as illustrated below:

![multimodal kalman](/assets/img/projects/varimodal.svg)

> **Unimodal performance**
We used the [concordance correlation coefficient](https://en.wikipedia.org/wiki/Concordance_correlation_coefficient) (**CCC**) as the evaluation metric used to compare submissions for the challenge task. The unimodal performance is summarixe below:

Modality | Arousal | Valence  |
--------:|:--------:|:--------|
Audio | 0.80 | 0.45 |
Video-appearance | 0.48 | 0.47 |
Video-geometric | 0.30 | 0.61 |
Electro-dermal activity | 0.08 | 0.18 |
ECG | 0.27 | 0.16 |
Heart rater variability | 0.38 | 0.29 |

> **Multimodal performance**
We compared our CCC performance with that of the challenge baseline using three different configurations as described below. All metrics were estimated in a Leave-one-subject-out (LOSO) setting to obtain stable estimates of CCC.
- **System 1**: Track arousal and valence separately using all modalities without a conditional framework to pick modalities.
- **System 2**: Track arousal first and use the predicted arousal as an additional observation to track valence using all modalities and no conditional framework.
- **System 3**: Track arousal first and use the predicted arousal to track valence with a conditional framework that decides which modality to pick depending on the available meta-data such as voicing probability to choose audio stream and presence of face to choose video stream.

Method | Arousal | Valence |
------:|:---------:|:-------|
*Development Set* | | |
Challenge baseline | 0.79 | 0.66 |
System 1 | 0.78 | 0.62 |
System 2 | 0.78 | 0.70 |
System 3 | 0.82 | 0.72 |
*Test Set* | | |
Challenge baseline | 0.68 | 0.64 |
System 3 | 0.70 | 0.68 |

> **Highlights**
- We employ linear dynamical systems to model unimodal predictions from trained regressors to initially predict arousal and then use the predicted arousal as an additional observation for valence prediction in an online fashion using Kalman filters.
- We propose a conditional framework to select from different multimodal Kalman filters while performing online tracking based on cues that incorporate observability of audiovisual data. 
- The proposed approach could be adopted for general behavioral coding and affective computing where different dimensions/classes are inter-correlated.


