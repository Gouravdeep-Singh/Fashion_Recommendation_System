# Fashion_Recommendation_System

# Objective
The aim of our project is to learn and implement about Deep Learning CNN Architecture as well as Image Processing. We have decided to build a Fashion Recommendation system which provides five similar images to the given image. We will be building our model instead of using Pre-Trained model like Resnet50, VG16. To handle the response time we will converting our images into vectors and extract their features. later on we save the model and extracted features to reduce processing time and provide recommendation by adding the features of our input image with the dataset. 

# Libraries

Tensorflow
Numpy
Pandas
Matplotlib
Seaborn
CV2
Scikit-Learn
Pickle

# Workflow 

* Load the dataset and perform EDA. After exploring, visualize the dataset using matplotlib and seaborn
  
* Start building the CNN Model. It has 3 convolution, 3 pooling layers, one flatten layer, 2 dense layers and a dropout of 0.5 for optimization

* Model is complied and optimized uisng Adam with a learning rate of 0.001

* Before extracting the features we resize the image uisng CV2 according to the size set in our model

* Then we calculate the cosine similarity of all the images stored in the dataset and save the normalized features in a numpy file

* After that we extract the features of our input image as well and combine it with the dataset providing recommendation

* We save the model as a pickle file so we don't have to repeat the process over and over again hence, saving time

* We load the pickle file and calculate similarity again but this time we also calculate similarity scores of our resulting five images for evaluation


  # Observations & Future scope

  * While exploration we found women had the largest share in types of clothes while clothes for respective seasons has almost similar share
 
  * The dataset contains fashion items which belong to the time period of 2010-18 with majority of items from the year 2012
 
  * Building our own CNN model was a challenge and while building we experimented with dropout and learning rate which produced different outputs. The best solution came with dropout of 0.5 and and learning rate of 0.001
 
  * To reduce the procesing time we converted the images into vectors and stored them in numpy file which reduced our output time by 70%
 
  * For future socpe, evaluation by similarity score won't be enough so it will be better to compare our model results with a pre-trained model
