<div align=center>
  
# ControlCap: Controllable Region-level Captioning
</div>

This is the official implementaion of paper [***ControlCap: Controllable Region-level Captioning***](https://arxiv.org/pdf/2401.17910.pdf), which is accepted in ***ECCV 2024***. This repository contains Pytorch training code, evaluation code, pre-trained models, and visualization method. Based on ControlCap, we build [***DynRefer***](https://github.com/callsys/DynRefer), which support more tasks and achieves better performance.

<div align=center>

[![arXiv preprint](http://img.shields.io/badge/arXiv-2307.09756-b31b1b)](https://arxiv.org/pdf/2401.17910.pdf)
![Python 3.8](https://img.shields.io/badge/Python-3.8-green.svg?style=plastic)
![PyTorch 1.11](https://img.shields.io/badge/PyTorch-1.11-EE4C2C.svg?style=plastic)
[![LICENSE](https://img.shields.io/github/license/vasgaowei/ts-cam.svg)](LICENSE)
</div>


<div align=center>
<img src="assets/framework.png" width="50%">
</div>


## 1. Contents
- ControlCap: Controllable Region-level Captioning
  - [1. Contents](#1-contents)
  - [2. Introduction](#2-introduction)
  - [3. Results](#3-results)
  - [4. Code Usage](#4-code-usage)
  - [5. Contacts](#5-contacts)
  - [6. Acknowledgment](#6-acknowledgment)
  - [7. Citation](#7-citation)

## 2. Introduction

Region-level captioning is challenged by the caption degeneration issue, which refers to that pre-trained multimodal models tend to predict the most frequent captions but miss the less frequent ones. In this study, we propose a controllable region-level captioning (ControlCap) approach, which introduces control words to a multimodal model to address the caption degeneration issue. In specific, ControlCap leverages a discriminative module to generate control words within the caption space to partition it to multiple sub-spaces. The multimodal model is constrained to generate captions within a few sub-spaces containing the control words, which increases the opportunity of hitting less frequent captions, alleviating the caption degeneration issue. Furthermore, interactive control words can be given by either a human or an expert model, which enables captioning beyond the training caption space, enhancing the model’s generalization ability. Extensive experiments on Visual Genome and RefCOCOg datasets show that ControlCap respectively improves the CIDEr score by 21.6 and 2.2, outperforming the state-of-the-arts by significant margins.

## 3. Results


<div align=center>
Region-level captioning performance on Visual Genome (VG) and RefCOCOg.
<img src="assets/result.png" width="50%">
</div>

<div align=center>
Gradio demo of ControlCap.
<img src="assets/controlcap_demo.gif" width="98%">
</div>

## 4. Code Usage

- [**Environment**](./docs/install.md)

- [**Dataset and Checkpoints**](./docs/data.md)

- [**Training and Evaluation**](./docs/train_and_eval.md)

- [**Demo**](./docs/demo.md)


## 5. Contacts
If you have any question about our work or this repository, please don't hesitate to contact us by emails or open an issue under this project.
- [zhaoyuzhong20@mails.ucas.ac.cn](zhaoyuzhong20@mails.ucas.ac.cn)
- [wanfang@ucas.ac.cn](wanfang@ucas.ac.cn)

## 6. Acknowledgment

- Part of the code is borrowed from [LAVIS](https://github.com/salesforce/LAVIS), [GlaMM](https://github.com/mbzuai-oryx/groundingLMM), [Osprey](https://github.com/CircleRadon/Osprey/tree/main) and [RAM](https://github.com/xinyu1205/recognize-anything), we sincerely thank them for their contributions to the community.

## 7. Citation

```text
@inproceedings{zhao2025controlcap,
  title={ControlCap: Controllable Region-Level Captioning},
  author={Zhao, Yuzhong and Liu, Yue and Guo, Zonghao and Wu, Weijia and Gong, Chen and Ye, Qixiang and Wan, Fang},
  booktitle={European Conference on Computer Vision},
  pages={21--38},
  year={2025},
  organization={Springer}
}
```
