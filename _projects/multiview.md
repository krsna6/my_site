---
layout: project
featured: true
show_collection: multi_view
title: Generalized Multiview Representation Learning
caption: Scalable multiview learning
description: >
  This is a central contrbution of my PhD dissertation.
date: 1 Jan 2020
image: /assets/img/projects/multiview.svg
links:
  - title: code
    url: https://github.com/usc-sail/gen-dmcca
  - title: speech application
    url: https://www.isca-speech.org/archive/Interspeech_2019/pdfs/3130.pdf
  - title: theoretical guarantees
    url: https://arxiv.org/abs/2005.06038
accent_color: '#4fb1ba'
accent_image:
  background: '#193747'
theme_color: '#193747'
sitemap: false
hide_description: true
---

<details><summary><b>What are multiple views and modalities?</b></summary>Data that is sampled from observing an event with different instruments to capture its various presentations. For example, consider the task of identifying the wake word(s) "OK Google" or "Alexa" regardless of age, accent, acoustic background and other factors, different variations of a given wake word are multiple views of the underlying task, i.e., recognizing the wake word. Another example is understanding the topic of a video using sound design, visuals and language as multiple modalities.</details>
<p></p>

<details><summary><b>Why do multiview learning?</b></summary>
<img src="/assets/img/why_multiview_learning.svg" alt="why do multiview learning">
<p></p>
So can machines. Learning from different devices or instruments observing multiple aspects of an underlying event can help build robust machine learning models.
</details>

> **Open research questions addressed by this work:**
- How can we model multiple views/modalities in parallel?
  - There is a need to develop methods that scale for a large number (>2) of views.
  - Need for view-agnostic methods i.e., having view-correspondence but not details of view acquistion
- Developing mechanisms for multimodal "disentanglement"
  - How to disocciate modality-specific information and shared information across modalities?
  - Need for generalizable unsupervised and self-supervised methodologies.

> **Central idea of this work:**
- Inherent variability of a semantic class can be uncorrelated across multiple views in the data
- Maximizing multiview correlation can transform input high-dim. data streams to low-dim. shared subspace across views
- The subspaces estimated by factoring out the variabilities arising from the many views of an event are naturally discriminative of the classes

We evaluated our methodology on several datasets in the domains of audio, video and images. Below are three demos of such applications:

**Click on the panels below to explore the learnt embeddings on different datasets**


<div class="container-img">
  <a href="https://sail.usc.edu/~somandep/maps/command_id.html">
  <img src="/assets/img/mvcorr_commands.svg" alt="Notebook" style="filter: blur(3px); width:50%;">
  <div class="content-img">
    <h1>Wake word classification</h1>
    <p>
From the speech commands dataset, our method learns to discriminate the 30 commands no matter who the speaker is in an semi-supervised manner.
</p>
  </div>
  </a>
</div>
<p></p>
<div class="container-img">
  <a href="https://sail.usc.edu/~somandep/maps/speaker_id.html">
  <img src="/assets/img/mvcorr_speakers.svg" alt="Notebook" style="filter: blur(3px); width:50%;">
  <div class="content-img">
    <h1>Text-dependent speaker ID</h1>
    <p>
From the speech commands dataset, our method learns to cluster the speakers no matter which of the 30 commands they spoke.
</p>
  </div>
  </a>
</div>
<p></p>
<div class="container-img">
  <a href="https://sail.usc.edu/~somandep/maps/dcase_2018_mvcorr.html">
  <img src="/assets/img/mvcorr_dcase.svg" alt="Notebook" style="filter: blur(3px); width:50%;">
  <div class="content-img">
    <h1>Domestic activity classification</h1>
    <p>
Learn to model multi-channel audio segments acquired by a microphone array in a house. The multiview shared subspace can robustly disentangle channel from class information to classify domestic activities such as cooking, cleaning.
</p>
  </div>
  </a>
</div>
<p></p>

<div class="container-img">
  <a href="https://sail.usc.edu/~somandep/maps/mvcnn.html">
  <img src="/assets/img/mvcorr_mvcnn.svg" alt="Notebook" style="filter: blur(3px); width:50%;">
  <div class="content-img">
    <h1>Multiview object recognition</h1>
    <p>
Embeddings learnt from multiple views of an object: Successfully classify 40 object categories imaged from 12 and 40 different views.
</p>
  </div>
  </a>
</div>

The visualizations above are developed using this [tool](https://github.com/krsna6/interactive-tsne)

> **Why does this work?**
The objective we maximize and the evolution of the eigenvalues in the objective through the training process is illustrated below:
![](/assets/img/projects/mvcorr_loss.svg)

