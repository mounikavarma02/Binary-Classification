# BINARY CLASSIFICATION
## Aim:
To write a python program to perform binary classification.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner /Google Colab

## related Theory Concept:
Binary classification refers to predicting one of two classes and multi-class classification involves predicting one of more than two classes. Binary classification is the task of classifying the elements of a set into two groups on the basis of a classification rule.

## Algorithm
   1. Define dataset
   2. Summarize dataset shape
   3. Summarize observations by class label
   4. Summarize first few examples
   5. Plot the dataset and color the by class label


## Program:

Program to implement binary classification.

Developed by:mounika.s.c

RegisterNumber:  212219040084

```python3

from numpy import where
from collections import Counter
from sklearn.datasets import make_blobs
from matplotlib import pyplot

X,y = make_blobs(n_samples=10,centers=2,random_state=1)
print(X.shape,y.shape)
counter=Counter(y)
print(counter)

for i in range(5):
    print(X[i],y[i])
    
for label, _ in counter.items():
    row_ix=where(y==label)[0]
    pyplot.scatter(X[row_ix,0], X[row_ix,1], label=str(label))
pyplot.legend()
pyplot.show()
```



## Output:
![image](https://user-images.githubusercontent.com/78891098/168517278-61c504d0-191b-40ed-a5e1-2c4715bf6d51.png)


## Result:
Thus the python program performed binary classification successfully.
