# Galactic Halo Segmentation with Bayesian Convolutional Networks

Welcome to the **Epoch of Reionization repository**. This project leverages advanced Bayesian Convolutional Neural Networks (BCNNs) to identify and segment high-probability mass regions within large-scale galactic halo datasets. Developed to process astronomical simulation data with rigorous uncertainty quantification, this repository provides a scalable and robust framework for researchers studying cosmic structures.

## Project Overview

Understanding the large-scale structure of the universe often requires precise segmentation of galactic halos from raw simulation data. This repository implements a Bayesian convolutional architecture that not only performs segmentation but also integrates uncertainty quantification—a crucial feature when dealing with the inherent noise and sparsity of cosmological data.

![Network Architecture](https://raw.githubusercontent.com/NiloofarESF1996/epoch-of-reionization/refs/heads/main/Images/img_1.png)

The diagram above illustrates the BCNN architecture used in this project. The network progressively downsamples and encodes the spatial information of the input map, passing through Bayesian sampling layers to capture probabilistic distributions of mass regions. Each layer of the network is carefully designed for optimal information retention and dimensional reduction, ultimately producing segmentation maps with pixel-wise uncertainty estimates.

## Data Preparation Workflow

The dataset preparation pipeline involves:

1. **Density Contrast Calculation**: Computes density contrast maps from raw ionisation data.
2. **Halo Data Binning**: Halo data are binned into a 2D grid to generate corresponding 2D halo maps.
3. **Labelling**: The maps are labelled to indicate high and low mass probability regions for training and validation.

The following flowchart provides an overview of this preprocessing sequence:

![Data Workflow](https://github.com/your-repo-path/image2.png)

This workflow efficiently processes high-dimensional data to generate both density and halo maps, crucial for training the BCNN to distinguish between regions of high and low mass concentrations.

## Input and Label Structure

The input data consists of 2D halo and density contrast maps, while labels correspond to binary segmentation maps highlighting regions with high and low mass probability. Below is a sample input alongside ground truth and model-predicted outputs:

![Input and Label](https://github.com/your-repo-path/image3.png)

These input-label pairs provide a comprehensive training set that enables the network to generalise well on unseen regions of the simulation data, supporting accurate predictions in high-dimensional galactic datasets.

## Bayesian Sampling Layer

To address uncertainties in predictions, our BCNN integrates **Bayesian Sampling Layers**. These layers provide an interpretable framework to estimate the probability of high-mass regions, enhancing the reliability of segmentation outcomes. Below is an illustrative breakdown of the Bayesian Sampling mechanism within the network:

![Bayesian Sampling Layer](https://github.com/your-repo-path/image4.png)

By incorporating these layers, the model captures a spectrum of possible outcomes, giving users confidence intervals for the segmented mass regions—ideal for scientific applications where precision and confidence are paramount.

## Results and Predictions

The network's predictive performance demonstrates promising results, achieving effective segmentation with minimal false positives. The following figure presents the **Ground Truth** versus **Predictions**, showcasing the model's accuracy and robustness across a random slice from the dataset:

![Results Comparison](https://github.com/your-repo-path/image5.png)

The output predictions closely match the ground truth labels, verifying the efficacy of the Bayesian layers in mitigating uncertainties in cosmological datasets.

## Installation and Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-repo-path/galactic-halo-segmentation.git
