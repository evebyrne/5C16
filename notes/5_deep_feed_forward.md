# deep networks
at least two hidden layers with non-linear activations

all networks studied can be a feed forward network

# success of dl fueled by: 
* big data
* powerful computing platforms

# deeper networks
* generalise better
* dont neccessarily have more units (can have one layer w loads if units)
* are harder to train

# activation fxns
* linear activation fxns do nothing
* ReLu, linear prevent vanishing gradients (not tanh or sigmoid)

# universal approximation theorem 
a single hidden layer neural network with a linear output unit can approximate any continuous function arbbitrarily well, given enough hidden units

the deeper layers learn more complex features

# gradient descent
## backprop 
uses chain rule to propogate the gradient info from the cost unit back to the weight units

## vanishing gradients
when at least one of the units produce a near zero derivative, when this happens the whole drivate will approach 0 and the gradient will get stuck

more likely for deeper networks

## mini batch gradient descent
usually have to calculating gradient for entire dataset, impractical

instead compute gradient over batches

small batch sizes means the computed gradient is 'noisier' and likely to change from batch to batch

can help escape from local minimums but can also lead to poor convergence

## epoch
the number of times all of the training vectors are used once to update the weights

after each epoch samples shuffled 

## decay
slow down learning rate over time

## momentum update
reuse previous gradients to influence the current gradient update

(if all going in same direction looks good - keep going faster)

## others 
adam, nadam


# stochastic gradient descent
mini batch with batch size =1 

gradient recomputed for each observation


# regularisation

works on assumption that smaller weights create a simpler model which will generalise better
## L2 
most common

Tikhonov reg of least squares 

adding a penalty to a loss fxn

E'(w) = E(w) + lambda(w<sub>i</sub>)<sup>2</sup>

lambda is the reglarisation parameter which determines how much to penalise the weights

# L1
E'(w) = E(w) + lambda|w<sub>i</sub>|

can end up setting weights to 0 and simplifying the network (good) 

feature selection bc sets weights of useless features to 0 

http://www.chioka.in/differences-between-l1-and-l2-as-loss-function-and-regularization/

# constraints
## max norm constraint
enforce upper bound on value of weights

prevents network from totally diverging in training

# dropout
randomly switch off units in training (ie set output to 0) 

a regularisation technique

a way of adding noise to the data

# getting more data
* dropout 
* add gaussian noise to original dataset

