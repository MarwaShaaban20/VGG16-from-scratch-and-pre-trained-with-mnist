## VGG16 for MNIST Classification

This repository contains a TensorFlow implementation of the VGG16 architecture applied to the MNIST dataset. The code defines the VGG16 model, preprocesses the MNIST data, trains the model, and evaluates its performance using confusion matrix, precision, recall, and F1 score.

### Overview

The VGG16 architecture is a convolutional neural network model originally developed for image recognition tasks. In this implementation, the model is adapted for the MNIST dataset, which consists of 28x28 grayscale images of handwritten digits.



### Model Architecture

The VGG16 model is defined as follows:
- **Block 1**: 2 Convolutional layers (64 filters, 3x3 kernel), followed by MaxPooling
- **Block 2**: 2 Convolutional layers (128 filters, 3x3 kernel), followed by MaxPooling
- **Block 3**: 3 Convolutional layers (256 filters, 3x3 kernel), followed by MaxPooling
- **Block 4**: 3 Convolutional layers (512 filters, 3x3 kernel), followed by MaxPooling
- **Block 5**: 3 Convolutional layers (512 filters, 3x3 kernel)
- **Fully Connected Layers**: Flatten, 2 Dense layers (4096 units), and an output layer (10 units for 10 classes)

### Data Preprocessing

The MNIST dataset is loaded and preprocessed as follows:
- Normalize pixel values to be between 0 and 1
- Convert labels to categorical format

### Model Training

The model is compiled and trained using the following configuration:
- **Loss Function**: Categorical Crossentropy
- **Optimizer**: Adam
- **Metrics**: Accuracy
- **Epochs**: 2
- **Batch Size**: 200

### Model Evaluation

The trained model is evaluated on the MNIST test set. The following metrics are computed:
- **Confusion Matrix**
- **Precision** (weighted)
- **Recall** (weighted)
- **F1 Score** (weighted)



### Results

The results, including the confusion matrix, precision, recall, and F1 score, are printed to the console after the model evaluation.

