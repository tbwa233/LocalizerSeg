# LocalizerSeg

This repository contains the implementation of LocalizerSeg. Our proposed model uses text prompts to tell a SAM-based model which anatomical structures to find and segment in 2D CT localizer images, allowing flexible segmentation of one or more organs.

## Abstract
Computed tomography (CT) localizer images are routinely acquired prior to volumetric CT reconstruction for patient positioning, scan range determination, and radiation dose optimization. Yet, they remain largely underutilized for automated anatomical understanding. Existing localizer segmentation methods rely on fixed-output supervised models that lack the flexibility necessary for deployment in real-world clinical workflows. Addressing this, we propose LocalizerSeg, a promptable multi-organ segmentation framework that combines semantic anatomical conditioning with an architecture inspired by the Segment Anything Model (SAM). Experiments on 35 anatomical structures demonstrate that LocalizerSeg achieves a mean Dice similarity coefficient of 0.8269, outperforming both existing promptable universal segmentation models as well as conventional fully-supervised approaches, while also providing much more flexibility than the latter models. These results demonstrate the feasibility of language-guided anatomical localization from CT localizer images and highlight the potential of promptable segmentation for organ-aware CT scan planning and other clinical imaging applications.

## Model
![Figure](https://github.com/tbwa233/LocalizerSeg/blob/main/images/LocalizerSeg-Model.jpg)

## Results

## Code
