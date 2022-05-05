# Cell Nuclei Detection using Semantic Segmentation with U-Net

The aim of the project is to detect cell nuclei from biomedical images effectively. As cell nuclei vary in shapes and sizes, semantic segmentation proves to be the best approach to detect them. A deep learning model is trained and deployed for this task. The model is trained with dataset from:  https://www.kaggle.com/competitions/data-science-bowl-2018/data

![image](https://user-images.githubusercontent.com/100325884/166873317-dd419720-b661-4945-83d1-b180570f351a.png)


## IDE and Framework
This project is created using Sypder as the main IDE. The main frameworks used in this project are TensorFlow, Numpy, Matplotlib, OpenCV and Scikit-learn.

## Methodology
The methodology is inspired by a documentation available in the official TensorFlow website: https://www.tensorflow.org/tutorials/images/segmentation

### 1. Data Preprocessing
The dataset files contains a train folder for training data and test folder for testing data, in the format of images for inputs and image masks for the labels. The input images are preprocessed with feature scaling. The labels are preprocessed such that the values are in binary of 0 and 1. No data augmentation is applied for the dataset. 

### 2. Data Pipeline
The train data is split into train-validation sets, with a ratio of 80:20

### 3. Model Pipeline
The model architecture used for this project is U-Net. In summary, the model consist of two components:
1. The downward stack (serves as the feature extractor) 
2. The upward stack (helps to produce pixel-wise output). 

The model is trained with a batch size of 16 and 100 epochs. Early stopping is also applied in the model training. The training stops at epoch 22, with a training accuracy of 97% and validation accuracy of 96%.


## Results
Upon evaluating the model with test data, the model obtain the following test results:
- Test Accuracy: 96%

Some predictions are also made with the model using some of the test data. The actual output masks and prediction masks are shown in figures below:
![image](https://user-images.githubusercontent.com/100325884/166876337-085666b7-7deb-4882-bb13-2de6b6cdde25.png)

