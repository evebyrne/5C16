a nn that is trained to attempt to copy its input to its output

'take an input and find the features that allow it to be reconstructed most effectively'

'compression'

'self-encoders'

input = x

output/reconstruction = r

encoder f maps x to h

decoder g maps h to r 

goal is x = r 

dimensions of h need to be less than x in order for it to learn useful features (undercomplete)

if dim h >= dim x then just copying the input (overcomplete) 

loss fxn penalises r for being dissimiliar to x eg. mse

# applications
* dimensionality reduction
* image compression 
* image denoising
* feature extraction
* image generation
* sequence to sequence prediction
* recommendation system

# code
1. flatten
2. encoded = dense layer with num neurons < flattened input layer
3. decoded = dense layer with num neurons = flattened input layer

# in images 
max pooling to reduce size (encoding)

up sampling to increase size (decoding)
