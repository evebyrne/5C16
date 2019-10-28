### Linear Regression

* p = num features
* n = num observations
* MSE is aggregation of error to minimise
* min error at dE/dw (gradient) = 0 
* y = Xw + e  
* X = Design Matrix
* y = w<sub>0</sub> + w<sub>1</sub>x<sub>1</sub> + w<sub>2</sub>x<sub>2</sub> + .. + w<sub>p</sub>x<sub>p</sub>
* w<sub>0</sub> = bias
* y = x<sup>T</sup>w
* for gradient derivations:
  * d(e<sup>f(x)</sup>)/dx = e<sup>f(x)</sup> * d(f(x))/dx
* Normal Equation:  
   **X<sup>T</sup>Xw = X<sup>T</sup>y**  
   w = X<sup>T</sup>y(X<sup>T</sup>X)<sup>-1</sup>
* Can use more complex models by using increasing powers of x
* Underfitting - can't get the error low enough
* Overfitting - low error on training, high on validation
  * Get more data
  * Regularisation
    * Tikhonov reg -> pulls weights towards 0 
* Maximum Likelihood
  * Assume gaussian distribution
  * find w that maximises p(y|X, w) (likelihood of y given X)
  * equivalent and easier to minimise negative log likelihood
    * w = argmin sum (xw-y)<sup>2</sup>

### Linear Algebra
Linear in calculus is not the same as linear in linear algebra...
linear fxn in linear alg - affine fxn
#### Matrix Multiplication

* (row x column)
* (m x n) * (n x q) = (m x q)
* n has to be equal 

#### Linearity
* Remember testing if linear in parameters so testing w 
* Two properties
  * Scalability (easier to calculate so do this first) => f(Lw) = Lf(w)
  * Additivity/Homogeneity => f(x<sub>1</sub> + x<sub>2</sub>) = f(x<sub>1</sub>) + f(x<sub>2</sub>)
  * Examples from test2:  
  y = w<sub>1</sub>logx<sub>1</sub> + w<sub>2</sub>cosx<sub>2</sub> Linear  
  y = w<sub>1</sub>x<sub>1</sub> Linear  
  y = w<sub>1</sub>x<sub>1</sub> + x<sub>2</sub>sin(w<sub>2</sub>) Non Linear  \
  y = w<sub>1</sub>w<sub>2</sub> + x<sub>1</sub> Non Linear
  
