# handwritten-digit-recognition-using-CNN
This project aims at doing handwritten-digit recognition using the CNN on two different datasets.

Datasets:

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
Part 1-
1. Load the EMNIST Letters dataset, and use plt.imshow() to verify that the image data has been loaded correctly and that the corresponding labels are correct.
2. Apply the network architecture from Chollet’s MNIST notebook to the EMNIST Letters data.
3. Note the accuracy obtained by that code compared to the previous example from Chollet.
4. Apply the same architecture to the EMNIST Letters data.


