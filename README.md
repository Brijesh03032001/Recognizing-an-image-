# Recognizing an image
Humans take no effort to distinguish a dog, cat, or flying saucer. But this process is quite difficult for a computer to emulate: 
it only looks easy because God designs our brains incredibly well to recognize images. One common example of image recognition 
with machine learning is optical character recognition. In this project , I am building an Image Recognition model with Machine Learning using PyTorch.

For the image recognition task,  the TorchVision package is used which contains some of the best performing neural network architectures for computer vision, such as AlexNet.
It also provides easy access to datasets like ImageNet and other utilities to learn about computer vision applications in PyTorch.

The predefined models can be found in torchvision.models:

>from torchvision import models<br>
>dir(models)<br>

### AlexNet
To run the AlexNet architecture on an input image, we can create an instance of the AlexNet class. Here’s how to do it:

>alexnet = models.AlexNet()

At this stage, alexnet is an object that runs the AlexNet architecture. It is not essential for us to understand the details of this architecture at this time. 
At the moment, AlexNet is just an opaque object that can be called as a function.

By providing alexnet with precisely sized input data, we will perform a direct transfer across the network. 
In other words, the input will go through the first set of neurons, the outputs of which will be transmitted to the next set of neurons, until the final output.

### ResNet
By using the resnet101 method, we can now instantiate a 101-layer convolutional neural network.

>resnet = models.resnet101(pretrained=True) <br>
>resnet

### Image Recognition
Now we can use an image for the image recognition task using our model. 
I took a picture of a dog and a cat too . We can start by loading an image from the local filesystem using Pillow, an image manipulation module for Python:

>from google.colab import files<br>
>uploaded = files.upload()<br>
>from PIL import Image<br>
>img = Image.open("dog.png")<br>
>img

![dog](https://user-images.githubusercontent.com/66316376/130175502-093fcdbf-b51d-420a-9cf2-ab3de0d9f234.png)


## Run The Image Recognition Model

By running the Image Recognition Model ,we get the following result:-<br>
> **"golden retriever", 96.29334259033203**
