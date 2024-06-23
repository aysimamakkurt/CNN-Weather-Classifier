# CNN Weather Detection

## Description
This project uses a Convolutional Neural Network (CNN) to classify images into four different weather conditions: fog, daily (clear), night, and rain. The CNN model is trained on a large dataset of weather images, and can accurately predict the weather condition in a given image.

## Installation
1. Clone this repository: `git clone https://github.com/yourusername/CNN-Weather-Classifier.git`
2. Install the required packages: `pip install -r requirements.txt`

## Dataset
This project uses four different datasets:
- Syndrone Dataset
- MWD Dataset
- ACDC Dataset
- UAVid Dataset

Each dataset consists of images under different weather conditions. The links to these datasets are provided in the project report.

## Model
The model is built using a pre-trained model as a base. The weights of the pre-trained model are frozen, and its output is passed through several additional layers:

- A Flatten layer to convert the output to a 1D tensor.
- Dense layers with 512, 256, 128, and 64 neurons, all using ReLU activation.
- Dropout layers after the 128-neuron and 64-neuron layers to prevent overfitting.
- A final Dense layer with a number of neurons equal to the number of classes, using softmax activation for multi-class classification.

The model is compiled with the Adam optimizer (learning rate 0.0001), categorical cross entropy loss, and accuracy as the metric.

The `fit` method is used to train the model. It takes as input a training data generator, a validation data generator, the number of steps per epoch for training and validation, and the number of epochs.
