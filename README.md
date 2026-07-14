# DIP-PROJECT-CSE-4106

**Comparative Performance Analysis of Classical Image Segmentation Techniques and U-Net on the ISIC 2018 Skin Lesion Segmentation Dataset**

This project is a Digital Image Processing (CSE 4106) course project that evaluates and compares classical image segmentation methods against a deep learning-based U-Net model for the task of dermoscopic skin lesion segmentation, using the ISIC 2018 dataset.

## Overview

Accurate segmentation of skin lesions from dermoscopic images is a key step in automated melanoma diagnosis systems. This project implements and benchmarks two broad categories of segmentation approaches:

- **Classical (non-learning-based) segmentation techniques** — e.g. thresholding, edge detection, and morphological operations — applied directly on preprocessed dermoscopic images.
- **U-Net (deep learning-based) segmentation** — a convolutional neural network trained end-to-end to predict lesion masks.

The performance of both approaches is compared using standard segmentation evaluation metrics to highlight the trade-offs between traditional image processing pipelines and modern deep learning methods.

## Dataset

- **ISIC 2018 Skin Lesion Segmentation Dataset** (Task 1), consisting of dermoscopic images and their corresponding ground-truth binary lesion masks.
- Dataset source: [ISIC Archive](https://www.isic-archive.com/) / [ISIC 2018 Challenge](https://challenge.isic-archive.com/data/)

## Repository Contents

| File | Description |
|---|---|
| `dip_project_final.ipynb` | Main Jupyter notebook containing the full pipeline: data loading, preprocessing, classical segmentation methods, U-Net model implementation, training, evaluation, and results comparison. |

## Methods

**Classical Segmentation Pipeline**
- Image preprocessing (noise removal, hair artifact removal, contrast enhancement)
- Thresholding-based segmentation (e.g. Otsu's method)
- Edge-detection-based segmentation
- Morphological post-processing to refine masks

**Deep Learning Pipeline**
- U-Net architecture for semantic segmentation
- Training on the ISIC 2018 training set with corresponding ground-truth masks
- Validation and evaluation on held-out test images

## Evaluation Metrics

The segmentation outputs from both approaches are compared using standard metrics such as:
- Dice Similarity Coefficient (DSC)
- Jaccard Index (IoU)
- Pixel Accuracy
- Sensitivity / Specificity

## Requirements

This project runs as a Jupyter/Colab notebook. Typical dependencies include:

```
numpy
opencv-python
matplotlib
scikit-image
tensorflow / keras (or pytorch, depending on implementation)
```

Install with:

```bash
pip install numpy opencv-python matplotlib scikit-image tensorflow
```

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/Abir-bleh/DIP-PROJECT-CSE-4106.git
   ```
2. Open `dip_project_final.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
3. Download the ISIC 2018 dataset and update the dataset paths in the notebook.
4. Run the notebook cells sequentially to reproduce preprocessing, segmentation, training, and evaluation results.

## Course Information

- **Course:** CSE 4106 — Digital Image Processing Sessional
- **Institution:** Rajshahi University of Engineering and Technology (RUET)

## License

No license has been specified for this repository. All rights reserved by the author unless stated otherwise.
