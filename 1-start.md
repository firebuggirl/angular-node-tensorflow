# MNIST TensorFlow/Angular Application

https://rubikscode.net/2019/09/09/integration-of-tensorflow-model-into-angular-application/

## Overview:

  - create an application in which user can `write down a number in some sort of the canvas` on the web page and `application will recognize which number is written` => use `MNIST data` set => contains 60000 images of handwritten digits => all the same size – `28×28` => available as a part TensorFlow library

  - images => use `Convolutional Neural Networks` => use several layers to detect features on the images => then neural networks to classify images based on those features

  - Detection of the features => `convolutional layers` =>  first detect low-level features (edges and curves...) => higher level features (face, hand, or hand-written digit...)

  - then additional layers to remove linearity

- from `./` => `which pip3 python3` => check to see if Python3 + pip3 are installed + additional layers for compressing the image and flattening

- then passed into a neural network, called `Fully-Connected Layer`


## Prerequisites/tools

`  pip3 install --upgrade pip `//decided to use Docker Ubuntu image w/ Python + python-pip
instead

` pip install tensorflowjs `//Python 2.7 will reach the end of its life on January 1st, 2020

` nvm use 12 `

` npm install -g @tensorflow/tfjs `

` npm install -g http-server `

` npm install -g angular-cli `

` ng new ang-tensor `

` ng serve `


## Building Convolution Neural Network

-  create a `neural network` using Python and TensorFlow high-level API


- Sequential class creates placeholder in which we can enter layers of neurons => building Convolutional Neural Network => follow explanation provided here(Introduction to Convolutional Neural Networks => https://rubikscode.net/2018/02/26/introduction-to-convolutional-neural-networks

  -  `Convolutional Layer` – Used to detect features

  -   `Non-Linearity Layer` – Introducing non-linearity to the system

  -   `Pooling (Downsampling) Layer` – Reduces the number of weights and controls overfitting

  -   `Flattening Layer` – Prepares data for Classical Neural Network

  -  `Fully-Connected Layer` – Standard Neural Network used for classification

    - add `convolutional layers first` => why Conv2D class is used => then add `MaxPolling` + `Flatten` layers

- + add a couple of `Dense layers` to create feed-forward neural network in the end

- endgame: `compile` the neural network => `connect all layers` put into Sequential class => neural network is now `ready for training` => `load MNIST data set` and `normalize` the data


- accuracy of 99.04% => 99% of the cases, neural network will be able to detect digit written in the image

- check that by running single predictions

- save model in a file:

 ` model.save('model.h5') ` => convert this file into .json file => doesn't work

    - convert the model from .h5 and for this we needed to install `TensorFlow.js` as a Python module => use tensorflow_converter tool to make model that is usable inside of Angular application

   - from `directory where model.h5 is located`:
<!-- outdated.....
      ` tensorflowjs_converter --input_format keras ./model.h5  ./trained_model `

       - will see several files in the `newly created trained_model folder`

          - from `trained_model directory`: -->

          ` http-server -p 3000 --cors `



## Angular Application

- In the folder where Angular application is created:

  ` nvm use 12 `

  `  npm install -g @tensorflow/tfjs `

  ` npm install `

  ` ng serve `
