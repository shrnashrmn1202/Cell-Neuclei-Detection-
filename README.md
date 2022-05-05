# Cell Nuclei Detection using Semantic Segmentation with U-Net

The aim of the project is to detect cell nuclei from biomedical images effectively. As cell nuclei vary in shapes and sizes, semantic segmentation proves to be the best approach to detect them. A deep learning model is trained and deployed for this task. The model is trained with dataset from:  https://www.kaggle.com/competitions/data-science-bowl-2018/data

![image](https://user-images.githubusercontent.com/100325884/166873317-dd419720-b661-4945-83d1-b180570f351a.png)


## IDE and Framework
This project is created using Sypder as the main IDE. The main frameworks used in this project are TensorFlow, Numpy, Matplotlib, OpenCV and Scikit-learn.

## Methodology
The methodology is inspired by a documentation available in the official TensorFlow website: https://www.tensorflow.org/tutorials/images/segmentation

### 1. Data Preprocessing
The datasets are cleaned first by removing unwanted features and label is encoded with label encoder

### 2. Data Pipeline
Data is then split into train-test sets, with a ratio of 70:30.

### 3. Model Pipeline
A feedforward neural network is constructed that is catered for classification problem. The structure of the model is fairly simple with three types of layers:
- Input layer
- Hidden layer
- Output layer

The model is trained with a batch size of 100 and for 100 epochs. The training accuracy of 99% and validation accuracy of 95%. The figure below shows the model accuracy of each epochs

![image](https://user-images.githubusercontent.com/100325884/163185927-f944b511-f148-44c3-b7b7-42498f4b7fb3.png)


## Results
Upon evaluating the model with test data, the model obtain the following test results:
- Test Accuracy: 95%

![image](https://user-images.githubusercontent.com/100325884/163182500-3995d029-215c-4553-95dc-5c3f6dd89974.png)
![image](https://user-images.githubusercontent.com/100325884/163182716-828cb7b1-2098-48c1-acd8-b16442f773ba.png)
