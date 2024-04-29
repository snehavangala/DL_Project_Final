# DL_Project_Final 

## FACE DETECTION AND RECOGNITION USING SIAMESE NETWORK WITH RESNET-50, RESNET-18 AND VGG16

This Main objective of this Project is to implement Face detection and recognization using Siamese network and VGG16 architecture  using the deep learning techniques to enhance accuracy and robustness. Heer we train the siamese network on a diverse dataset capturing various facial characteristics. Our architecture uncludes ResNet-18 and ResNet-50 as the base models for feature extraction, leveraging their residual blocks and Global Average Pooling layers. The siamese network will focus on learning facial similarity  through shared embeddings and a distance metric, enabling accurate detection of dissimilarity or similarity between faces. Additionally, We will add VGG16 for face recognition, Utilizing its powerful convolutional layers and fully connected head to classify faces into different categories based on their features.

## INSTALLATION

1.Clone the repository.

2.Install dependencies.

3.Configure the environment variables.

4.Run the project.

## USAGE

## FACE DETECTION 

At first we will install MTCNN as it is not readily available in Google Colab.Then, we start setting up the environment by installing the required packages , as the coding process is done in Google Colab so, we took the data from the google drive for the easier access and all our raw data is present in the drive. then we used a pre-trained haar cascade classifier for detecting the face in an image(shown in the execution output). Then we extracted the faces from all the images in our data set.Now we Will split the data into training, testing and validation datasets by creating folders for the same. Here, we are calculated mean and standard deviation for the normalisation purpose.Then we have defined a the class named siamesenetwork data set. It implements a pytorch data set for generating pairs of images along with their corresponding labels for network training.The the process of visualization process is done where Zeros are correct pairs and ones are incorrect pairs.As part of our first network architecture, we are using Resnet 18. Here we defined Resnet as its initial layer as part of transfer  learning, followed by the convolution layer and fully connected layers.constructive loss function ensures that similar pairs have small euclidean distance and dissimilar pairs  have large distances. It is the loss based on Euclidean distance.Now, this is where we start training our siamese network,wheer we can get the training and validation loss. Raytune is called for calculating best configurations.Then we check the availability of the GPU.

Here we are training the siamese network with the best configuration parameters Which helps to decrease training and validation losses.we are testing the siamese model to find the accuracy.Now, we are Going to use mini siamese network on a smaller data set and we will see testing and training results.

Now come resnet 50 Architecture where we will perform all the steps as above abd will acquire the accuracy. then we will move on to smaller data set and will repeat the process to find test accuracy and training accuracy. 

Apart from Resnet we also have built a siamese network from scratch with its own convolution layers and fully connected layers. Now we are testing the siamese network With the test data set and will see dissimilarities scores for pairs, lower the dissimilarities score, similar the faces are and vice versa which was explained with an example.

We can also implement this using gradio, which is just an another interface to test our models. 

## FACE RECOGNITION

Coming to the which is face recognition. Here we implemented VGG 16 model architecture using Keras framework.The code runs the VGG 16 model pre-trained on image net and removes its top layers, then adds custom fully connected layers on top of base VGG16 model to adopt for the specific classification task here in this case faced recognition with four classes.As part of our image preprocessing, we are generated the training and validation data.Then we will start the model training. Which gives training validation accuracy.Then visualisation is done which gave us the fianal output.

## Contributing

We welcome contributions!

## Contact

"Kasulanati, Sreenivas" <skasu5@unh.newhaven.edu>; 
"Shaik, Adil" <ashai45@unh.newhaven.edu>;
"Vangala, Sneha" <svang16@unh.newhaven.edu>.
