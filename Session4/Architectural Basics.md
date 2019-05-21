#### Image Normalization
I think image normalization is to normalize the pixel values as image values varies from 0 to 255 and when higher integer values comes it might slow down the process and so we will normalize all the pixels to default range

#### How many layers
By seeing the input dataset we will get to know what is the input size of the image so that we can get to know how many layers should be used to get the required receptive field to see the size of the object

#### 3x3 Convolutions
Once we get to know the input size we can think how to build the architecture and since we use 3*3 kernals to convolute i choose this step as next one

#### Receptive Field
while convoluting each layer what the kernal is able to see is the receptive field at that layer so we will get to know the receptive field at each layer

#### Kernels and how do we decide the number of kernels?
kernals is basically used to feature extraction and number of kernals will be based on the dataset given, we can use smaller kernals if we can extract features in few convolutions

#### 1x1 Convolutions
1*1 kernals are used to reduced the number of channels and this is the ideal way to reduce the channels

#### MaxPooling
Maxpooling layer is used to reduce the number of layers to convolute and also reduce the parameters and using this we can get most shouting pixel

#### Position of MaxPooling
We cannot use maxpooling right after the first layer since the model should be able to recognize all the edges and patterns so we should convolute atleast 3 or more layers first and can use max pooling and also we cannot use at the end layer where next step would be output, we should stop using maxpooling before 2 convolution layers

#### The distance of MaxPooling from Prediction
we should stop using maxpooling before 2 convolution layers and should not use near to prediction because we will lose the spatial information

#### Batch Normalization
It will normalize the pixel values and get them into range of -1 to +1, so by doing this we can achieve all the pixels are given equal weightage

#### The distance of Batch Normalization from Prediction
BatchNormalization shouldn't be at the final layer since it reduces the values to range -1 to 1 and we will be having values 0 to 1 near the prediction

#### Concept of Transition Layers
Transition layer consists of one 1*1 and maxpooling, by using the transition block we will reduce the number channels and also the resolution of the image

#### Position of Transition Layer
Transistion block can be used when we are having architecture with high number of channels and if needed to reduce the channels and resolution

#### DropOut
Dropout layer is used to reduce the overfitting, Dropout actually disable the kernels for working 

#### When do we introduce DropOut, or when do we know we have some overfitting
Dropout can be used in each convolution layer and we will get to know it is overfitting if we check the training and validation accuracy. If training accuracy keeps on increasing and validation accuracy comes to ideal state then there will be overfitting

#### When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered)
when we can see the whole information in the earlier receptive field then we can stop convoluting further and we can stop since we are able to see whole image at that receptive field

#### SoftMax
Softmax is used while prediction since we have multiple classification

#### Adam vs SGD
Adam and SGD are the learning rates where we can achieve the global minima when we execute the complex function. In SGD we usually end up achieving the local minima and adam we can achieve the global minima

#### When to add validation checks
Validation checks will be done in every epoch to check the validation data performace in every epoch

#### Batch Size, and effects of batch size
Batch size : if we give batch size as 32 it will take 32 images and do 32 images forward propogation and one backward propagation
If we increase the batch size we are increasing the number of inputs for each epoch so that model can learn more accurate

#### Number of Epochs and when to increase them
If we see there is sequential improvement in the validation accuracy and you end up due to less epoch then we can increase the epochs so that we can achieve the better accuracy

#### Learning Rate
one of the optimizer technique to achive the global minimum. it will used with the adam or SGD

#### LR schedule and concept behind it
it will schedule the learning rate values for the designed epochs and we will do it because in each epoch it will schedule the LR and optimize accordingly

#### How do we know our network is not going well, comparatively, very early
When we find the validation accuracy is very less compared to training accuracy we can say our model is not performing well 
Also if we get very least accuracy in the early epochs then also we can say model is performing bad






