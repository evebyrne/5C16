# Recurrent Neural Networks

Sequential data - audio, stock market, vehicle trajectory, NLP, machine translation

Remembers

H - Context/Hidden Layer - Dense layer w tanh as activation fxn - simple RNN arch - Elman network

hidden state updated at every timestep to signify change in knowledge of the nw about the past

Tanh bc can produce + or - values and bounds between -1 and 1 - avoids explosion of state values

U - updates H

W - updates X(input)


#### Equations

h<sub>t</sub> = tanh(W<sub>h</sub>x<sub>t</sub> + U<sub>h</sub>h<sub>t-1</sub> + b<sub>h</sub>)

y<sub>t</sub> = sigma<sub>y</sub>(W<sub>y</sub>h<sub>t</sub>+b<sub>y</sub>)

x = input vector

h = vector of hidden layer states

y = output vector

sigma<sub>y</sub> = activation fxn

W<sub>h</sub>, b<sub>h</sub> = parameter matrix for h

U<sub>h</sub> = matrix for feedback parameters for h?? 

W<sub>y</sub>, b<sub>y</sub> = parameter matrix for y

Wh, Wy, bh, by shared by all input vectors xt

## Back prop through time
unroll the network into a standard feed forward network

gradient depends on gradients of previous states at all previous timesteps

### truncated bptt

unrolled nw an b very big and can be hard to parrallelise

so split sequence into chunks and appy bptt on these parts

## problems
rnns can get very deep leading to vanishing gradients

rnns remember alot of irrelevant information

## alternatives to pure rnn

### LSTM 1997
to deal w exploding and vanishing gradient problem

can selectively remember and forget things

comprised of memory blocks called cells

two states being transferred to next cell/memory block - cell state, hidden state

manipulating these memory blocks done through gates: input, forget, output

**input gate** adds info to cell state

**forget gate** removes info from cell state via multiplication of a filter (filter it out)

removes info no longer required for understanding or info of lesss importance

**output gate** selects useful info from cell state

## Gated Recurrent Units 2014
simpler, faster than LSTM

similiar perf, better on simple, worse on complex problems

reset gate, update gate

# Encoding
representing data in a way the computer can understand
## Label encoding
give each category a number ie cats 0 dogs 1 hamster 2

prob: will give higher numbers higher weight

prob: average of cats and hamsters is dogs(0+2)/2 = 1 
## One hot encoding




