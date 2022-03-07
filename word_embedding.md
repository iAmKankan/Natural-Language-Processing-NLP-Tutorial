## Index
![deep](https://user-images.githubusercontent.com/12748752/150695343-8977b5d0-3cd4-4959-b90e-9fe72d336d42.png)
* [Word Embeddings or Word vectorization](#word-embeddings-or-word-vectorization)
* [What is Word Embedding?](#what-is-word-embedding)
* [Word Embedding properties](#word-embedding-properties)
* [Mathematically Representation](#mathematically-representation)
* [Word Vectorization or Word Embeddings types](#word-vectorization-or-word-embeddings-types)
   * [1. One-hot Encoding](#1-one-hot-encoding)
   * [2. Word Embedding](#2-word-embedding)
     * [Word2vec](#word2vec)
         * [1) The Skip-Gram Model](#1-the-skip-gram-model)
         * [2) The Continuous Bag of Words (CBOW) Model](#2-the-continuous-bag-of-words-cbow-model)
     * Glove

## Word Embeddings or Word vectorization
![deep](https://user-images.githubusercontent.com/12748752/150695343-8977b5d0-3cd4-4959-b90e-9fe72d336d42.png)
* **_Word Embeddings_ or _Word vectorization_ is a methodology in NLP to map _words_ or _phrases from vocabulary_ to a corresponding vector of real numbers which used to find word predictions, word similarities/semantics.**
<img src="https://user-images.githubusercontent.com/12748752/151629694-24298066-ce77-4eed-a32c-a7e8114aa18e.png" width=100% />

### What is Word Embedding?
* Word embedding is just a fancy name for a [_`feature vector`_](https://ds055uzetaobb.cloudfront.net/brioche/uploads/JERsKXkW4T-screen-shot-2016-05-05-at-123118-pm.png) that represents a word.
* We can take a categorical object (a word in this case) and then map this object to a list of numbers in other words a vector we say we have embedded this word into a vector space. 
* So that's why we call them word embeddings.

### Word Embedding properties
* The operation (text to number) or vectorization is done either on **"word"** or on "**character**" level.
* The process of converting words into numbers are called **Vectorization**.
* This is one of the most important advances in Deep NLP research.
* Word Emeddings allow you to map words into a vector space.
* **Once you can represent something as a vector, you can perform arithmetic on it.**
* So, this is where the famous phrases come from.
   * **_king - man = queen - woman_**, 
   * **_December - Novemeber = July - June_** or
   * **_France - Paris = England - London_** 

### Mathematically Representation
* **Embedding mathematically represents a mapping , <a>f: X &rarr; Y,</a> which is a function**. 
* Where the function is -
    * **injective** (which is what we call an **injective function** , each Y has a unique X correspondence, and vice versa)
    * **structure-preserving** ( structure preservation , for example, X1 < X2 in the space to which X belongs, then the same applies to Y1 <Y2 in the space to which Y belongs after mapping).

* _**So for word embedding, the word word is mapped to another space, where this mapping has the characteristics of injective and structure-preserving.**_


### Word Vectorization or Word Embeddings types
* The neural network cannot train the original text data. 
* We need to process the text data into numerical tensors first. 
* This process is also called **_text vectorization_**.
* There are several strategies for text vectorization:
   * _**Split text into words**_, each word is converted into a vector
   * _**Split text into characters**_, each character is converted into a vector
   * Extract _**n-gram**_ of words or characters n-gram to a vector
* There are two main methods for word vectorization:
   1. **_One-hot Encoding_**
   2. **_Word Embedding_**

## 1. _One-hot Encoding_ 
![light](https://user-images.githubusercontent.com/12748752/150695340-c086876c-1e29-4493-b03b-cbff51dba02a.png)
* Why is it called one-hot? 
   * After each word is one-hot encoded, only one position has an element of 1 and the other positions are all 0.
* **Example:**  **_"the boy is crying"_** (assuming there are only four English words in the world), after one-hot encoding,
   * **_the_** corresponds to (1, 0, 0, 0)
   * **_boy_** corresponds to (0, 1, 0, 0）
   * **_is_** corresponds to (0, 0, 1, 0)
   * **_crying_** corresponds to (0, 0, 0, 1)
* Each word corresponds to a position in the vector, and this position represents the word.

### Avoid using One-hot Encoding 
* This way requires a very high dimension, because if all vocabularies have **100,000** words, then each word needs to be represented by a vector of length **100,000**.
   * **_the_** corresponds to (1, 0, 0, 0, ..., 0) (length is **100,000**)
   * And so on, to get high-dimensional sparse tensors.

### Why One-Hot Vectors are bad?
* A main reason is that one-hot word vectors cannot accurately express the similarity between different words, such as the [_cosine similarity_](https://github.com/iAmKankan/Mathematics/blob/main/linearAlgebra.md#cosine-similarity) that we often use. 
* Since the [_cosine similarity_](https://github.com/iAmKankan/Mathematics/blob/main/linearAlgebra.md#cosine-similarity) between one-hot vectors of any two different words is 0, one-hot vectors cannot encode similarities among words.

## 2. _Word Embedding_
![light](https://user-images.githubusercontent.com/12748752/150695340-c086876c-1e29-4493-b03b-cbff51dba02a.png)

> #### _The word2vec_ tool was proposed to address the issue with using _One-Hot Vector_.
* In contrast, _Word Embedding_ embeds words into a low-dimensional dense space.
* **Example:** the same **"the boy is crying"** sentence (assuming that there are only 4 English words in the world), after encoding, it may become:
    * **_the_** corresponds to **_(0.1)_**
    * **_boy_** corresponds to **_(0.14)_**
    * **_is_** corresponds to  **_(0)_**
    * **_crying_** corresponds to **_(0.82)_**
* We assume that the embedded space is 256 dimensions (generally 256, 512 or 1024 dimensions, the larger the vocabulary, the higher the corresponding spatial dimension)
* **Then the corresponding ( 0.1, 0.2, 0.4, 0 , ...) (vector length is 256) boy corresponds to (0.23, 0.14, 0, 0 , ...) is corresponding to (0, 0 , 0.41, 0.9, ...) , 0.82, 0, 0.14, ...)**
*  But in practice, the word **(boy) to word (man) should be very close** (because they are closely related), and **the word (cat) to word (stone) should be very far** (because they are basically unrelated).
* Embedding space has low dimensions and allows space to have structure .
* For example, the distance between the vectors can reflect gender, age, etc. (this requires training, and the unembedding layer has no structure), for example:
   * **man-woman = boy-girl**
   * **man-daddy = woman-mother**
* There are two most popular algorithms for finding Word Embeddings-
    1) **_Word2vac_**
    2) **_GloVe_**

## _Word2vec_
* _**Word2Vec is a shallow, two-layer Neural Networks which is trained to reconstruct linguistic contexts of words.**_
* It takes a large corpus of **_words_ as its input**  and produces a vector space, typically of **several hundred dimensions**, with each unique word in the corpus being assigned a corresponding vector in the space.
* Word vectors are positioned in the vector space such that words that share common contexts in the corpus are located in close proximity to one another in the space.
* Word2Vec is a particularly **computationally-efficient predictive model** for learning word embeddings from raw text.
* It comes in two flavors, the Continuous Bag-of-Words (CBOW) model and the Skip-Gram model.
* Algorithmically, these models are similar.

> ### _We Don't train our own Word2vec model. always use pretrained one_
> Coz the bias terms we dont know.
> Its very difficult to odentify the right hyperparameters.
> Its 
* Learning Rate is very important
* The word2vec tool contains two models, namely-
   1) _**Skip-gram**_ [_`Mikolov et al`_]= We predict the context words from the target
   2) _**Continuous bag of words (CBOW)**_ [_`Mikolov et al`_]= We predict the target word from the context.
* For semantically meaningful representations, their training relies on conditional probabilities that can be viewed as predicting some words using some of their surrounding words in corpora. 
> #### _Word2vec is a Self-Supervised learning_
> Since supervision comes from the data without labels, both skip-gram and continuous bag of words are self-supervised models.

### _1) The Skip-Gram Model_
* **The skip-gram model assumes that a word can be used to generate its surrounding words in a text sequence.**
> #### Take the text sequence “the”, “man”, “loves”, “his”, “son” as an example. 
> * Let us choose “loves” as the center word and set the context window size to 2. 
> * Given the center word “loves”, the skip-gram model considers the conditional probability for generating the context words:
> * “the”, “man”, “his”, and “son”, which are no more than 2 words away from the center word:

>> <img src="https://latex.codecogs.com/svg.image?P(\textrm{''the''},&space;\textrm{''man''},&space;\textrm{''his''},&space;\textrm{''son''}&space;\mid&space;\textrm{''loves''})" title="P(\textrm{''the''}, \textrm{''man''}, \textrm{''his''}, \textrm{''son''} \mid \textrm{''loves''})" />

* Assume that the context words are independently generated given the center word (i.e., conditional independence). 
* In this case, the above conditional probability can be rewritten as

>> <img src="https://latex.codecogs.com/svg.image?\mathrm{P(\textrm{''the''}\mid\textrm{''loves''})\cdot&space;P(\textrm{''man''}\mid\textrm{''loves''})\cdot&space;P(\textrm{''his''}\mid\textrm{''loves''})\cdot&space;P(\textrm{''son''}\mid\textrm{''loves''}).}" title="\mathrm{P(\textrm{''the''}\mid\textrm{''loves''})\cdot P(\textrm{''man''}\mid\textrm{''loves''})\cdot P(\textrm{''his''}\mid\textrm{''loves''})\cdot P(\textrm{''son''}\mid\textrm{''loves''}).}" />


> ![skip-gram](https://user-images.githubusercontent.com/12748752/139602656-549ebe0a-e0b3-4083-84c0-fa415ac8246b.png)

### _2) The Continuous Bag of Words (CBOW) Model_

* CBOW model is similar to the skip-gram model.
*  The major difference from the skip-gram model is that the continuous bag of words model assumes that a center word is generated based on its surrounding context words in the text sequence.
*   For example, in the same text sequence “the”, “man”, “loves”, “his”, and “son”, with “loves” as the center word and the context window size being 2,
*   The continuous bag of words model considers the conditional probability of generating the center word “loves” based on the context words “the”, “man”, “his” and “son”-

> <img src="https://latex.codecogs.com/svg.image?P(''loves''|''the'',''man'',''his'',''son'')" title="P(''loves''|''the'',''man'',''his'',''son'')" />

<img src="https://user-images.githubusercontent.com/12748752/156842326-a1509f1c-8efd-4e58-8ab7-dd190231a16d.png" align="right" width=30%/>

![cbow](https://user-images.githubusercontent.com/12748752/140629052-8a09da15-4be3-47fa-ab58-b87221f7e414.png)

* The "Window size" or "The token of interest" is generally 4.
> ### Example 1:

* For a sentence -“the”, “man”, “loves”, “his”, and “son”.
* It will generate like this

&rArr; <img src="http://latex.codecogs.com/svg.latex?\begin{matrix}The,&space;&&space;&space;Man,&space;&space;&&space;&space;Loves,&space;&&space;His,&space;&&space;&space;Family&space;&space;\\\downarrow&&space;\downarrow&space;&&space;\downarrow&space;&&space;\downarrow&space;&&space;&space;\\W_{t-2}&W_{t-1}&W_{t&plus;1}&W_{t&plus;2}&\end{matrix}" title="http://latex.codecogs.com/svg.latex?\begin{matrix}The, & Man, & Loves, & His, & Family \\\downarrow& \downarrow & \downarrow & \downarrow & \\W_{t-2}&W_{t-1}&W_{t+1}&W_{t+2}&\end{matrix}" align="top" />

&rArr; <img src="http://latex.codecogs.com/svg.latex?W_1\rightarrow&space;Embedding&space;\rightarrow&space;[\&space;\]_{(k)}&space;\rightarrow&space;Flattening\&space;Op\rightarrow&space;Fully\&space;Connected\&space;&space;Layer\left&space;(Softmax&space;\to&space;\right&space;)&space;\begin{Bmatrix}&space;W_t\end{matrix}_{(Vocab\&space;size)}" title="http://latex.codecogs.com/svg.latex?W_1\rightarrow Embedding \rightarrow [\ \]_{(k)} \rightarrow Flattening\ Op\rightarrow Fully\ Connected\ Layer\left (Softmax \to \right ) \begin{Bmatrix} W_t\end{matrix}_{(Vocab\ size)}" align="center" />
  
<img src="http://latex.codecogs.com/svg.latex?\\W_1\rightarrow&space;Embedding&space;\rightarrow&space;[\&space;\]_{(k)}&space;\rightarrow&space;Flattening\&space;Op\rightarrow&space;Fully\&space;Connected\&space;Layer\left&space;(Softmax&space;\to&space;\right&space;)&space;\begin{Bmatrix}&space;W_t\end{matrix}_{(Vocab\&space;size)}\\{\color{Red}\underbrace{W_1\rightarrow&space;Embedding&space;\rightarrow&space;[\&space;\]_{(k)}}&space;&space;&space;}\\&space;\\{\color{Blue}&space;This\&space;section\&space;is\&space;Fixed&space;\&space;or&space;\&space;Pre-Computed&space;\&space;or&space;\&space;Weight&space;Frizer}&space;" title="http://latex.codecogs.com/svg.latex?\\W_1\rightarrow Embedding \rightarrow [\ \]_{(k)} \rightarrow Flattening\ Op\rightarrow Fully\ Connected\ Layer\left (Softmax \to \right ) \begin{Bmatrix} W_t\end{matrix}_{(Vocab\ size)}\\{\color{Red}\underbrace{W_1\rightarrow Embedding \rightarrow [\ \]_{(k)}} }\\ \\{\color{Blue} This\ section\ is\ Fixed \ or \ Pre-Computed \ or \ Weight Frizer} " />

#### Improving the accuracy
![light](https://user-images.githubusercontent.com/12748752/134754235-ae8efaf0-a27a-46f0-b439-b114cbb8cf3e.png)
* Choice of Model architecture (CBOW/Skipgram)
   * Large Corpus, higher dimensions, slower- skipgram
   * Small Corpus, Faster - CBOW
* Increasing the training dataset.
* Increasing the vector dimensions
* Increasing the windows size.
* **Smaller dataset** is < **_30 MB_**

#### How do they work internally?
![light](https://user-images.githubusercontent.com/12748752/134754235-ae8efaf0-a27a-46f0-b439-b114cbb8cf3e.png)
<img src="https://wiki.pathmind.com/images/wiki/word2vec_diagrams.png" width=60%/>
* We take _One-hot-Vector_ for each words from the sliding window at a time as a input to the neural network.
* For CBOW our predicted value would be 'Love' in this case campared with the actual word
* This is how we get the weight matrix
* In Skip-gram the target word is input the y would be the context words(just opposite of CBOW)

