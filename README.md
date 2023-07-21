# Deep Ensemble Optimized Transformers 

Heart Rate Classification
This code provides a solution for classifying heart rate data using a transformer-based neural network model. It utilizes the TensorFlow and Keras libraries for deep learning.

Dataset
The code assumes that you have two CSV files: 'heart_rate.csv' and 'labels.csv', containing the heart rate data and corresponding labels, respectively. It reads the data using the Pandas library and splits it into training and testing sets.

Model Architecture
The model architecture is based on a transformer encoder, which consists of multiple transformer blocks. Each transformer block includes a multi-head self-attention layer, normalization, and a feed-forward network. The output of the transformer blocks is globally average pooled and then passed through a multi-layer perceptron (MLP) for classification.

The transformer_encoder function implements a single transformer block, while the build_model function creates the complete model based on the specified parameters. The model is compiled with the sparse categorical cross-entropy loss function, Adam optimizer, and metrics for evaluation.

Training
The code trains the model using the fit function, passing the training data (x_train and y_train) and validation split ratio. It also specifies the number of epochs, batch size, and early stopping callbacks to prevent overfitting.

Evaluation
After training, the model is evaluated using the evaluate function with the testing data (x_test and y_test). The evaluation provides the loss value and sparse categorical accuracy metric.

Please make sure to have the necessary dataset files in the correct format before running the code. Adjust the parameters and model architecture as needed for your specific use case.
