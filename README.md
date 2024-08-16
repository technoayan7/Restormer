---

# Restormer: Efficient Transformer for High-Resolution Image Restoration

[![paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2111.09881)
[![supplement](https://img.shields.io/badge/Supplementary-Material-red)](https://drive.google.com/file/d/1oKGON8vG4uDWMmZKqHeTMnFowhOubifK/view?usp=sharing)
[![video](https://img.shields.io/badge/Video-Presentation-F9D371)](https://www.youtube.com/watch?v=3mqu6N4_0pY&t)
[![slides](https://img.shields.io/badge/Presentation-Slides-B762C1)](https://drive.google.com/file/d/19wKhnQtr3mcD6IsLj0ZFSwCgIRKUkDQJ/view?usp=sharing)
[![Summary](https://img.shields.io/badge/Summary-Slide-87CEEB)](https://drive.google.com/file/d/1wyKAMLzJpDqHiF6AMsmnmGQC241GyT8q/view?usp=sharing)


#### News
-  Added Colab Demo. [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lOzh9Rpz4cdLput6Y00sU4tNuZJTtjBY#scrollTo=SRd46QaXlklQ)
-  Restormer is selected for an ORAL presentation at CVPR 2022 :dizzy:
-  Training codes are released :fire:
- Testing codes and pre-trained models are released!
<hr />

> **Abstract:** *Since convolutional neural networks (CNNs) perform well at learning generalizable image priors from large-scale data, these models have been extensively applied to image restoration and related tasks. Recently, another class of neural architectures, Transformers, have shown significant performance gains on natural language and high-level vision tasks. While the Transformer model mitigates the shortcomings of CNNs (i.e., limited receptive field and inadaptability to input content), its computational complexity grows quadratically with the spatial resolution, therefore making it infeasible to apply to most image restoration tasks involving high-resolution images. In this work, we propose an efficient Transformer model by making several key designs in the building blocks (multi-head attention and feed-forward network) such that it can capture long-range pixel interactions, while still remaining applicable to large images. Our model, named Restoration Transformer (Restormer), achieves state-of-the-art results on several image restoration tasks, including image deraining, single-image motion deblurring, defocus deblurring (single-image and dual-pixel data), and image denoising (Gaussian grayscale/color denoising, and real image denoising).* 
<hr />

## Network Architecture

<img src = "https://i.imgur.com/ulLoEig.png"> 

## Demo

To test the pre-trained Restormer models of [Deraining](https://drive.google.com/drive/folders/1ZEDDEVW0UgkpWi-N4Lj_JUoVChGXCu_u) on your own images, you can either use Google Colab [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lOzh9Rpz4cdLput6Y00sU4tNuZJTtjBY#scrollTo=SRd46QaXlklQ), or command line as following
```
python demo.py --task Task_Name --input_dir path_to_images --result_dir save_images_here
```
Example usage to perform Deraining on a directory of images:
```
python demo.py --task Deraining --input_dir './demo/degraded/' --result_dir './demo/restored/'
```
Example usage to perform Deraining on an image directly:
```
python demo.py --task Deraining --input_dir './demo/degraded/portrait.jpg' --result_dir './demo/restored/'
```


## Results
<details>
<summary><strong>Image Deraining</strong> (click to expand) </summary>
  
### Results on Rain100L Dataset
<img src = "https://i.imgur.com/yRTvF21.png"> 

### Results on Rain100H Dataset
<img src = "https://i.imgur.com/j2SJN7x.png"> 

### Comaparisons with Different Models
<img src = "https://i.imgur.com/mMoqYJi.png"> 
</details>

## Training and Evaluation

Training and Testing instructions for Deraining are provided in their respective directories. Here is a summary table containing hyperlinks for easy navigation:

<table>
  <tr>
    <th align="left">Task</th>
    <th align="center">Training Instructions</th>
    <th align="center">Testing Instructions</th>
    <th align="center">Restormer's Visual Results</th>
  </tr>
  <tr>
    <td align="left">Deraining</td>
    <td align="center"><a href="Deraining/README.md#training">Link</a></td>
    <td align="center"><a href="Deraining/README.md#evaluation">Link</a></td>
    <td align="center"><a href="https://drive.google.com/drive/folders/1O1FJ-eAOgfuzB2rQvx9J4OJ2dsulnDur?usp=sharing">Download</a></td>
  </tr>
</table>

**Acknowledgment:** This code is based on the [BasicSR](https://github.com/xinntao/BasicSR) toolbox and [HINet](https://github.com/megvii-model/HINet). 

