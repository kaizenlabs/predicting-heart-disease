# Predicting Heart Disease w/ Machine Learning - Cleveland Clinic Data

[![Tensorflow](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT7b9ZDD7lMdkByT-f_RCAqSQYqnq_CpgD16IFrwfmUwWCmdt7H)](https://www.tensorflow.org/beta/guide/effective_tf2)

[![Colab](https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667)](https://colab.research.google.com/github/JohnAntonusMaximus/predicting-heart-disease/blob/master/Predicting_Heart_Disease_w_TensorFlow_2_0.ipynb)

## Background

Advances in artificial intelligence is allowing us to give better tooling to healthcare providers around the world, from predicting cancer, to analyzing human genome sequences. Using data from Cleveland Clinic, I wanted to try analyzing patient datasets on heart disease to see how machine learning could potentially help cardiologists.

Here we're trying to determine whether a patient has heart disease, and if they do, the severity of the disease using 4 different classes, with the most extreme being the rarest in the data set.

 This database contains 76 attributes, but all published experiments
 refer to using a subset of 14 of them.  In particular, the Cleveland
 database is the only one that has been used by ML researchers to 
 this date.  The "goal" field refers to the presence of heart disease
 in the patient.  It is integer valued from 0 (no presence) to 4.
 Experiments with the Cleveland database have concentrated on simply
 attempting to distinguish presence (values 1,2,3,4) from absence (value
 0).  

 The names and social security numbers of the patients were recently 
 removed from the database, replaced with dummy values.

The dataset in its entirety can be found here:
http://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/

						

## Approach

Using a Tensorflow 2.0, I constructed a neural network for categorical classificiation with an Adam optimizer. The data had a number of null values and data types that needed to be changed, also the distribution of the data had large relative min/maxes, so I normalized some of the columns in the data using a lambda function.

## Results

The results were subpar for categorical classification, mostly attributed to only have 14 features and a small dataset (~300 paitents with complete metrics). When I changed the model to a binary classification problem, the results improved. 

In other words, when I changed the problem from "Does the patient have heart disease and what kind?" to just "Does the patient have heart disease?", accuracy improved to around 77%, which is still subpar for a diagnostic tool. 

Would need more patient data and additional features to finely tune this to state-of-the-art.


# Links

* [KaizenTek](http://www.kaizentek.io) - IT Consulting & Cloud Professional Services