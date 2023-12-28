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
We prepare the images creating a dataset and normalising the images.

