---
layout: project
title: 'Robust multiview face clustering'
caption: Solving "who appears where" in movies.
description: >
  Self supervised mining of face images for robust face clustering in movies.
date: 1 Dec 2019
image: 
  path: assets/img/projects/faces.svg
links:
  - title: code
    url: https://github.com/usc-sail/mica-deep-mcca
  - title: paper
    url: https://arxiv.org/abs/2008.11289

accent_color: '#4fb1ba'
accent_image:
  background: '#193747'
theme_color: '#193747'
sitemap: false
featured: false
---

<details><summary><b>What is the need for robust face clustering in videos?</b></summary>
Robust face clustering is a key step towards computational understanding of visual character portrayals in media i.e., automatically extracting "who" appears "where" statistics. A first step toward developing such tools is the ability to automatically identify the characters in the visual modality i.e., the "who". 
This is a difficult task because characters are often portrayed with varying degrees of complexity with respect to appearance and design in different media forms 
</details>
<p></p>

<details><summary><b>
What are the challenges in video content?
</b></summary>
Face recognition and clustering in videos in the absence of domain-matched training data remains a challenging problem. 
In TV shows and movies, we need to robustly identify the characters in the presence of multiple "visual distractors" such as changes in appearance, background imagery, facial expression, size (resolution), view points (pose), illumination, partial detection (occlusion), and in some cases, age.
</details>
<p></p>

> **Our idea to mine weakly labeled face tracks**
We use self-supervised methods to harvest movie face tracks by exploiting temporally co-occurring faces in a video. Faces that belong to the same track are segmented into 'tracklets' that are used as positive samples. Faces from co-occurring tracks are used as hard-negatives. 
 
![Face tracklets](/assets/img/projects/hf-tracklets.svg)

> **Data details:**
The table below summarizes the face tracks extracted per our method. We use this dataset for adapting pre-trained face embeddings for movies.

Data/statistic                | Count 
:----------------------------:|:--------------------------------------:
No. Hollywood movies          | 240
Total no. tracks              | 335,845 (~1390 face tracks per movie)
Total no. co-occurring tracks | 169,201 (~726 face tracks per movie)
Total no. faces               | 10.2 million faces
Faces per track (mean, std.)  | 63.3, 9.1


> **Benchmarking dataset**
We augmented current video datasets used for benchmarking with more racially diverse datasets. 
A few exemplars from the Hidden Figures (2014) movie is shown below:

![Hidden figures](/assets/img/projects/hf-exemplars.svg)

The summary of the complete benchmarking dataset we created is shown below:

| movie_name         | Mean faces/track | No. tracks | No. characters | cluster density range
|--------------------|----------------|------------|----------------|---------------------|
| Hidden Figures (2016)     |          59.82 |       1407 |             24 |        0.57 - 20.11 |
| About Last Night (2014)   |          38.17 |       1565 |             10 |        1.02 - 31.37 |
| Maleficent (2014)         |          64.07 |        694 |             10 |        2.02 - 36.60 |
| Dumb and Dumber To (2014) |          70.77 |       1457 |             10 |        0.82 - 38.23 |
| Notting Hill (1999)       |          79.15 |       1435 |             12 |        1.25 - 40.77 |

We showed that adapting pre-trained face embeddings using the weakly labeled faces improve over face verification and face clustering perfrmance in movies. Please see our [preprint paper](https://arxiv.org/abs/2008.11289) for more details on experiments and results.
