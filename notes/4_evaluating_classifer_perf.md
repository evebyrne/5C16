## Evaluating Classifer Performance

P = TP+FN (Everythings that's actually Positive)

N = TN + FP (Everything that's actually Negative)

### Recall 
 TP/P 

'Out of everything that is postive, how many did you get right'

### Precision
 TP/(TP+FP)
 
'Out of everything that you classed as positive, how many were actually positive?'

### False Positive Rate

FP/N

'Out of everything that is not positive, how many did you classify incorrectly as positive?'

### Accuracy

everything right / everything

### F1 Score
2*(Pr*R)/(Pr+R)

**Need at least 2 metrics**

**ROC (Receiver Operating Characteristic Curve)**

### Multiclass Classifiers
#### Micro-averaging
Precision: micro TP / (micro TP + micro FP) 

micro TP = sum of TP of each class

#### Macro-averaging
Precision: Sum of precisions for each class / Num classes
