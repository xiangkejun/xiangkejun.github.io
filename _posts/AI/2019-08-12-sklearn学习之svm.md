---
title: sk-learn学习之svm
date: 2019-03-3 10:30:23
tags:
- AI
categories:
- AI
---


svm是很强大的分类器，可以用于监督学习，半监督/无监督学习中，在工业界和学术界都有广泛的应用。

1. svm一个简单的二分类例子

[svm-classification](https://scikit-learn.org/stable/modules/svm.html#svm-classification
)


```
#二分类
from sklearn import svm
X = [[0, 0], [1, 1]] # [n_samples, n_features]
y = [0, 1]  #  class labels
clf = svm.SVC(gamma='scale')
clf.fit(X, y) 
print(clf.predict([[2., 2.]])) # 1

print(clf.predict([[-1., -1.]]))  # 0
```
