---
layout: archive-dates
permalink: /mldl/
title: Machine Learning(ML), Deep Learning(DL) Projects
---

In the following links, you can check out some interesting Machine learning and Deep Learning models I've worked with!

-------------

### Master of Science Thesis 

This study explains the design and implementation of a garbage detector as both
a web app (UI) and system software for installation on edge devices like cameras. 
The system is constructed using the YOLOv5, a pre-trained, state-of-the-art,
single-stage neural network used for real-time object detection. 
Data gathering, data processing, model training, and model testing phases of the
garbage detection software were facilitated by an MLOps pipeline developed previously
in a company setting where Emilie Naples participated as an intern during the development of the thesis. 
The MLOps pipeline is a Jupyter notebook connected to MLflow for model version registration and a Google Cloud database where training images are stored. When is integrated with cameras, it will capture image
metadata from video streams and transmit this data back to a centralized database for
efficient and better-optimized trash pick-up.

- [Real Time Garbage Detection with YOLOv5 for City Streets](/Notebooks/masterthesis.pdf)


### YOLOv5 CNN Network Architecture & Implementation

The architecture of the YOLOv5 pre-trained neural network can be seen below:

<img src="/images/yoloarchitecture.png?raw=true"/>

The YOLO neural network has a sequence of convolutional layers to extract features with max pooling for dimensionality reduction and batch normalization to speed up learning. Leaky ReLU activation functions introduce non-linearity, while fully connected layers near the end interpret the features to predict bounding boxes and class probabilities for object detection.

YOLOv5 builds on the YOLO architecture and is a more modular network, allowing for easier customization and scalability. It incorporates Cross-Stage Partial networks (CSPNet) for better gradient flow and feature reuse, uses a mosaic data augmentation technique for training, and has an adaptive anchor box calculation. It is a great choice for real-time object detection because of its single-staged nature in that with only one pass through the network, it is able to both detect and classify the object(s) of interest.

### Variational Autoencoders

To concisely present the "Variational Autoencoders" project in your portfolio, consider the following streamlined summary:

### Project Title: Understanding Variational Autoencoders

This project explores Variational Autoencoders (VAEs) through the lens of the CelebA dataset, focusing on image generation. Using a subset of 11,000 celebrity images, it demonstrates how VAEs can learn and generate new facial images. The emphasis here is on deep learning techniques for image generation and the potential of VAEs in synthetic data creation and beyond.

- **Concepts:** VAEs, probabilistic models, inference, and training loss (ELBO).
- **Uses:** PyTorch and torchvision for model building and training for the celebrity face generation.
- **Outcome:** Successfully trained a VAE model, illustrating its effectiveness in generating realistic and varied images.

- [Variational Autoencoders](/Notebooks/Variational_Autoencoders.html)

### Image Classification with MLPs

In this short project, I implement an image classifier using MLPs and the MNIST dataset, which consists of greyscale handwritten digits. Each image is 28x28 pixels. The goal is to build a neural network that can take one of these images and predict the digit in the image.

- [Image Classification with MLPs](/Notebooks/Image_Classification_with_MLPs_Part_1.html)

<img src="/images/s.png?raw=true"/>

### Regularizing MLPs

In this second part of the previous MLPs side project, I use the [Fashion-MNIST dataset](https://github.com/zalandoresearch/fashion-mnist), to experiment with early stopping, dropout, and L2 weight regularization:

- [Regularizing MLPs](/Notebooks/Regularizing_MLPs.html)


### Experimenting with Spectral Clustering

This notebook and mini project experiments with spectral clustering and the results on different data. 

- [Spectral Clustering](/Notebooks/Spectrual_Clustering_Experiments.html)