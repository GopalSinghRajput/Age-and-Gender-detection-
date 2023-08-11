# Age-and-Gender-detection
👋 Welcome to my face recognition CNN model project! This project uses a pre-trained CNN model to predict the age and gender of faces based on face data that includes age, gender, and ethnicity.

# Dataset
The dataset used for this project is available [here](https://www.kaggle.com/datasets/nipunarora8/age-gender-and-ethnicity-face-data-csv)

# Model
The face recognition CNN model is implemented in Python using TensorFlow and Keras. The code for age and gender prediction is available in the notebook  The architecture of the models is as follows:
~~~
Model: "Age"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d_22 (Conv2D)          (None, 46, 46, 64)        640       
 max_pooling2d_15 (MaxPoolin  (None, 23, 23, 64)       0         
 g2D)                                                            
 batch_normalization_15 (Bat  (None, 23, 23, 64)       256       
 chNormalization)                                                
 conv2d_23 (Conv2D)          (None, 23, 23, 64)        36928     
 conv2d_24 (Conv2D)          (None, 21, 21, 64)        36928     
 max_pooling2d_16 (MaxPoolin  (None, 10, 10, 64)       0         
 g2D)                                                            
 dropout_15 (Dropout)        (None, 10, 10, 64)        0         
 batch_normalization_16 (Bat  (None, 10, 10, 64)       256       
 chNormalization)                                                
 conv2d_25 (Conv2D)          (None, 10, 10, 64)        36928     
 conv2d_26 (Conv2D)          (None, 8, 8, 64)          36928     
 max_pooling2d_17 (MaxPoolin  (None, 4, 4, 64)         0         
 g2D)                                                            
 dropout_16 (Dropout)        (None, 4, 4, 64)          0         
 flatten_4 (Flatten)         (None, 1024)              0         
 dense_8 (Dense)             (None, 128)               131200    
 dropout_17 (Dropout)        (None, 128)               0         
 dense_9 (Dense)             (None, 1)                 129       
=================================================================
Total params: 289,281
Trainable params: 288,641
Non-trainable params: 640
~~~

~~~
Model: "Gender"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d_28 (Conv2D)          (None, 46, 46, 64)        640       
 max_pooling2d_19 (MaxPoolin  (None, 23, 23, 64)       0         
 g2D)                                                            
 batch_normalization_19 (Bat  (None, 23, 23, 64)       256       
 chNormalization)                                                
 conv2d_29 (Conv2D)          (None, 21, 21, 64)        36928     
 max_pooling2d_20 (MaxPoolin  (None, 10, 10, 64)       0         
 g2D)                                                            
 dropout_19 (Dropout)        (None, 10, 10, 64)        0         
 batch_normalization_20 (Bat  (None, 10, 10, 64)       256       
 chNormalization)                                                
 conv2d_30 (Conv2D)          (None, 8, 8, 64)          36928     
 conv2d_31 (Conv2D)          (None, 6, 6, 64)          36928     
 max_pooling2d_21 (MaxPoolin  (None, 3, 3, 64)         0         
 g2D)                                                            
 dropout_20 (Dropout)        (None, 3, 3, 64)          0         
 flatten_5 (Flatten)         (None, 576)               0         
 dense_10 (Dense)            (None, 128)               73856     
 dropout_21 (Dropout)        (None, 128)               0         
 dense_11 (Dense)            (None, 1)                 129       
=================================================================
Total params: 149,185
Trainable params: 148,801
Non-trainable params: 384
~~~

# Results
The models achieved an silhouette_score
of 0.436. 

# Acknowledgements
This project was inspired by [here](https://www.kaggle.com/code/gcdatkin/face-image-classification-with-cnns)
