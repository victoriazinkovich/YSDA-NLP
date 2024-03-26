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

- it is generally a good idea to split data into train/test **before** anything is done to them.

1. **Naive Bayes Classifier** $-$ we rewrite the conditional class probability $\(P(y=k|x)\)$ using Bayes's rule and get $\(P(x|y=k)\cdot P(y=k)\)$.




