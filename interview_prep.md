# Computer Science Fundamentals

## Algorithm Analysis

| Big-O      | Name              | Evaluation |
|------------|-------------------|------------|
| O(1)       | Constant time     | Excellent  |
| O(log(n))  | Logarithmic time  | Good       |
| O(n)       | Linear time       | Fair       |
| O(nlog(n)) | Linearithmic time | Bad        |
| O(n^2)     | Quadratic time    | Horrible   |
| O(2^n)     | Exponential time  | Horrible   |
| O(n!)      | Factorial time    | Horrible   |

* Master theorem

## Sorting Algorithms

| Sorting Algorithm | Best Case | Average Case | Worst Case |
|-------------------|-----------|--------------|------------|
| Quicksort         | Ω(nlog(n))| Θ(nlog(n))   | O(n^2)     |
| Mergesort         | Ω(nlog(n))| Θ(nlog(n))   | O(nlog(n)) |
| Heapsort          | Ω(nlog(n))| Θ(nlog(n))   | O(nlog(n)) |
| Bubble Sort       | Ω(n)      | Θ(n^2)       | O(n^2)     |
| Insertion Sort    | Ω(n)      | Θ(n^2)       | O(n^2)     |
| Selection Sort    | Ω(n^2)    | Θ(n^2)       | O(n^2)     |
| Tree Sort         | Ω(nlog(n))| Θ(nlog(n))   | O(n^2)t    |
| Bucket Sort       | Ω(n+k)    | Θ(n+k)       | O(n^2)     |
| Radix Sort        | Ω(nk)     | Θ(nk)        | O(nk)      |
| Counting Sort     | Ω(n+k)    | Θ(n+k)       | O(n+k)     |

* Comparison sorts: compares list values
* Simple sorts (linearithmic bound)
  * Insertion sort: step through list, find minimal non-sorted value, place at beginning, shift all non-sorted values by one, repeat
  * Selection sort: step through list, find minimal non-sorted value, swap with first non-sorted value, repeat
* Efficient sorts (linearithmic bound)
  * Merge sort: compare adjacent elements, swap if unsorted, merge sorted 2-lists into sorted 4-lists, repeat
  * Heapsort: take heap, minimal value guaranteed to be root node, remove and re-arrange heap to get next largest, repeat
  * Quicksort: select pivot element, step through list, swap items such that left list is smaller than pivot value, right list greater, then recurse
* Bubble sort and variants (linearithmic bound)
  * Bubble sort: step through list, compare adjacent pairs, swap
* Distribution sorts (linear bound)
  * Counting sort
  * Radix sort: sort list by least significant digit, retain order of appearance for ties, repeat with next more significant digit
  * Bucket sort
  
## Data Structures

|                     | Average Case |           |           |           | Worst Case |           |           |           |
|---------------------|--------------|-----------|-----------|-----------|------------|-----------|-----------|-----------|
| Data Structure      | Access       | Search    | Insert    | Delete    | Access     | Search    | Insert    | Delete    |
|---------------------|--------------|-----------|-----------|-----------|------------|-----------|-----------|-----------|
| Array               | Θ(1)         | Θ(n)      | Θ(n)      | Θ(n)      | O(1)       | O(n)      | O(n)      | O(n)      |
| Stack               | Θ(n)         | Θ(n)      | Θ(1)      | Θ(1)      | O(n)       | O(n)      | O(1)      | O(1)      |
| Queue               | Θ(n)         | Θ(n)      | Θ(1)      | Θ(1)      | O(n)       | O(n)      | O(1)      | O(1)      |
| Singly-Linked List  | Θ(n)         | Θ(n)      | Θ(1)      | Θ(1)      | O(n)       | O(n)      | O(1)      | O(1)      |
| Doubly-Linked List  | Θ(n)         | Θ(n)      | Θ(1)      | Θ(1)      | O(n)       | O(n)      | O(1)      | O(1)      |
| Hash Table          | N/A          | Θ(n)      | Θ(n)      | Θ(n)      | N/A        | O(n)      | O(n)      | O(n)      |
| Binary Search Tree  | Θ(log(n))    | Θ(log(n)) | Θ(log(n)) | Θ(log(n)) | O(n)       | O(n)      | O(n)      | O(n)      |
| Red-Black Tree      | Θ(log(n))    | Θ(n)      | Θ(n)      | Θ(n)      | O(log(n))  | O(log(n)) | O(log(n)) | O(log(n)) |

