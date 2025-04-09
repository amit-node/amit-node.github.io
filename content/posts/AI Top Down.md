---
title: AI Top Down
date: 2025-04-09
tags:
  - AI_DL
---

### 6.1.1) One stage detectrons : fast and light weight
[An overview of object detection: one-stage methods.](https://www.jeremyjordan.me/object-detection-one-stage/)
A deep learning technique for object detection using CNN. 

In general, there's two different approaches for object detection – we can either make a fixed number of predictions on grid (one stage) or leverage a proposal network to find objects and then use a second network to fine-tune these proposals and output a final prediction (two stage).

Here object detection means recognize the presence of object in image and describe the location of each detected object by using rectangle bounding box (localization).
1. 
One stage or one shot, a model architecture which requires no intermediate task and directly predict object bounding box for an image in one stage fashion.

1. **Yolo v 10 n** `already done`
2. **Efficient Det - D0**
	- Light weight
	- easy to modify for grayscale
	- Based on EfficientNet

### 6.1.2) Two stage : more accurate but relatively slower
Important thing is region proposal.
Stage 1 : Region proposals generation, typically using selective search or the Region Proposal Network (RPN).
Stage 2 : Object classification and bounding box refinement on each proposed region.

3. **Faster RCNN with mobilenet backbone**
	- Lighter than ResNet based version
	- Can be adaptable to grayscale
4. **SSD with mobile net** `already done`

### 6.1.3) Transformer based models :
First introduced in the 2017 paper [‘Attention is All You Need’](https://arxiv.org/abs/1706.03762) and have since become the foundation for many state-of-the-art [NLP](https://inc42.com/tag/natural-language-processing/) tasks.
They are especially powerful for handling sequence of data. like sentences, time series and Images too.

Before Transformers, we used models like:
- RNNs (Recurrent Neural Networks)
- LSTMs (Long Short-Term Memory networks)
These worked by processing words one by one in order. That was slow and made it hard to remember information from far back in the sequence.

Transformers changed the game by using core idea **Attention Mechanism**:
- Processing all words (or tokens) at once
- Using a mechanism called self-attention to understand the relationships between words.

5. **DETR - light variant**
	- Heavier than yolo, but lighter variants also there