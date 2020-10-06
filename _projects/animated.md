---
layout: project
title: 'Unsupervised discovery of characters in animated movies'
caption: Extracting model sheets for animated content, Automatically.
description: >
  Our proposed system can automatically extract character exemplars from an animated movie..
date: '08-01-2018'
image: 
  path: assets/img/projects/animated_2.svg
links:
  - title: code
    url: https://github.com/usc-sail/mica-animation
  - title: dataset
    url: https://docs.google.com/forms/d/e/1FAIpQLSdrqlSnjxoWJiCJ7NfwIkFPasFWI9My58Gns1ayc8R7VagL6A/viewform
  - title: poper
    url: https://sail.usc.edu/~mica/pubs/somandepalli2018unsupervised.pdf
accent_color: '#4fb1ba'
accent_image:
  background: '#193747'
theme_color: '#193747'
featured: true
sitemap: false
---

<details><summary><b>
What are character dictionaries for movies?
</b></summary>
Automatic movie or multimedia content analysis requires audio-video diarization (i.e., <b>"who"</b> appeared? and <b>"when"</b>). For video diarization in particular, where the characters that appear on screen are not known, a key step is to provide a list of characters that form the <b>who appeared</b> component of the system.
We refer to such a list of characters specific to each movie <b>character dictionary</b>.
</details>
<p></p>

<details><summary><b>
Why is it hard to get character dictionaries for animation movies?
</b></summary>
Human face detection is the crux of character labeling methods for live action TV. Since human-characters can be uniquely identified by their faces, this method performs adequately well. 
But, such methods developed for human faces do not work for the digital animation genre. Animated characters, though mostly anthropomorphic (having human characteristics) are not always human-like in appearance. They can be fictional animals, inanimate objects or abstract in design.
</details>
<p></p>

> **Our proposed system for animation movie character dictionaries:**
We propose an unsupervised approach which requires no prior information about the characters in a movie.
- First, we use a deep neural network based object detector that is trained on natural photographs to identify a set of initial character candidates.
- Second, these candidates are further pruned using saliency constraints and object tracking.
- A character dictionary per movie is then generated from exemplars obtained by clustering these candidates.
![animated](https://drive.google.com/uc?id=0B3ydbkt5jAUyLUUtc2hUWm5GdzQ)

Schematic diagram of the proposed system for discovery of characters in animation movies
{:.figcaption }

We were able to identify both anthropomorphic and non-anthropomorphic characters in a dataset of forty-six animation movies with varying composition and character design.  
See a few results below:  
> (Click on the images to enlarge them)
 
Cars 2 (2011)             |  Free Birds (2014)
:-------------------------:|:-------------------------:
[![cars 2](https://drive.google.com/uc?id=0B3ydbkt5jAUycVZTc3FMbzg2RFU "Cars 2 (2011)")](https://drive.google.com/uc?id=0B3ydbkt5jAUyaklpLTRFYmh4M0U)  |  [![free birds](https://drive.google.com/uc?id=0B3ydbkt5jAUyNWNMNXJ3WjFGeVk "Free Birds (2014)")](https://drive.google.com/uc?id=0B3ydbkt5jAUyNHBMc2tHV2RsOVk)


Frozen (2013)             |
:-------------------------:|
[![alt text](https://drive.google.com/uc?id=0B3ydbkt5jAUydEo0Vzk3MVUwZjg "Frozen (2013)")](https://drive.google.com/uc?id=0B3ydbkt5jAUyWU5wSXFYTjB4Z1k) |

**Evaluation of the proposed system on forty-six movies** |
:--------------------------------------------------------:| 
![performance](https://drive.google.com/uc?id=0B3ydbkt5jAUyQ1pJYjFseEhrT0k "Performance Evaluation") |


### SAIL Animation Movie Character Database (SAIL AMCD)

**Results from our system and movie casts used for evaluation**  
Instructions to download the data:  
First, fill out this [Google form](https://docs.google.com/forms/d/e/1FAIpQLSdrqlSnjxoWJiCJ7NfwIkFPasFWI9My58Gns1ayc8R7VagL6A/viewform) with the required information to receive the password.  
Then, use the password to download the data at this [link](https://128.125.20.152:5001/sharing/khXraiWim) for the outputs and annotations used in the system evaluation of the paper  

The database consists of the following directories *(Please see README for more details)*:  
![alt text](https://drive.google.com/uc?id=0B3ydbkt5jAUyTnZ2R3p0a0dLd0k "SAIL-AMCD download")  



