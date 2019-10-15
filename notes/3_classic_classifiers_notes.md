## Classic Classifiers

### KNN
  * pros 
    * non-parametric (no assumption about distribution) (num parameters increases w training data)
    * high accuracy if large training set
  * cons
    * computationally expensive, scales badly
    * dont learn much about features
    
### Decision Trees
  * pros
    * fast
    * non parametric
  * cons
    * decisions on axis -> cant do diagonal splits 
   
### SVM
* same as logistic regression but different loss fxn
* Hinge loss = sum(i) [y=0]max(0, x<sup>T</sup>w) + [y=1]max(0, 1-x<sup>T</sup>w)
* Learns which examples contribute the most -> support vectors
  * pros
    * non-parametric
  * cons
    * high cost for large datasets
    
All non-parametric are likely to overfit if small training set

### No Free Lunch Theorem 
All perform equally well on average, which is best depends on the problem

### Kernel Trick ??? 

* Allows us to map features to a higher dimension without actually having to compute the features.... ??
* As the dimension increases the number of features increases a lot so infeasible to explicitly compute them 
* Something to do with dot products
* Kernel fxn = k(x,z) = dot product(x<sup>T</sup>) * dot product(z)
* Can define k without defining the dot products ??? How ??? 
* Kernel fxns already defined to use.. Don't need to find the kernel fxn
* Example - Radial Basis Fxn - k(u,v)= e<sup>-a||u-v||<sup>2</sup></sup>
* Used by kernel methods which are inefficient for large datasets
