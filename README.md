# MNIST-LeNet
MNIST ("Modified National Institute of Standards and Technology") is the de facto “hello world” dataset of computer vision. Since its release in 1999, this classic dataset of handwritten images has served as the basis for benchmarking classification algorithms. As new machine learning techniques emerge, MNIST remains a reliable resource for researchers and learners alike.
___
## MNIST dataset

The MNIST database is available at https://www.kaggle.com/c/digit-recognizer/data

The MNIST database is a dataset of handwritten digits.  Each image is represented by 28x28 pixels, each
containing a value 0 - 255 with its grayscale value.

![](hhttps://raw.githubusercontent.com/imsahil007/MNIST-LeNet/master/res/data.png?token=AISMIWFVZWD2XZFFEBCILI27DEXB2)

The digits have been size-normalized and centered in a fixed-size image.
# LeNet:
LeNet's design:
[](https://github.com/imsahil007/MNIST-LeNet/raw/master/res/LeNet5.png)

## Tweaks that I made:

* Two stacked 3x3 filters replace the single 5x5 filters. These become nonlinear 5x5 convolutions
* A convolution with stride 2 replaces pooling layers. These become learnable pooling layers.
* ReLU activation replaces sigmoid.
* Batch normalization is added
* Dropout is added
* RMSProp used in place of Adam optimizer

# Use saved model:
Download [this](https://github.com/imsahil007/MNIST-LeNet/raw/master/res/model_data.zip)
Extract model_data.zip
```
from tensorflow import keras
model = keras.models.load_model($model_path)
```
You can also use this [sample](https://github.com/imsahil007/MNIST-LeNet/blob/master/res/sample.pdf)
# References:
* [LeNet Architecture](http://yann.lecun.com/exdb/publis/pdf/lecun-01a.pdf)
* [Keras optimizer](https://keras.io/api/optimizers/)
