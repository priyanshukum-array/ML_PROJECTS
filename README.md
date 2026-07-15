# Machine Learning & Deep Learning Projects

This repository documents my learning journey in Machine Learning and Deep Learning through hands-on projects. Rather than only studying theory, I focused on implementing different neural network architectures to understand where they are used, how they work, and how they perform on different types of data.

The projects cover the three fundamental deep learning architectures:
- **Artificial Neural Networks (ANN)** for structured/tabular data.
- **Convolutional Neural Networks (CNN)** for image classification tasks.
- **Recurrent Neural Networks (RNN/LSTM)** for sequential and time-series data.

Each project includes data preprocessing, model development, training, evaluation, and performance analysis using appropriate metrics such as confusion matrices, classification reports, and accuracy. The objective of this repository is to build a strong practical foundation in deep learning while maintaining clean, well-documented implementations.
# Human Activity Recognition using Artificial Neural Networks (ANN)

## Overview

This project implements an Artificial Neural Network (ANN) to classify human activities using smartphone sensor data. The objective was to understand the fundamentals of deep learning by building a neural network from scratch and applying it to a real-world multiclass classification problem.

The model predicts different human activities based on features extracted from accelerometer and gyroscope sensors. Since each sample consists of independent numerical features, an ANN is an appropriate architecture for this task.

---

## Dataset

**Dataset:** UCI Human Activity Recognition (HAR) Dataset

The dataset contains sensor measurements collected from smartphones worn by participants while performing daily activities.

### Activities Classified

- Walking
- Walking Upstairs
- Walking Downstairs
- Sitting
- Standing
- Laying

---

## Project Workflow

- Loaded and explored the dataset
- Performed data preprocessing
- Split the dataset into training and testing sets
- Built an Artificial Neural Network using TensorFlow/Keras
- Trained and validated the model
- Evaluated performance using accuracy, confusion matrix, and classification report
- Performed basic hyperparameter tuning by experimenting with different hidden layer sizes
- Saved the trained model for future inference

---

## Model Architecture

- Input Layer
- Dense Hidden Layer (ReLU)
- Dense Hidden Layer (ReLU)
- Output Layer (Softmax)

---

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## Results

- Achieved approximately **97% test accuracy**
- Successfully classified six different human activities
- Evaluated model performance using:
  - Accuracy
  - Confusion Matrix
  - Classification Report

---

## Key Concepts Learned

- Artificial Neural Networks (ANN)
- Forward Propagation
- Backpropagation
- Activation Functions (ReLU & Softmax)
- Loss Functions
- Hyperparameter Tuning
- Model Evaluation
- Saving and Loading Trained Models

---

## Future Improvements

- Experiment with deeper neural network architectures
- Perform systematic hyperparameter optimization
- Compare ANN performance with traditional machine learning algorithms
- Deploy the trained model as a simple web application
# Pneumonia Detection from Chest X-ray Images using Convolutional Neural Networks (CNN)

## Overview

This project focuses on detecting pneumonia from chest X-ray images using deep learning techniques. The primary objective was to understand how Convolutional Neural Networks (CNNs) learn spatial features from images and to compare the performance of different computer vision approaches.

Three different models were implemented throughout the project. The first model was a custom CNN built entirely from scratch to understand the working of convolutional layers, pooling operations, and feature extraction. The second model applied Transfer Learning using MobileNetV2, leveraging a pre-trained network trained on ImageNet. Finally, the third version explored Fine-Tuning by unfreezing the final layers of MobileNetV2 to adapt the network specifically for chest X-ray classification.

---

## Dataset

**Dataset:** Chest X-ray Pneumonia Dataset (Kaggle)

The dataset consists of chest X-ray images divided into two classes:

- Normal
- Pneumonia

The images were resized, normalized, and prepared for deep learning training.

---

## Project Workflow

- Loaded the image dataset
- Image preprocessing and normalization
- Training and validation split
- Built a custom CNN from scratch
- Trained and evaluated the custom CNN
- Implemented Transfer Learning using MobileNetV2
- Fine-tuned the pre-trained MobileNetV2 model
- Compared the performance of all three approaches
- Evaluated models using test accuracy and loss

---

## Model Versions

### Version 1 — Custom CNN

A CNN was built from scratch using:

- Conv2D Layers
- MaxPooling2D
- Flatten Layer
- Dense Layers
- Sigmoid Output Layer

This version was implemented to understand how convolutional neural networks learn image features directly from pixel data.

---

### Version 2 — Transfer Learning (MobileNetV2)

The custom CNN was replaced with MobileNetV2 pre-trained on ImageNet.

Only the final classification layer was trained while the feature extraction layers remained frozen.

This significantly reduced training time while improving model performance.

---

### Version 3 — Fine-Tuning

The final layers of MobileNetV2 were unfrozen and retrained using a very small learning rate.

This experiment demonstrated how fine-tuning allows a pre-trained model to adapt to a specific dataset while preserving previously learned image features.

---

## Technologies Used

- Python
- TensorFlow / Keras
- OpenCV
- NumPy
- Matplotlib
- Scikit-learn
- Kaggle Dataset

---

## Results

### Version 1 — Custom CNN

- Learned CNN architecture from scratch
- Achieved approximately **72% test accuracy**

### Version 2 — MobileNetV2 (Transfer Learning)

- Achieved approximately **87% test accuracy**
- Faster convergence than the custom CNN

### Version 3 — Fine-Tuning

- Explored fine-tuning by retraining the final layers of MobileNetV2
- Compared performance with the frozen model to understand the effect of transfer learning and fine-tuning

---

## Key Concepts Learned

- Image Preprocessing
- Convolutional Neural Networks (CNN)
- Convolution Filters
- Max Pooling
- Feature Extraction
- Flatten vs Global Average Pooling
- Binary Image Classification
- Transfer Learning
- MobileNetV2
- Fine-Tuning
- ImageNet Pre-trained Models
- Model Evaluation

---

## Future Improvements

- Apply Data Augmentation
- Experiment with EfficientNet and ResNet architectures
- Hyperparameter Optimization
- Deploy the trained model as a web application
- Extend the model to classify multiple lung diseases
