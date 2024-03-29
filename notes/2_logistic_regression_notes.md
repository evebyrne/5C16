### Logistic Regression

* Classification - 0 or 1
* x<sup>T</sup>w = risk score / logit -> larger -> more certain y = 1
* assume logistic distribution
* probit regression -> assume normal distribution 
* logistic fxn/sigmoid = 1/(1+e<sup>-t</sup>)
* p(y=1|x) = likelihood that y = 1 = p(e<x<sup>T</sup>w) = h<sub>w</sub>(x) = 1/(1+e<sup>x<sup>T</sup>w</sup>)
* p(y=0|x) = 1 - p(y=1|x)
* estimating likelihood of 1 or 0 not value of the outcome
* Error fxn = Cross Entropy = sum(i) (-y<sub>i</sub>ln(h<sub>w</sub>(x<sub>i</sub>)) - (1-y<sub>i</sub>)ln(1-h<sub>w</sub>(x<sub>i</sub>))
* Cross Entropy is derived from negative log likelihood of the total likelihood

#### Gradient Descent
* w<sup>t+1</sup> = w<sup>t</sup> + l*(dE/dw)(w<sup>t</sup>)
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

![alt text](https://github.com/evebyrne/5C16/blob/master/notes/Screenshot_2019-12-05%20Screenshot%20from%202019-12-05%2014-44-26%20png%20(PNG%20Image%2C%201920%20%C3%97%201080%20pixels)%20-%20Scaled%20(99%25).png)

best classifier for this is logistic regression and the least likely to overfit
