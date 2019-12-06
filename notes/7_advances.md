## Transfer Learning

Use model trained in one domain in another domain

Use pretrained weights to extract features

Then train the classification part on the new data.

Eg. 
Use cat model to generate same features on dogs. Then train it to classify those features for dogs....

### Fine Tuning

As well as retraining the final classification part also retrain some of the previous layers

Do this if enough data

### Freezing 
Don't update weights

if not enough data in target domain

### Normalisation

scale data according to training set statistics

Used before activation fxn

With some activation fxns the output is not constrained within a range

for domain adaptation - one dataset to another

#### Local Response Normalisation

Introduced in AlexNet w ReLu

Non trainable layer

Square normalises within a neighbourhood

want to detect high freqency features with a large response

normalise arounf local neighbourhood so becomes even more sensitive as compared to it's neighbours

#### Batch Normalisation

Normalisation of features across a mini batch

Appears to stabilise gradient and reduce overfitting, may not need dropout

Normalise activation of nodes by subtracting mean and dividing by std dev 

**training**

Mean and std dev are that of the mini batch

**evaluation**

averaged over entire training set

## General Adversarial Networks

Discriminatory model + Generative model

**Example** 

Generator generates fake faces

The generated fake faces and real faces are fed into the discriminator nw. This classifies the images as real or fake. The output of this is fed back to the generator so the generator knows if it was successful in fooling the discriminator. The generator uses this feedback to improve and create faces that look more real. Best outcome is when the discriminator cant discriminate between real and fake. Feedback is the classification of the discriminator. Loss is calculated from this. Back prop carried out based on this loss to update weightd of generator. 

Discrimintator **training**

Trained on real data to see if can correctly predict as real

Trained on fake data to see if can correctly predict as fake

Generator takes random noise as initial input

Discriminator is not useful after training

distribution of noise in initial input to generator is not important

## introduce parallel path to avoid vanishing gradients 
## Inception

a subnetwork

dimensionality reduction

to solve problem of computaional cost and overfitting

instead of stacking multiple kernels on top of eachother, do them in parallel (wider not deeper)

parallel paths to avoid vanishing gradients -> the deeper the more multiplications the more likely to vanish

1X1 convolutions reduce the number of multiplications needed (reduce depth - 3 channels to 1)

layer of 1x1 convolutions is called the bottleneck layer

most simple = 3 convolutions (3 different sizes of filter), 

### example multiplications
#### no 1x1 convolutions
input- 28x28x92

apply 32 5x5 filters

28x28x92x32x5x5 multiplications needed

#### w 1x1 conv
28x28x192 apply one 1x1 con = 28x28x1 (all depth -> one)

28x28x192 apply 16 = 28x28x16 (bottleneck layer)

multiplications = 28x28x192x1x1x16 

then 28x28x16x32x5x5

### GoogleNet 2014
parallel connections

9 inception blocks

22 layers

## ResNet 2015
parallel connections between deeper and shallower layers by adding the result of a previous layer to the result after **2** convolutions

152 layers

Only difference to normal convolution is the identity connection

input = x 

output = H(x)

usually trying to learn H(x)

in resnet trying to learn H(x)-x

Constantly reminding the network of the input

why adding? 
