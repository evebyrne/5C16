## Recurrent Neural Networks

Sequential data - audio, stock market, vehicle trajectory, NLP, machine translation

Remembers

H - Context/Hidden Layer - Dense layer w tanh as activation fxn - simple RNN arch - Elman network

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
