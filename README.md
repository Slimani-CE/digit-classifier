# Digit Classifier : End to End application

This is a digit classifier application that allows users to draw handwritten digits and get predictions using a trained Artificial Neural Network (ANN) model.
## 📚 Table of Content
  - [📚 Table of Content](#-table-of-content)
  - [📝 Overall](#-overall)
  - [📦 Dependencies](#-dependencies)
  - [📝 Implementation](#-implementation)
  - [✅ Test](#-test)
  - [📊 Perspective](#-perspective)


## 📝 Overall
The application consists of three main components: a frontend, a backend, and the machine learning part. The frontend provides a user-friendly interface for drawing digits, the backend handles API requests and serves predictions, and the machine learning part includes the training of the ANN model on the MNIST dataset.

## 📦 Dependencies
![TENSORFLOW](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white) ![Opencv](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white) ![pickle](https://img.shields.io/badge/Pickle-FFA500?style=for-the-badge&logo=pickle&logoColor=white) ![numpy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white) ![fastapi](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white) ![uvicorn](https://img.shields.io/badge/Uvicorn-2C3E50?style=for-the-badge&logo=fastapi&logoColor=white) ![JS](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) ![html5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![css3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

## 📝 Implementation

The implementation of the application includes the following steps:

1. **Machine Learning Part**: In the `ml` directory, you can find the Jupyter Notebook (`MNIST_ANN_Classifier.ipynb`) that demonstrates the training and evaluation of the ANN model on the MNIST dataset. The trained model is then exported using the pickle library and saved as `digit-classifier-model.pkl`.

2. **Backend**: The backend is built using the FastAPI framework in Python. The backend code can be found in the `backend` directory. It includes a FastAPI service (`main.py`) that imports the trained model using the pickle library and exposes a POST endpoint (`/digit-classifier-api`) to receive images for classification. The backend handles image preprocessing and uses the `DigitClassifier` class to make predictions. This API is deployed on an `Oracle Cloud ubuntu instance`, and can be used all around the world by requesting this `POST` endpoint `https://132.145.60.229:1337/digit-classifier-api` and providing the image to classify as a parameter called `image` 
   
3. **Frontend**: The frontend code can be found in the `frontend` directory. It includes an HTML file (`index.html`) with a canvas element for drawing digits and JavaScript code (`script.js`) to handle the drawing, clearing, and submitting of the drawn image. When the user submits the image, it is converted to a data URL, sent as multipart form data in a POST request to the backend API, and the predicted digit is displayed.

## ✅ Test
![Illustration gif](assets/illustration.gif)

## 📊 Perspective
Collect User Feedback: One potential avenue for improving the digit classifier model is to collect user feedback on the accuracy of the classified images. By allowing users to provide feedback on whether the predicted digit matches their intended input, we can gather valuable data to refine and enhance the model's performance over time. This feedback loop can help identify and address any misclassifications or areas of improvement, ultimately leading to a more accurate and reliable digit recognition system."