* Linear data structures
  * Array: a number of elements in specific order, accessed using an integer index
  * Linked lists
    * Singly-Linked List
    * Doubly-Linked List
* Trees
  * Binary trees
    * Binary Search Tree
    * Red-black Tree
  * B-tree
  * Heap
    * Binary heap
    * Binomial heap

* Hash tables
* Binary search trees
* Red-Black Trees

## Sources
* [Big-O Cheat Sheet](http://bigocheatsheet.com/)

# Programming Skills

* Python

# Data Science Fundamentals (Probability and Statistics)

## Exploratory Data Analysis (EDA)

## Data Pre-Processing / Data Cleansing / Data Imputation

## Feature Engineering

# Machine Learning Fundamentals

> Machine learning algorithms are described as learning a target function (f) that best maps input variables (X) to an output variable (Y): Y = f(X)

## Supervised Learning
All data is labelled and the algorithms learn to predict the output from the input data.

* Linear Regression: rule of thumb - remove correlated and unrelated variables
* Logistic Regression: binary classification
* Linear Discriminant Analysis (LDA)
* Decision Trees / Classification and Regression Trees: each node represents a single input variable and a split point on that variable
* Naive Bayes: predict posterior probability of class C given inputs x (i.e. p(C|x)) as joint probability of class C and inputs x (i.e. p(C)p(x|C)) divided by prior probability of inputs x (i.e. p(x)) - called naive because strong independence assumption between input features, also denominator ignored because x is fixed, MAP decision rule often used
* K-Nearest Neighbours (KNN): classify unseen point as mode (for classification) or mean (for regression) of K nearest neighbours - prone to imbalanced feature scales, breakdown of distance concept in high dimensions
* Support Vector Machines (SVM): fits a hyperplane to best separate points in input feature space by class by minimizing margin (distance between hyperplane and closest points)
* Bootstrap Aggregation / Bagging: an ensemble ML algorithm that trains multiple statistical models (us. decision trees) on different training sets, then averages predictions at test time - used to decrease variance of high-variance (overfitted) algorithms
  * Random Forest: an ensemble ML algorithm that trains multiple decision trees, but with suboptimal splits, then averages predictions at test time
* Boosting: ensemble technique that trains a weak classifier on training data, then a second classifier to correct first classifier's errors, and so on
  * AdaBoost / Adaptive Boosting: boosting on decision trees for binary classification, train weak tree on training data, weight current stage prediction, add all previous weak learners, calculate error, then re-assign training error weight for each sample equal to the previous error at that point - emphasizes correcting mistakes, so needs outliers removed

## Unsupervised Learning
All data is unlabelled and the algorithms learn the inherent structure from the input data.

* Clustering
* Anomaly Detection
  * Local Outlier Factor (LOF)
* Neural Networks
  * Autoencoders
  * Deep Belief Nets
  * Hebbian Learning
  * Generative Adversarial Networks
  * Self-Organizing Map (SOM)
* Association
  * Apriori algorithm for Association Rule Learning

## Semi-Supervsed Learning
Some data is labelled but most of it is unlabelled and the algorithms either learn to predict the output or the inherent structure from the input data.

## Weakly Supervised Learning
* Definition 1: all data is labelled with related outputs and the algorithms learn to predict the desired output from the input data.
* Defintiion 2
  * Incomplete supervision: subset of training data is labelled
  * Inexact supervision (identical to Definition 1): training data labelled with coarse-grained labels
  * Inaccurate supervision: given labels are not always ground truth
  
## Data transformations

## Evaluation and performance metrics