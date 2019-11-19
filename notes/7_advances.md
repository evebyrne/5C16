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
### Normalisation

Used before activation fxn

With some activation fxns the output is not constrained within a range

for domain adaptation - one dataset to another

#### Local Response Normalisation

Introduced in AlexNet w ReLu

Non trainable layer

Square normalises within a neighbourhood

#### Batch Normalisation

Normalisation of features across a mini batch

Appears to stabilise gradient and reduce overfitting

Normalise activation of nodes by subtracting mean and dividing by std dev 

Mean and std dev are that of the mini batch

## General Adversarial Networks

Discriminatory model + Generative model

Example 

Generator generates fake faces

The generated fake faces and real faces are fed into the discriminator nw. This classifies the images as real or fake. The output of this is fed back to the generator so the generator knows if it was successful in fooling the discriminator. The generator uses this feedback to improve and create faces that look more real. Best outcome is when the discriminator cant discriminate between real and fake. Feedback is the classification of the discriminator. Loss is calculated from this. Back prop carried out based on this loss. 

Discrimintator training

Trained on real data to see if can correctly predict as real

Trained on fake data to see if can correctly predict as fake


Genrator takes random noise as initial input

## Inception

dimensionality reduction

to solve problem of computaional cost and overfitting

instead of stacking multiple kernels on top of eachother, do them in parallel

1X1 convolutions reduce the number of multiplications needed

layer of 1x1 convolutions is called the bottleneck layer

### GoogleNet

9 inception blocks

## ResNet

Only difference to normal convolution is the identity connection

input = x 

output = H(x)

usually trying to learn H(x)

is resnet trying to learn H(x)-x

Constantly reminding the network of the input

why adding? 
