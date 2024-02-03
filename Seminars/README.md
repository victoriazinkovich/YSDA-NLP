Here will briefly write about the seminars and the most important things I learned in them.

---

## 1. Word Embeddings

- **Principial Component Analysis** (PCA) $-$ the simplest linear dimensionality reduction method.

<br>

- **t-distributed Stochastic Neighbor Embedding** (t-SNE) $-$ popular method for exploring high-dimensional data, ability to create compelling two-dimensonal “maps” from data with hundreds or even thousands of dimensions.

<br>

<br>

## 2. Text Classification

- **Generative** vs **Discriminative** $-$ in generative we learn the joint distribution of data (we can then generate this data independently), discriminative - we are only interested in the separating boundary between classes 

<br>

- **Laplace (add-one) smoothing** $-$ adding a small amount to the numerator and denominator of a fraction to yield a non-zero probability of encountering the word in the document 

<br>

*Classical Classification methods:*

1. **Naive Bayes classifier** $-$ generative model, which assumes that all words are in a certain "bag" and their order is not important to us; not a very accurate model, but it is easy to control what and where went wrong

<br>

2. **Logistic Regression** $-$ there is some set of attributes, by which we define the object, and we introduce weights for each attribute; as a probability we take the softmax of the scalar product $w^{(k)}f$

<br>

3. **Support Vector Machine** (SVM) $-$ also match features for an object (sentence), then apply SVM for classification (uses bag of words + biagrams)

<br>

*Neural Classification methods:*

Instead of hand selection, the features vector is selected by a neural network.

1.





































