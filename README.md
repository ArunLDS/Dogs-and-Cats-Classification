# Cats vs Dogs Image Classification

## Overview
This project aims to classify images of cats and dogs using machine learning techniques. The dataset used consists of images labeled as either cat or dog, and various models are trained to distinguish between the two.   
[View this notebook in kaggle](https://www.kaggle.com/code/arunl15/dogs-vs-cats-ml)

## Dataset
The dataset used for this project is from Kaggle's Dogs vs. Cats competition.

[Click here to get the dataset](https://www.kaggle.com/competitions/dogs-vs-cats/data)

### Preprocessing & Model Training Key Steps
- The images are downscaled to 15x15 while maintaining the aspect ratio to avoid distortions. Empty areas are padded with black borders.
- Wavelet decomposition is used to extract components such as edges, textures, and other patterns from the images. Low-frequency data is removed, and the image is reconstructed.
- The resized and wavelet-processed images are horizontally stacked and used for training the classifiers.
- RandomForestClassifier, SVC, and XGBoostClassifier models are trained on this dataset and evaluated.
- PCA was used to reduce the dimensionality of training data for SVC classifier since training takes long time with SVC for high dimensional data
- Optuna is used to optimize the XGBoostClassifier model for maximizing accuracy. The best accuracy achieved on the test set is 71%.
