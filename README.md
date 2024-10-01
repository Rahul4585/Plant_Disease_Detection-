<div align="center">

# 🌿 Plant Disease Detection from Images 🌿

</div>

<div align="center">

[![](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=darkgreen)](https://www.python.org)
[![](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/stable/)
[![](https://img.shields.io/badge/Numpy-007EBA?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org)
[![](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)](https://pytorch.org)
[![](https://img.shields.io/badge/ONNX-00B2E2?style=for-the-badge&logo=onnx&logoColor=white)](https://onnx.ai)
[![](https://img.shields.io/badge/TensorFlow-FF4B00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://www.tensorflow.org)
[![](https://img.shields.io/badge/Matplotlib-FF7F0E?style=for-the-badge&logo=matplotlib&logoColor=white)](https://matplotlib.org)

</div>

<div align="center">

![Screenshot_2024-09-27_190325-transformed](https://github.com/user-attachments/assets/3f9a3972-a573-4257-9dc2-2cc0d896b16d)


</div>

## 📋 Project Overview

Our project focuses on creating an intuitive Streamlit application that empowers users to upload images of plant leaves for accurate identification of plant diseases. Utilizing a Convolutional Neural Network (CNN) model, this tool is designed to support farmers and gardeners in swiftly diagnosing plant health issues, thereby facilitating timely interventions to enhance crop management.

## 📂 Dataset

The dataset for our project comprises images categorized into **38 classes** of plant species and their associated diseases, structured into training, validation, and testing subsets. 

**Key classes include:**

- **Tomatoes** (e.g., Late blight, Healthy, Early blight)
- **Grapes** (e.g., Healthy, Black rot)
- **Oranges** (e.g., Huanglongbing)
- **Potatoes** (e.g., Healthy, Late blight)
- **Corn (maize)** (e.g., Northern Leaf Blight)
- **Strawberries** (e.g., Leaf scorch)
- **Other classes** such as Peaches, Apples, Soybeans, Squash, Blueberries, and Cherries.

This structured dataset enables effective training and evaluation of machine learning models for plant disease detection.


## 📥 Download the Dataset

You can download the dataset from this link: [New Plant Diseases Dataset](https://www.kaggle.com/datasets/vipoooool/new-plant-diseases-dataset).

## 🎯 Objectives and Goals

Our project encompasses comprehensive development, including the establishment of an image upload interface using Streamlit, training the CNN model, and delivering a fully functional application that is easy to use. With a strong emphasis on real-world applicability, the project aims to equip farmers and gardeners with a rapid diagnosis tool, ultimately enabling them to respond effectively to plant diseases and optimize their agricultural practices.

## 🚀 Approach

### 1. Image Preprocessing
Implemented image preprocessing steps such as resizing, normalization, and augmentation to improve model performance. Utilized the **New Plant Diseases Dataset** from Kaggle, which contains images of plant leaves labeled with various diseases.

### 2. Disease Classification
Developed and trained a Convolutional Neural Network (CNN) model to classify plant diseases based on the uploaded images. Used the dataset from Kaggle for training and testing, applying techniques such as data augmentation and transfer learning to enhance model accuracy. Additionally, compared the performance of the **Custom CNN model** with at least three pretrained models to ensure the custom model outperforms existing ones. In our project, we have used these pre-trained models:

- **[VGG16](https://pytorch.org/vision/main/models/generated/torchvision.models.vgg16.html)**: A deep convolutional neural network known for its simplicity and effectiveness, featuring 16 weight layers and small receptive fields for improved feature extraction.

- **[AlexNet](https://pytorch.org/vision/main/models/generated/torchvision.models.alexnet.html)**: A pioneering deep learning model that significantly advanced image classification tasks, introducing techniques like ReLU activations and dropout regularization.

- **[DenseNet](https://keras.io/api/applications/densenet/)**: A convolutional neural network that enhances feature propagation and reuse by connecting each layer to every other layer in a feed-forward fashion, resulting in more efficient training.



### 3. Performance Metrics

We are predicting the different plant diseases using our **Custom CNN**. Therefore, the following are the __metrics__ that we used:

- [__Accuracy__](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html): Measures the overall correctness of the predictions.

- [__F1 Score__](https://towardsdatascience.com/micro-macro-weighted-averages-of-f1-score-clearly-explained-b603420b292f): Balances performance across all classes by averaging F1 scores.

- [__Precision__](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.precision_score.html#precision-score): Measures how many of the positive predictions were correct.

- [__Recall__](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.recall_score.html#recall-score): Evaluates the ability of the model to capture all relevant positive cases.

### 4. User Interface Development
We have created a web interface using Streamlit that allows users to upload images of plant leaves. Implemented validations to check the type of file uploaded (e.g., JPEG, PNG) and ensured that the application is intuitive and user-friendly, with clear instructions and feedback for users.

### 5. Deployment and Testing
Deployed the Streamlit application using Streamlit. Conducted extensive testing to ensure the application correctly predicts plant diseases and handles various image inputs effectively.

## 🔍 Model Comparison

<div align="center">
  
| **Model**                                                                                                                | **Accuracy (%)** | **Precision (%)** | **Recall (%)** | **F1-score (%)** |
|:-------------------------------------------------------------------------------------------------------------------------:|:----------------:|:------------------:|:--------------:|:----------------:|
| [**1. Custom CNN**](https://www.tensorflow.org/tutorials/images/cnn) | **87.56**        | **88.06**          | **87.56**      | **87.61**        |
| [**2. DenseNet**](https://keras.io/api/applications/densenet/) | 87.41            | 89.72              | 87.41          | 87.76            |
| [**3. AlexNet**](https://pytorch.org/vision/main/models/generated/torchvision.models.alexnet.html) | 87.12            | 88.29              | 87.12          | 87.15            |
| [**4. VGG16**](https://pytorch.org/vision/main/models/generated/torchvision.models.vgg16.html) | 85.32            | 86.84              | 85.32          | 85.36            |

</div>

- The **Custom CNN** model achieved the best overall performance, with the highest accuracy of **87.56%** and a strong F1-score of **87.61%**, making it the most reliable model for this task.
- **DenseNet** recorded an accuracy of **87.41%**, but it did not surpass **Custom CNN** in overall effectiveness.
- **AlexNet** had an accuracy of **87.12%**, falling behind the **Custom CNN**.
- **VGG16** showed the lowest accuracy at **85.32%**, with weaker overall performance.

- Overall, **Custom CNN** stands out as the best model, offering the highest accuracy and balanced performance, making it the optimal choice for this classification task.


## 🧪Streamlit Application

### Upload an Image:
Upload an image of a plant leaf through the Streamlit application interface.

### Get Predictions:
The application will display the predicted disease and its confidence score based on the uploaded image.

<p align="center">
  <img width="500" alt="corn" src="https://github.com/user-attachments/assets/3b399395-bc60-4662-b0cf-7f3d1688aed9"> 
  <img src="https://github.com/user-attachments/assets/18685bd2-49fd-4071-a82f-889a055d3c03" alt="streamlit" width="500"/>
</p>

## 📚 User Guide

For detailed instructions on using the application and interpreting predictions, please refer to the [User Guide](User_Guide.docx).


## 🚧 Challenges and Future Work

### Challenges:
In plant disease detection, one significant challenge is handling imbalanced datasets, where some diseases have fewer images for training. This imbalance can bias the model towards more common classes, resulting in poor performance on rare diseases. While the provided dataset was already augmented, implementing image preprocessing steps such as resizing, normalization, and further augmentation could enhance model performance. Moreover, optimizing the application for real-time inference is critical, as users expect quick and accurate predictions. Achieving low latency requires careful optimization of both the model architecture and the application infrastructure, ensuring seamless user experiences without compromising prediction accuracy.

### Future Work:
Future enhancements could include implementing a feedback mechanism for users to report incorrect predictions, providing valuable data for model improvement and fostering community engagement. Furthermore, expanding the model to recognize a wider range of plant species and diseases is crucial to meet the diverse needs of users in agriculture. By continually updating the dataset and refining the model, the application can become a vital tool for farmers and gardeners in managing plant health effectively.

## 🌱 Results

The project aims to deliver a fully functional Streamlit-based web application that allows users to upload images of plant leaves and receive accurate predictions about plant diseases. A detailed model performance report will accompany the application, highlighting the accuracy and other evaluation metrics of the CNN model. Additionally, the project will include a user guide that explains how to operate the application and interpret the results effectively.

