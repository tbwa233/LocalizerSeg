# LocalizerSeg

This repository contains the implementation of LocalizerSeg. Our proposed model uses text prompts to tell a SAM-based model which anatomical structures to find and segment in 2D CT localizer images, allowing flexible segmentation of one or more organs.

## Abstract
Computed tomography (CT) localizer images are routinely acquired prior to volumetric CT reconstruction for patient positioning, scan range determination, and radiation dose optimization. Yet, they remain largely underutilized for automated anatomical understanding. Existing localizer segmentation methods rely on fixed-output supervised models that lack the flexibility necessary for deployment in real-world clinical workflows. Addressing this, we propose LocalizerSeg, a promptable multi-organ segmentation framework that combines semantic anatomical conditioning with an architecture inspired by the Segment Anything Model (SAM). Experiments on 35 anatomical structures demonstrate that LocalizerSeg achieves a mean Dice similarity coefficient of 0.8269, outperforming both existing promptable universal segmentation models as well as conventional fully-supervised approaches, while also providing much more flexibility than the latter models. These results demonstrate the feasibility of language-guided anatomical localization from CT localizer images and highlight the potential of promptable segmentation for organ-aware CT scan planning and other clinical imaging applications.

## Model
<p align="center">
  <img src="https://github.com/tbwa233/LocalizerSeg/blob/main/images/LocalizerSeg-Model.jpg" alt="Figure">
</p>

## Results
A brief summary of our results are shown below. Our LocalizerSeg is compared to various fully-supervised and promptable baselines. In the table, the p < α column indicates baseline methods that were outperformed by LocalizerSeg in a statistically significant manner. For the ResU-Net baselines, † indicates that the model was randomly initialized, and ‡ indicates that the model was pretrained with ImageNet-1K weights. For LocalizerSeg, * indicates that MedSAM was used as the segmentation backbone, while ** indicates SAM as the backbone.
<p align="center">
  | Method | DSC | $p < \alpha$ |
  |---|---:|:---|
  | U-Net | 0.8125 | No ($p > 0.05$) |
  | ResU-Net ($\dagger$) | 0.7839 | Yes ($p < 0.01$) |
  | ResU-Net ($\ddagger$) | 0.8003 | No ($p > 0.05$) |
  | U-Net++ | 0.7766 | Yes ($p < 0.01$) |
  | nnU-Net | 0.8092 | No ($p > 0.05$) |
  | Swin-Unet | 0.7382 | Yes ($p < 0.01$) |
  | UNETR | 0.7532 | Yes ($p < 0.01$) |
  | Swin-UNETR | 0.8041 | Yes ($p < 0.01$) |
  | CLIP-Driven Universal Model | 0.7583 | Yes ($p < 0.01$) |
  | UniSeg | 0.7938 | No ($p > 0.05$) |
  | DUM | 0.5981 | Yes ($p < 0.01$) |
  | U-KAN-Seg | 0.7498 | Yes ($p < 0.01$) |
  | LocalizerSeg (*) | 0.8265 | No ($p > 0.05$) |
  | LocalizerSeg (**) | 0.8269 | **---** |
</p>

## Code
