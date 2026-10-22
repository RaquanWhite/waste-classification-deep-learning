# waste-classification-deep-learning
# Waste Classification Using Deep Learning

### Binary Image Classification | TensorFlow • Keras • VGG16 • Transfer Learning

## Project Overview

This project explores deep learning techniques for classifying waste images into two categories: **Organic** and **Recyclable**.

Using a pretrained VGG16 convolutional neural network (CNN), I implemented and evaluated two approaches:

1. **Feature Extraction:** Using pretrained convolutional features with newly trained classification layers.
2. **Fine-Tuning:** Unfreezing selected pretrained layers to improve classification performance.

The objective was to evaluate how transfer learning and fine-tuning affect image classification accuracy.

This project was completed as part of IBM's *Deep Learning with Keras* course and executed using Google Colab with GPU acceleration.

## Model Performance

| Metric | Feature Extraction | Fine-Tuned Model |
|---|---|---|
| Test Accuracy | 77% | **81%** |
| Weighted Precision | 77% | **82%** |
| Weighted Recall | 77% | **81%** |
| Weighted F1-Score | 77% | **81%** |

**Key Result:** Fine-tuning improved test accuracy by 4 percentage points compared with the feature-extraction model.

## Technologies Used

- Python
- TensorFlow and Keras
- VGG16 Convolutional Neural Network
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- Transfer Learning and Fine-Tuning

## Methodology

### 1. Data Preparation

Prepared image datasets representing organic and recyclable waste.

- Resized images to 150 × 150 pixels.
- Normalized pixel values.
- Applied image augmentation, including shifts and horizontal flips.
- Created training, validation, and testing image generators.

### 2. Feature Extraction

Loaded VGG16 with pretrained ImageNet weights and removed its original classification head.

The convolutional base was frozen while new classification layers were trained for binary waste classification.

### 3. Model Training

Configured the model using:

- Binary crossentropy loss
- Adam optimizer
- Learning rate of 0.00001
- Accuracy as the primary training metric

Monitored training and validation accuracy and loss.

### 4. Fine-Tuning

Unfroze selected upper layers of VGG16 and retrained the model to adapt its learned features to the waste-classification dataset.

### 5. Model Evaluation

Evaluated both models on a held-out test dataset using accuracy, precision, recall, and F1-score.

Visualized training curves and individual predictions to compare model performance.

## Results and Observations

The fine-tuned model achieved better overall classification performance than the feature-extraction model.

This experiment demonstrated how adapting pretrained neural network features to a specific classification task can improve predictive performance.

The results also highlight the importance of evaluating models on test data rather than relying exclusively on training accuracy.

## Project Files

- `Final-Proj-Classify-Waste-Products.ipynb` — Jupyter notebook containing model development, training, evaluation, and visualizations.

## Future Improvements

Potential extensions include:

- Experimenting with alternative architectures such as ResNet and EfficientNet.
- Expanding the dataset to include additional waste categories.
- Performing hyperparameter optimization.
- Evaluating model robustness under different lighting and image conditions.
- Developing a web application for real-time image classification.

## About This Project

This is a guided educational project completed through IBM's *Deep Learning with Keras* course on Coursera. The provided notebook served as the foundation for implementing, training, fine-tuning, and evaluating the models.

The repository documents my practical learning experience with deep learning and computer vision as I continue developing skills in AI and machine learning engineering.
