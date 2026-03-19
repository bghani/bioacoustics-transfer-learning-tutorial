# Bioacoustics transfer learning tutorial

A hands-on tutorial notebook for exploring transfer learning, embedding extraction, and few-shot classification with bioacoustic data.

This repository was created for a spring school workshop and is designed to be practical, readable, and easy to adapt to your own dataset.

## What this tutorial covers

The notebook walks through a simple but powerful workflow:

- extracting embeddings from audio with pretrained models
- visualizing embeddings in 2D
- training a linear probe on top of embeddings
- running a few-shot learning experiment
- plotting performance as the number of training recordings increases

The broader idea is to show how pretrained audio models can be reused for ecological and biodiversity tasks, especially when labeled data is limited.

## Repository contents

- `transfer_learning_tutorial.ipynb`  
  The main workshop notebook with explanations and code

## Who this is for

This tutorial is aimed at:

- students and researchers working with bioacoustics
- people curious about transfer learning in ecology
- anyone who wants a lightweight and practical entry point into embedding-based classification

## Requirements

The notebook was developed in Google Colab, but it can also be adapted to run locally.

Typical dependencies include:

- Python 3.11+
- numpy
- matplotlib
- scikit-learn
- torch
- jupyter
- bacpipe


## Using your own dataset

The notebook currently assumes that embeddings or audio files live in a folder structure like this:

```text
dataset_root/
├── class_A/
└── class_B
```
## Reference paper

This workshop is based on the following paper:

- [Global birdsong embeddings enable superior transfer learning for bioacoustic classification](https://www.nature.com/articles/s41598-023-49989-z)  
  *Scientific Reports, 2023*

The core idea explored in both the paper and this notebook is:

> Instead of training models from scratch, we can use embeddings from pretrained bioacoustic models and adapt them to new tasks with very little data.

The study shows that embeddings learned from large-scale bird vocalization datasets:
- generalize well across species and even taxa (birds, bats, frogs, marine mammals, etc.)
- outperform embeddings from general-purpose audio models
- enable effective few-shot learning with very limited labeled data :contentReference[oaicite:3]{index=3}

In this notebook, we recreate a simplified version of this pipeline in a hands-on way. 
    