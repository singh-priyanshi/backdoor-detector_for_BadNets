# Backdoor Attack Defense - User Guide

Welcome to the Backdoor Attack Defense repository! This guide will help you understand the purpose of the code, set up the environment, and run the defense mechanism against backdoor attacks using a pruning strategy.

## Table of Contents

1. [Overview](#overview)
2. [Getting Started](#getting-started)
    - [Requirements](#requirements)
    - [Dataset](#dataset)
    - [Model](#model)
3. [Defense Mechanism](#defense-mechanism)
    - [Running the Code](#running-the-code)
    - [Results](#results)
4. [GoodNet Model](#goodnet-model)
    - [Evaluation](#evaluation)
5. [Customization and Contributions](#customization-and-contributions)
6. [Conclusion](#conclusion)

## Overview

This repository contains code to defend machine learning models against backdoor attacks. The defense strategy involves pruning specific activation channels in vulnerable layers to fortify the model against potential manipulations by backdoor patterns. Additionally, a GoodNet model is introduced to detect anomalies by combining the predictions of the original Backdoor Model and the Repaired Backdoor Model.

## Getting Started

### Requirements

Make sure you have the following dependencies installed:

- TensorFlow (`pip install tensorflow`)
- Keras (`pip install keras`)
- h5py (`pip install h5py`)
- NumPy (`pip install numpy`)
- Matplotlib (`pip install matplotlib`)
- scikit-learn (`pip install scikit-learn`)
- Pandas (`pip install pandas`)
- tqdm (`pip install tqdm`)

### Dataset

The code assumes the availability of clean and backdoored datasets in HDF5 format. Update the file paths in the code to point to your specific dataset locations.
![image](https://github.com/singh-priyanshi/backdoor-detector_for_BadNets/assets/31034647/c6df546e-1023-4598-9972-7778f5d21f35)

![image](https://github.com/singh-priyanshi/backdoor-detector_for_BadNets/assets/31034647/a1fe2df2-75ba-4d4a-b814-f7eb1b0f1e19)

### Model

A pre-trained model (`bd_net.h5`) is used for demonstration purposes. Make sure you have the model file in the specified path or replace it with your own model.

![image](https://github.com/singh-priyanshi/backdoor-detector_for_BadNets/assets/31034647/d644ef7a-839b-4af9-bd2b-94b739ae26ac)

## Defense Mechanism

### Running the Code

Execute the code in a Python environment. Adjust file paths, dataset locations, and model filenames as needed. The code guides you through the backdoor defense, evaluating the model's performance before and after pruning.

### Results

Explore the results of the defense strategy on the validation dataset. Visualize clean and poisoned data, and understand the trade-offs between clean accuracy and attack success rate under different pruning thresholds.

##### Performance of model on Validation Dataset
![image](https://github.com/singh-priyanshi/backdoor-detector_for_BadNets/assets/31034647/fc2864f3-d8d7-4c7c-a0b4-88043fcbfa95)

##### Performance of model on Test Dataset
![image](https://github.com/singh-priyanshi/backdoor-detector_for_BadNets/assets/31034647/17357b3a-13e7-4355-8005-364ab3da1861)
![image](https://github.com/singh-priyanshi/backdoor-detector_for_BadNets/assets/31034647/eee668ce-592b-451e-83b7-61eae53612c6)

## GoodNet Model

### Evaluation

Learn about the GoodNet model, which combines the original Backdoor Model and the Repaired Backdoor Model. Evaluate the GoodNet model's performance on the test dataset and understand its ability to detect anomalies in case of backdoor attacks.

### Results: Goodnet Accuracy v/s Attack success rate on Test dataset
![image](https://github.com/singh-priyanshi/backdoor-detector_for_BadNets/assets/31034647/e645c3f6-427a-464d-acae-39dbffe95902)

![image](https://github.com/singh-priyanshi/backdoor-detector_for_BadNets/assets/31034647/313d9263-402d-491a-9c0e-6537e7027fbd)


## Customization and Contributions

Feel free to customize the code, experiment with different models, datasets, or defense strategies. Contributions to enhancing the security of machine learning models against backdoor attacks are welcome!

## Conclusion

Thank you for using the Backdoor Attack Defense code. We hope this tool helps you strengthen your machine learning models against potential backdoor threats. If you have any questions or feedback, please reach out to us.

