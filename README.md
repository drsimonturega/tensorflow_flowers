# tensorflow_flowers

## Contents
* Introduction
* Milesstones
  
### Introduction

This is a work through of the Image classification tutorial at https://www.tensorflow.org/tutorials/images/classification.The tutorial teaches image classification tf.keras.Sequential model using a provided directory of flower photos. 

### Milestones
#### Milestone 1
Setup python environment

Pakeage inatallation ```conda install matplotlib```, ```conda install tensorflow``` .

Download the images usthing pathlib, not quite sure where the files are stored,
```
import pathlib

dataset_url = "https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz"
data_dir = tf.keras.utils.get_file('flower_photos.tar', origin=dataset_url, extract=True)
data_dir = pathlib.Path(data_dir).with_suffix('')
```

#### Milestone 2
We prepare the images creating a dataset and normalising the images.The data set is split 80% training and 20% validation. splitting the data into batches  of 32 image tensors. 

#### Milestone 3

We build a basic Keras model with an Adam opitimizer and a Sparse Categorical Cross entropy loss function. the first model is train for 10 epochs thats 92 trainings of the 32 image tensors. This was tested 

![Alt](/snapshot1.png "analysis of first fit")

The analysis of first fit suggested the model had been overfit!. to improve the training we used data augmentation and dropout methods to improve the model, the number of epochs was increased to 15.


