## Convolutional NN

Take advantage of spatial structure of an image - pixels close  together are related to eachother

Not fully connected -> every unit in one layer is **not** connected to every unit in the previous layer

For images a fully connected layer would require alot of computations as alot of pixels

In input layer -> num units = num pixels = width* height* num channels

Kernel = weight mask

Padding
  * same = values outside image domain extrapolated to 0
  * valid = no padding -> cropped
  
Example of convolution in written notes

**Filters** reduce num **weights**  

**Stride and pooling** reduce num **units**

Stride  = Distance that seperates each processed pixel 
  * =1 => all pixels processed 
  * =2 => every second pixel vertically and horizontally is processed
  
Pooling - Subsampling - max, average, stochastic
### Dates 
* Le-Net-5 - 1998 - MNIST
* AlexNet - 2012
* VGGNet - 2013/14

### Visualisation

Find image that maximises response from a filter, this image will show what that filter is recognising 

Process: 
  1. loss fxn = mean value of activation for that filter
  2. use back prop to get gradient of loss fxn wrt input image
  3. update the image to maximise the loss fxn (activation)
