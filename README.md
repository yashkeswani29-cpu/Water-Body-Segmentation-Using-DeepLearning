# Water-Body-Segmentation-Using-DeepLearning
# Research Paper Summaries: Surface Water Detection

This repository contains internship research summaries of two papers on **water body / surface water segmentation** using deep learning, covering an ensemble approach for satellite imagery and a lightweight hybrid network for autonomous surface vehicles (USVs).

## Contents

1. [Dataset](#dataset)
2. [Models](#models)


## Dataset

This project uses the **Water Bodies Segmentation Dataset with Split** from Kaggle:
**https://www.kaggle.com/datasets/sovitrath/water-bodies-segmentation-dataset-with-split**

It contains satellite RGB images of water bodies paired with binary segmentation masks, pre-divided into train/validation/test splits, ready for use with segmentation models such as U-Net.

To use it without downloading manually, fetch it at runtime with `kagglehub` (requires a Kaggle API token):

```python
import kagglehub

path = kagglehub.dataset_download("sovitrath/water-bodies-segmentation-dataset-with-split")
print("Path to dataset files:", path)
```

## Models

Implementation notebooks (Google Colab) for each segmentation model tried on the dataset above:

| Model | Notebook |
|---|---|
| U-Net | [u-net.ipynb](https://colab.research.google.com/drive/1Ax08rcLT4BIgaxpaI83xqyNF75t9xDBK?usp=sharing) |
| W-Net | [Colab link](https://colab.research.google.com/drive/1wYSjOaM93PJS1iDlHYkJHozS1fxr_dT8?usp=sharing) |
| MSR-Net | [Colab link](https://colab.research.google.com/drive/1m3tMqNrEymW2xW38sCCJmmoiHLl_vwDv?usp=sharing) |
| DeepLabV3+ (hybrid) | [water_segmentation1.ipynb](https://colab.research.google.com/drive/1IXPLozaZ2yXasQIk3GSw2abst3ONJGEm?usp=sharing) |
| MLHI + DeepLab (50 epochs, preprocessed images) | [2.ipynb](https://colab.research.google.com/drive/1MCMbWPwgCwaoxQSRdq4r_EWiKD1iGrxt?usp=sharing) |
| U-Net (preprocessed images) | [Colab link](https://colab.research.google.com/drive/16FrGvuIRugzA1WPseIPUcbZdcluGdOnq?usp=sharing) |
| MSR-Net (preprocessed images) | *link not provided* |

### Results

| Model | Accuracy (Train) | IoU | Dice |
|---|---|---|---|
| U-Net | 82% | 0.707 | 0.82 |
| W-Net | 90.18% | 0.70 | 0.84 |
| MSR-Net | 91.14% | 0.76 | 0.86 |
| DeepLabV3+ | 97.27% | 0.9218 | 0.9593 |
