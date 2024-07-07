---
title: Encode Text Data for ML
author: Bobae Bak
date: 2024-07-02
category: Jekyll
layout: post
---

Encoding in the context of data science and machine learning refers to the process of transforming data into a different format. This is often necessary to convert data into a format that machine learning models can understand and work with effectively. There are several types of encoding methods, each suited to different types of data and scenarios.

### Label Encoder
A label encoder is a tool used in ML and data preprocessing to convert categorical data into a numerical format that can be used by machine learning algorithms. Many algorithms require input features and labels to be numeric, so this conversion is necessary for training and prediction tasks.

```python
from sklearn.preprocessing import LabelEncoder

# Sample data
fruits = ["apple", "banana", "orange", "banana", "apple"]

# Initialize the encoder
encoder = LabelEncoder()

# Fit and transform the data
encoded_fruits = encoder.fit_transform(fruits)

print(encoded_fruits)  # Output: [0 1 2 1 0]
```

