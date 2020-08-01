# SIIM-Classification-Kaggle

Notebook for SIIM Classification Competion Kaggle V1

The data provided is image od skin lesion as well as the metadata of that patient.
First preprocessing of the data is done to take care of the Nan values as well as other 
categorical data, then a custom model is developed to classify the patient as benign or malignant

The model consists of three networks,

One convolutional network that will take in the image and generate an embedding vector of dimension [B, 512]
Another data takes in the metadata about the patient provided in the csv file and generates an embedding vector of dimension [B, 512]

These two vectors are then simply added, and the passed on two a Fully Connected Network (FCN) and classification is done using softmax
as the activation function in the last layer.

For loss function currently using cross entropy loss. 

Since two types of data is available different architectures and training techniques are possible. Plan to explore all of them over time
