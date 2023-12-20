
# NutriChive : Food Ingredient, Recipe, and Nutrition Archive

An application that utilize machine learning, especially in the field of computer vision, to create an application that can recognize food ingredients and recommend food recipes that can be obtained from them so that food ingredients can be utilized properly.

## Setup
### Environtment

This experiment was executed on the Kaggle platform, leveraging the GPU P100 accelerator. The implementation was carried out using the Python programming language, with the TensorFlow framework serving as the primary computational tool. This choice of infrastructure and technology stack ensures a robust and scalable environment for conducting sophisticated machine learning tasks.

### Dataset
The dataset utilized for training the model is the Fruit and Vegetable Image Recognition dataset (Kritik Seth, 2020). The dataset consists of 36 classes contains 3 folders:
- Training Set (100 images each class)
- Validation Set (10 images each class)
- Testing Set (10 images each class)

The image in the dataset is resized to a size of 224 x 224 pixels. In addition, to prevent overfitting, augmentation is also carried out on the training set in the form of random brightness, random rotation, random contrast, random rotate, and also random zoom until finally 6140 training set data is obtained.

Source :

Kritik Seth, "Fruits and Vegetables Image Recognition Dataset," Kaggle 2020 [https://www.kaggle.com/kritikseth/fruit-and-vegetable-image-recognition]

## Model
### Architecture
The model we used was created from scratch. We used Convolutional Neural Network in creating it. After the convolution process we do downsampling by using max pooling operation. The activation function we use is ReLU. The model we created consists of 5 levels of convolution process with the number of filters/kernels applying multiples of 2 at each level. In addition, at the end of the model there is a Global Max Pooling operation and also a dense layer with 36 units according to the number of classes in the dataset we use.
