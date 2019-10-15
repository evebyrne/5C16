### Logistic Regression

* Classification - 0 or 1
* x<sup>T</sup>w = risk score / logit -> larger -> more certain y = 1
* assume logistic distribution
* probit regression -> assume normal distribution 
* logistic fxn/sigmoid = 1/(1+e<sup>-t</sup>)
* p(y=1|x) = likelihood that y = 1 = p(e<x<sup>T</sup>w) = h<sub>w</sub>(x) = 1/(1+e<sup>x<sup>T</sup>w</sup>)
* p(y=0|x) = 1 - p(y=1|x)
* estimating likelihood of 1 or 0 not value of the outcome
* Error fxn = Cross Entropy = sum(i) (-y<sub>i</sub>h<sub>w</sub>(x<sub>i</sub>) - (1-y<sub>i</sub>)ln(1-h<sub>w</sub>(x<sub>i</sub>))
* Cross Entropy is derived from negative log likelihood of the total likelihood

#### Gradient Descent
* w<sup>t+1</sup> = w<sup>t</sup> + l*dE/dw
* l = learning rate 
* Method: 
  1. set initial weight w<sup>0</sup>
  2. for t = 0,1,2, ... do until convergence
  3. Compute gradient 
  4. update weights
  
#### Multiclass classification
* One vs all - multiple binary classifiers for different classifiers ... but imbalanced data
* Multinomial Logistic Regression
  * Uses softmax -> outputs likelihood of each class
  * Maximum likelihood derivation to get similiar cross entropy error fxn
  * also uses gradient descent
