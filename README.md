# Keras to Caffe2 Converter
[Caffe2](https://github.com/caffe2/caffe2) is currently one of the fastest deep learning libraries available on both Android and iOS. 
However, a lot of researches and engineers use [Keras](https://github.com/fchollet/keras) to train their models.
This tool combines the best of both worlds, as it allows the models trained in Keras and to be deployed on Android and iOS by converting them to Caffe2.

### Prerequisites
* [Numpy](https://github.com/numpy/numpy)  <br />
* [Keras](https://github.com/fchollet/keras) <br />
* [Caffe2](https://github.com/caffe2/caffe2)  <br />
### Installing
Clone the repository and install it as a python module:
```
git clone https://github.com/arakhmat/keras-to-caffe2
cd keras-to-caffe2
pip install -e .
```
While in the same directory, test the installation by running:
```
python test_conv.py
```

## Supported Layers
* Conv2D
* MaxPool2D
* Flatten
* Dense
* BatchNormalization (for Conv2D layer only)

## Supported Activations
* Relu
* Softmax

## Known Limitations
* Only convolutional 2D neural networks are supported
* There is no BatchNormalization layer for dense networks
* Conv2D and MaxPool2D layers must have 'channel_first' data format
* Conv2D layers cannot be padded
* It is assumed that a network always has Conv2D as its first layer

