# BrainLeaks: On the Privacy-Preserving Properties of Neuromorphic Architectures against Model Inversion Attacks

This repository contains the code for the paper ["BrainLeaks: On the Privacy-Preserving Properties of Neuromorphic Architectures against Model Inversion Attacks"](https://arxiv.org/abs/2402.00906) by Hamed Poursiami, Ihsen Alouani, and Maryam Parsa.

## Introduction

In this work, we investigate the privacy-preserving properties of spiking neural networks (SNNs) and their vulnerability to model inversion attacks. We propose two novel model inversion attack techniques tailored for the spiking domain: BrainLeaks-v1 and BrainLeaks-v2.

## Datasets

The experiments are conducted on the following datasets:
- AT&T Face Database
- MNIST
- N-MNIST
- IBM DvsGesture Dataset

## Files

The repository includes the following files:
- **.ipynb**: Jupyter Notebooks of the experiments 
  - Format: [Dataset Name] + [SNN / ANN] + [Attack and/or Evaluation]
  - "Attack" corresponds to target model training and model inversion attack 
  - "Evaluation" corresponds to evaluation classifier training and the attack evaluation
- **Weights**: State Dictionary of trained models (Target or Evaluation Classifiers)
  - Format: [Dataset Name] + [SNN / ANN] + [Weights] + [Target / Eval]
- **Inverted**: Pytorch tensors containing the reconstructed samples
  - Format: [Dataset Name] + [ANN/SNN] + [Inverted] + [ - / BL1 / BL2 ]
- **Data-Related files**: 
  1. Face_ATnT_Data.zip: Contains the AT&T Face Database training and test samples
  2. ibm_gestures_train / ibm_gestures_test: Pytorch dataset object helpful for preprocessing stage of IBM data

## Requirements

The code is written in Python and requires the following libraries:
- PyTorch
- SNNTorch
- Tonic


You can install the required libraries using pip:

```bash
pip install pytorch snntorch tonic 
```


## Usage
1.	Clone or download the repository.
2.	Install the required libraries.
3.	Run the .ipynb notebooks to reproduce the experiments and results.

## Citation
If you use this code in your research, please cite our paper:

```
@article{poursiami2024brainleaks,
  title={BrainLeaks: On the Privacy-Preserving Properties of Neuromorphic Architectures against Model Inversion Attacks},
  author={Poursiami, Hamed and Alouani, Ihsen and Parsa, Maryam},
  journal={arXiv preprint arXiv:2402.00906},
  year={2024}
}
```


#### Note
The repository contains essential files for running experiments, including Jupyter notebooks and the raw AT&T Face dataset. Some non-essential files, like pre-trained model weights, might be omitted due to size constraints. However, all necessary files for training models, executing attacks, and evaluating results are included, ensuring full reproducibility.


