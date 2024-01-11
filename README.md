
# Handwritten Digit Recognition using CNN
This project aims at doing handwritten-digit recognition using the CNN on two different datasets.

#Datasets:
## EMNIST
The Extended MNIST or EMNIST dataset expands on the MNIST database commonly used as
a benchmark, adding handwritten letters as well as additional samples of handwritten digits. There are several “splits” of the data by various characteristics. We will be using the “EMNIST Letters” dataset, which contains values split into 27 classes, one unused (class 0) and one for
each letter in the English alphabet.
Note: Some classes in this dataset can be challenging to recognize because each class
contains images of both upper- and lower-case letters. For example, while ‘C’ and ‘c’ are very
similar in appearance, ‘A’ and ‘a’ are quite different.

## Binary AlphaDigits:
The Binary Alphadigits dataset contains another set of handwritten letters and digits, in a different image size, in bitmap format. The file binaryalphadigits.npz contains the letters from this dataset, in a format that can be
opened with the numpy.load() method. The data contains two arrays: 'images' and
'labels'. The values have been adjusted from the original Binary Alphadigits dataset in order
to match the EMNIST Letters:
● The images of digits have been omitted.
● The labels are in the same format as EMNIST Letters, including the unused class 0.
However, the resolution of the images is different in this dataset: 20×16 rather than 28×28.

Once the baseline convolutional network for comparison, begin
experimenting with alternative architectures (e.g. adding additional filters to learn
features and additional hidden layers to learn combinations of features) and with
adjusting hyperparameters.

## Steps:
## Part 1-
1. Load the EMNIST Letters dataset, and use plt.imshow() to verify that the image data has been loaded correctly and that the corresponding labels are correct.
2. Apply the network architecture from Chollet’s MNIST notebook to the EMNIST Letters data.
3. Note the accuracy obtained by that code compared to the previous example from Chollet.
4. Apply the same architecture to the EMNIST Letters data.

## Part 2-
1. You should have found that while the EMNIST Letters are harder to learn than the MNIST digits, switching to a different network architecture led to a significant increase in model performance.
2. Now that you have a baseline convolutional network for comparison, begin experimenting with alternative architectures (e.g. adding additional filters to learn features and additional hidden layers to learn combinations of features) and with adjusting hyperparameters.
3. Hyperparameter tuning using the following techniques is performed on the baseline model.
Weight initialization
Choice of activation function
Choice of optimizer
Batch normalization
Data augmentation
Regularization
Dropout
Early Stopping
Pooling
4. When you are satisfied with your model's performance, save your model and evaluate the results on the test set.

## Part 3-
1. The process of transfer learning can be used to apply an existing model to a new dataset.
2. The images in the Binary Alphadigits dataset are a different size from those in EMNIST Letters. Use a function like tf.image.resize_with_pad(), PIL.ImageOps.pad(), or the PyTorch torchvision.transforms.Resize class to resize them into the right format for the network you trained in Part 2.
3. Compare the performance of the model you built in step (3) with the performance of a brand-new model trained only on the Binary AlphaDigits dataset.

## Results-
## Part 1 - Task 1
The model produced a training accuracy of .9886 and a loss of .0384 after the 5th epoch and a testing accuracy of .9802 with a loss of .0678.

## Part 1 - Task 2
Used plt.imshow() to verify that the image data has been loaded correctly and that the corresponding labels are correct.

## Part 1 - Task 3
Using the model's dense (fully connected) architecture on our emnist training's data set and only changing the input layer to accept 784 pixels and the output layer to have 27 nodes, the accuracy received after the 5th epoch while training was .9238 while the loss received was .2323. This accuracy was lower as compared to the mnist training data set, and respectively, the loss was higher.

During evaluating with the test data set, this model produced an accuracy of .9016 and a loss of .3233. As compared to the mnist evaluation on the test data set, this model's accuracy was lower and the loss was higher.


