# Rice Leaf Disease Detection Using Deep Learning

A deep learning project that explores automated classification of rice leaf diseases using Convolutional Neural Networks (CNN) and transfer learning. The project compares four deep learning architectures to identify and classify three types of rice leaf diseases.

## Project Overview

Rice is one of the world's most important food crops, and leaf diseases can significantly affect crop health and agricultural productivity. Early identification of plant diseases can help support timely intervention and better crop management.

This project develops an image classification pipeline to identify three rice leaf diseases from leaf images using deep learning techniques.

The project focuses on exploratory data analysis, image preprocessing, data augmentation, model development, performance evaluation, and comparison of different architectures.

## Objectives

- Explore and understand the rice leaf image dataset.
- Perform image preprocessing and data augmentation.
- Develop a custom Convolutional Neural Network.
- Implement transfer learning using pre-trained architectures.
- Compare model performance using classification metrics.
- Identify the strengths and limitations of each model.

## Dataset Description

The dataset contains images belonging to three rice leaf disease categories.

| Disease Class         | Number of Images |
| --------------------- | ---------------: |
| Leaf Smut             |               39 |
| Brown Spot            |               40 |
| Bacterial Leaf Blight |               40 |
| **Total**             |          **119** |

### Exploratory Data Analysis

The dataset was examined to understand its structure, image properties, and class distribution.

Key observations:

- 119 readable images were identified.
- The dataset contains three disease categories.
- Images were available in 34 distinct dimensions.
- No unreadable images were detected.
- No exact duplicate image groups were identified.

## Technologies and Libraries

- Python
- Jupyter Notebook
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- PIL (Python Imaging Library)

## Methodology

### 1. Data Preprocessing

The images were prepared for deep learning model training through:

- Image resizing to 128 × 128 pixels.
- Aspect-ratio-preserving padding.
- RGB image processing.
- Label encoding.
- Stratified dataset splitting.

### 2. Dataset Splitting

The dataset was divided into three subsets:

| Dataset    | Percentage | Images |
| ---------- | ---------: | -----: |
| Training   |        70% |     83 |
| Validation |        15% |     18 |
| Testing    |        15% |     18 |

Stratified splitting was used to maintain class representation across the subsets.

### 3. Data Augmentation

Image augmentation was applied dynamically during model training to introduce image variations.

Techniques included:

- Horizontal flipping
- Rotation
- Translation
- Zoom
- Contrast adjustment

### 4. Deep Learning Models

Four architectures were implemented and evaluated:

**Custom CNN**

A convolutional neural network developed to establish a baseline classification model.

**MobileNetV2**

A lightweight pre-trained architecture used for transfer learning.

**EfficientNetB0**

An efficient convolutional architecture evaluated for its feature extraction and classification capabilities.

**ResNet50**

A residual neural network used to investigate deeper feature extraction through transfer learning.

ImageNet-pretrained weights were used for the transfer learning models, with fine-tuning applied to the final 20 layers.

## Model Evaluation

The models were evaluated using accuracy, precision, recall, and F1-score.

### Test Set Performance

| Model          | Test Accuracy | Macro F1-Score |
| -------------- | ------------: | -------------: |
| Custom CNN     |         33.3% |          23.5% |
| MobileNetV2    |         77.8% |          77.0% |
| EfficientNetB0 |         72.2% |          69.3% |
| ResNet50       |         83.3% |          83.6% |

### Validation Performance

| Model          | Validation Accuracy |
| -------------- | ------------------: |
| Custom CNN     |               50.0% |
| MobileNetV2    |               66.7% |
| EfficientNetB0 |               88.9% |
| ResNet50       |               83.3% |

### Key Findings

- The custom CNN provided a baseline for comparison.
- Transfer learning models achieved better test performance than the custom CNN.
- EfficientNetB0 achieved the highest validation accuracy.
- ResNet50 achieved the highest observed test accuracy and macro F1-score.
- The results demonstrate the potential of transfer learning for small image classification datasets.

## Challenges and Limitations

- The dataset contains a relatively small number of images.
- Variations in image dimensions required consistent preprocessing.
- Model performance may be affected by the limited number of training samples.
- The test set contains only 18 images, so the reported test metrics have considerable uncertainty.
- Further evaluation using a larger and more diverse dataset is necessary before considering real-world deployment.

## Future Improvements

- Expand the dataset with additional rice leaf images.
- Evaluate more deep learning architectures.
- Conduct controlled experiments to measure the impact of augmentation.
- Apply hyperparameter tuning.
- Improve model generalization through additional training data.
- Explore deployment through a web-based disease prediction application.

## Project Structure

```text
Rice-Leaf-Disease-Detection/
│
├── Rice_Leaf_Disease_DEENAJOSE.ipynb
├── PRCP-1001-RiceLeaf.pdf
├── PRCP-1001-RiceLeaf.zip
└── README.md
```

## How to Run

1. Clone this repository:

```bash
git clone https://github.com/deenajose/Rice-Leaf-Disease-Detection.git
```

2. Navigate to the project directory:

```bash
cd Rice-Leaf-Disease-Detection
```

3. Open the Jupyter Notebook:

```bash
jupyter notebook Rice_Leaf_Disease_DEENAJOSE.ipynb
```

4. Execute the notebook cells in sequence.

Ensure the dataset is extracted and available at the location expected by the notebook before running the analysis.

## Conclusion

This project demonstrates the application of deep learning and transfer learning techniques to rice leaf disease classification. By comparing a custom CNN with MobileNetV2, EfficientNetB0, and ResNet50, the project investigates how different architectures perform on a small agricultural image dataset.

The results provide a foundation for further experimentation, improved classification performance, and potential development of an automated plant disease identification system.

---

**Project Domain:** Deep Learning | Computer Vision | Agricultural AI

**Author:** Deena Jose

**GitHub:** https://github.com/deenajose
