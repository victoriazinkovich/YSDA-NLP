Here will briefly write about the homeworks and the most important things I learned in them.

---

## 1. Word Embeddings

- **Procrusters problem** $-$ is about finding a linear transformation that establishes a correspondence between words in two languages

$$W^*= \arg\min_W \sum_{i=1}^n||Wx_i - y_i||_2$$

$$W^*= \arg\min_W ||WX - Y||_F$$

![embedding_mapping.png](https://github.com/yandexdataschool/nlp_course/raw/master/resources/embedding_mapping.png)

<br>

- It can be shown that a self-consistent linear mapping between semantic spaces should be orthogonal. 
We can restrict transform $W$ to be orthogonal. Then we will solve next problem:

$$W^*= \arg\min_W ||WX - Y||_F \text{, where: } W^TW = I$$

$$I - \text{identity matrix}$$

<br>

<br>

## 2. Text Classification

- **Naive Bayes Classifier** $-$ generative model (intrested in joint distribution), we rewrite the conditional class probability $P(y=k|x)$ using Bayes's rule and get $P(x|y=k)\cdot P(y=k)$; Naive Bayes is a *generative model*, it models the joint probability of data

- **Logistic Regression** (aka Maximum Entropy Classifier) $-$ discriminative model, we choose weights such that the data is more likely to appear (use gradient ascent)
  - In this approach, used the idea, that minimization of the cross-entropy loss is equivalent to maximizing the data log-likelihood

To Note:
- it is generally a good idea to split data into train/test **before** anything is done to them.


<br>

<br>

## 3. Language Modelling

1. **Neural Language Model** $-$ Just like for N-gram LMs, we want to estimate probability of text as a joint probability of tokens; instead of counting all possible statistics, we want to train a neural network with parameters $\theta$ that estimates the conditional probabilities

$$P(X) = \prod_t P(x_t \mid x_0, \dots, x_{t-1})$$

2. **RNN Language Models** $-$ such model processes one token at a time, left to right, and maintains a hidden state vector between them
