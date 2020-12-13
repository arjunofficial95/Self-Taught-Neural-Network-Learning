1. Load Task2C_labeled.csv, Task2C_unlabeled.csv and Task2C_test.csv data sets and required libraries (e.g., H2O). Note that we are going to use Task2C_labeled.csv and Task2C_unlabeled.csv for training the autoencoder. We are going to use Task2C_labeled.csv for training the classifier. Finally, we evaluate the trained classifier on the test Task2C_test.csv.

2. Train an autoencoder with only one hidden layer and change the number of its neurons to: 20, 40, 60, 80, ..., 400.

3. For each model in Step 2, calculate and record the reconstruction error which is simply the average (over all data points while the model is fixed) of Euclidian distances between the input and output of the autoencoder.

4. Build the 3-layer NN or “h2o.deeplearning” function (make sure you set “ autoencoder = FALSE”) to build a classification model using all the original attributes from the training set and change the number of its neurons to: 20, 40, 60, 80, .., 400 like Step 2. For each model, calculate and record the test error.

5. Build augmented self-taught networks using the models learnt in Step 2. For each model:
  a. Add the output of the middle layer as extra features to the original feature set.
  b. Train a 3-layer NN using all features (original + extra). Then calculate and record the test error.
