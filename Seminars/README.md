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

### *Classical Classification methods:*

1. **Naive Bayes classifier** $-$ generative model, which assumes that all words are in a certain "bag" and their order is not important to us; not a very accurate model, but it is easy to control what and where went wrong

<br>

2. **Logistic Regression** $-$ there is some set of attributes, by which we define the object, and we introduce weights for each attribute; as a probability we take the softmax of the scalar product $w^{(k)}f$

<br>

3. **Support Vector Machine** (SVM) $-$ also match features for an object (sentence), then apply SVM for classification (uses bag of words + biagrams)

<br>

### *Neural Classification methods:*

Instead of hand selection, the features vector is selected by a neural network.

1. *Weighted* Bag of Words (BOW) $-$ just summarize embeddings of words in the text and get feature vector

<br>

2. Convolutional Neural Network (CNN) $-$ like CNN's idea for pictures (find a cat no matter where it is);
    - **convolution** $-$ linear layer that takes only some window of vectors
    - **non-lineariry** (ReLU) $-$ 0 if no cat, 1 if cat (like threshold)
    - **pooling** $-$ averaging, if there is a cat at least somewhere 

<br>

3. Recurrent Neural Network (RNN) $-$ a more natural idea for texts, the RNN reads the text word for word;
    - **two RNN layers** can be done: remember everything that you read and read one more time
    - **disadvantage**: can forget the beginning of the phrase if it's long
    - **fix**: one RNN reads left-to-right, the second reads right-to-left and then result is concatenated  

<br>

### To Note:
- **Fine-tuning importance:** in Word2Vec, for example, antonyms will have very close embeddings ("black" and "white", "good" and "bad") because they often occur in similar contexts: this can be bad for the semantics task.
- **Data Augmentation:**
    - word dropout (replace word with UNK/random word/synonyoums)
    - paraphrasing (translate and translate back)















































