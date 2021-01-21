# Handwritten-Digit-Recognisation
Using Deep Learning to recognize Handwritten Digits

# The MNIST dataset
This is probably one of the most popular datasets among machine learning and deep learning enthusiasts. The MNIST dataset contains 60,000 training images of handwritten digits from zero to nine and 10,000 images for testing. So, the MNIST dataset has 10 different classes. The handwritten digits images are represented as a 28×28 matrix where each cell contains grayscale pixel value.

# In the training file

    1. Import the libraries and load the dataset
       First, import all the modules that are needed for training our model. The Keras library already contains some datasets and MNIST is one of them. So we can easily import the dataset and start working with it. The mnist.load_data() method returns us the training data, its labels and also the testing data and its labels.
    2. Preprocess the data
       The image data cannot be fed directly into the model so we need to perform some operations and process the data to make it ready for our neural network. The dimension of the training data is (60000,28,28). The CNN model will require one more dimension so we reshape the matrix to shape (60000,28,28,1).
    3. Create the model
       A CNN model generally consists of convolutional and pooling layers. It works better for data that are represented as grid structures, this is the reason why CNN works well for image classification problems. The dropout layer is used to deactivate some of the neurons and while training, it reduces offer fitting of the model. Then the model is compiled the Adadelta optimizer.
    4. Train the model
       The model.fit() function of Keras will start the training of the model. It takes the training data, validation data, epochs, and batch size.
       It takes some time to train the model. After training, the weights and model definition is saved in the ‘mnist.h5’ file.
    5. Evaluate the model
       There are 10,000 images in the dataset which will be used to evaluate how good our model works. The testing data was not involved in the training of the data therefore, it is new data for our model. The MNIST dataset is well balanced so I got around 85% accuracy.         
    
