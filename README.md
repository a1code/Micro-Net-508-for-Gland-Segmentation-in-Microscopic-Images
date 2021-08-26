# Micro-Net-508-for-Gland-Segmentation-in-Microscopic-Images

**Note**: Please refer [ProjectDescription.pdf]() and [ProjectSlides.pdf]() for details.   
Colab Notebook with the full code is [here]().   

**Dataset** : Out of the three data sets used in the paper, only one of them is accessible publicly. Both the Multiplexed Fluorescence Imaging Data and the Computational Precision Medicine (CPM) data set for nuclear segmentation were unavailable. So we used the public Warwick-QU dataset from the Gland Segmentation (GLaS) Challenge for training and evaluating our implementation of Micro- Net-508. The dataset consists of 85 training images along with their respective ground truth images that were annotated by pathologists. The dataset used for our implementation can be accessed [here]().  

**Implementation Summary**:  
• Implemented MicroNet-508 architecture for T2I using PyTorch and trained the model on   
• Implemented modules for 
• Setup the d  

**Abstract**:  
For automated microscopic image analysis, segmentation and localization of key structures like tumours, glands, and cells is a crucial step to improve the accuracy of downstream tasks. Deep CNN architectures have been found to be really effective for this task, while also allowing re-usability to segment various structures across different modalities through retraining and hyper-parameter tuning. In this work, we present the details of our implementation of the Micro-Net-508 architecture, which was proposed as the state-of-the-art for gland segmentation from microscopic images. With no implementation available currently and lack of large annotated training data, we found this an interesting problem to contribute towards. Our goal is to compare our implementation of Micro-Net-508 to the model proposed in the paper, and try to reproduce the observed results.

**Observations**:
The available RAM on Google Colaboratory Pro GPU with High-RAM configuration is 27.4 GB. Our model fails to train on this infrastructure with the given memory availability. We get CUDA out of memory exception either when moving the model instance created on CPU to the GPU, or during the very first epoch of training.
The paper describes the setup used for training as a Windows 10 machine with Intel E5-2670 v2 CPU, TitanX Maxwell GPU and 96 GB RAM. With this configuration, that authors’ model takes around 4.5 days to train over 25 epochs.
