---
title: "Feature Scaling (Normalisation and Standardisation) / Python implementation"
summary: "following the previous article about handle cyclical features, feature scaling is also important when we are going to use a machine learning algorithms. Is a method to scale the features in a comparative form. But, how can we scaling it ? what is the difference between normalizat"
date: 2023-08-29
authors:
  - me
tags:
  - "Machine Learning"
---

following the previous article about [handle cyclical features](/blog/handling-cyclical-features-for-use-in-method-such-us-machine-learning/), feature scaling is also important when we are going to use a machine learning algorithms. Is a method to scale the features in a comparative form. But, how can we scaling it ? what is the difference between normalization and standardization ? and when we can use it ? All this questions is gone solve at the current article/blog post. 

**Equations**

      

![ \begin{center}     Normalization(Min-Max Transform):     \[ X' = \frac{X - X_{\text{min}}}{X_{\text{max}} - X_{\text{min}}} \]     Standardization (Z-Score Transform):     \[ X' = \frac{X - \mu}{\sigma} \] \end{center} ](https://savvaspanagi.com/wp-content/ql-cache/quicklatex.com-379cf12134d3869d1cbcb49c1e3e6c99_l3.png)

Base on the very helpful Udemy courses that i have take (Machine learning A-Z) i will try to provide what’s the problem if we are not scaling the features and how scaling can help be giving a simple example. Let’s imagine that we have 2 columns of **income** and **age**, also we have 3 different persons as the following table:

PersonIncomeAge (Years)170.000€45260.000€44352.000€40

So which 2 of this 3 persons is more similar together?  We are clearly sure that the person 1-3 is the worst similar couple that we can take so ignore this pattern. If we try to calculate the difference between the remain combinations, person 1 from 2 has salary difference of 10.000€ and age different of 1 year, but person 2 from 3 has salary different of 8.000€ and age different of 4 years. So numerically the best pair is the person 2-3 which has less totally “distance” (8004<10001). Is this true? No, because is not acceptable to compare income with age. If we want to compare different units of measurement like income with age we have to change the units to a common comparable form. 

What is the different of each transform (Normalisation and Standardisation) ? 

Normalization, transform the data’s is a scale of [0-1], in contrast the standardisation is not predetermined scale from before and as larger is the standard deviation (σ) as closest to the zero was the standardisation data’s. 

When we use each transform ? 

Normalisation is recommended when the features follows normal distribution, in contrast the standardisation can be used in the most of situations without any problem. But this universal usage of standardisation does not mean that is always the best choice to scaling the features.

Going back to the problem we have described and try to normalisation the values ,we will have the following table:

PersonIncomeAge 11120.4440.8300

What about the most common pair now? 

Person [1-2] = (1-0.444)+(1-0.8) = 0.756

Person [2-3] = (0.444-0)+(0.8-0) = 1.244

So is obvious that the most similar couple is the person 1 with person 2 and not the above results he had calculated before normalization.

To implement this 2 methodologies with python, i will propose to use sklearn.preprocessing library. 

**Standardisation:**

```

import numpy as np
from sklearn.preprocessing import StandardScaler

# Create a sample dataset with two features (columns)
data = np.array([[10, 2],
                 [20, 4],
                 [30, 6],
                 [40, 8]])

# Create a StandardScaler object
scaler = StandardScaler()

# Fit the scaler to the data and transform the data
normalized_data = scaler.fit_transform(data)

print("Original Data:\n", data)
print("\nNormalized Data:\n", normalized_data)

```

**Normalisation:**

```

import numpy as np
from sklearn.preprocessing import MinMaxScaler

# Create a sample dataset with two features (columns)
data = np.array([[10, 2],
                 [20, 4],
                 [30, 6],
                 [40, 8]])

# Create a MinMaxScaler object
scaler = MinMaxScaler()

# Fit the scaler to the data and transform the data
normalized_data = scaler.fit_transform(data)

print("Original Data:\n", data)
print("\nNormalized Data:\n", normalized_data)

```

Your thoughts and questions are important for me. Feel free to share your insights or inquire about anything in the comments section below. Let’s keep the conversation going!

