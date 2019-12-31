# Build CNN

- use Colab=> https:/colab.research.google.com => save in Google drive

    - can also use Jupyter Notebook IDE

- Intro to CNNS =>
https://rubikscode.net/2018/02/26/introduction-to-convolutional-neural-networks/


- process an image(s) through several layers:


  - `Convolutional Layer` – Used to detect features

      - `filter` => EX: detect edges => usually a multi-dimensional array of pixel values => 5x5x3 = height & width in pixels & depth

      - process of applying (EX) `3×3 filter filter` = `convolution`

      - move the filter through the image using `matrix multiplication` => detect features

  - `Non-Linearity Layer` – Introducing non-linearity to the system

  - `Pooling (Downsampling) Layer` – Reduces the number of weights and controls overfitting

  - `Flattening Layer` – Prepares data for Classical Neural Network

  - `Fully-Connected Layer` – Standard Neural Network used for classification
