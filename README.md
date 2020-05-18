# semi supervised ae

A semi supervised convolutional autoencoder for MNIST handwritten digits classification.

This notebook gives a brief look at how a convolutional autoencoder can be used to make an image classification. 

## Autoencoders

An autoencoder is made of two principal components, the encoder and the decoder. The encoder is used as a feature extractor, it detects features from low level to high level as data goes from shallow to deeper layers. The extracted features are stored in a vector called latent vector. The decoder takes those features and converts them back to the original shape, in the case of image inputs it tries to reconstruct the original image.

![alt text](https://raw.githubusercontent.com/snatch59/keras-autoencoders/master/assets/autoencoder_latent_space.png)

## Semi supervised learning

Semi supervised learning falls between supervised and unsupervised learning. The training needs a large amount of labeled data and a small amount of unlabeled data. Autoencoders are unsupervised learning models, combining them with a classifier makes a semi supervised learning model. The classification takes the latent vector of the autoencoder as input and outputs the corresponding class. the main difference between a semi supervised model and a supervised classifier is that the later needs a lot more labeled data than the first, which may not be always possible like in cases where only few labeled samples are avalible.

## Results

classifier accuracy : 98.62%   , classifier loss : 0.06

decoder accuracy : 80.89% , decoder loss : 0.01
