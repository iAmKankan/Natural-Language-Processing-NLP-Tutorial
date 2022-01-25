## Index
![deep](https://user-images.githubusercontent.com/12748752/150695343-8977b5d0-3cd4-4959-b90e-9fe72d336d42.png)
![light](https://user-images.githubusercontent.com/12748752/150695340-c086876c-1e29-4493-b03b-cbff51dba02a.png)

## Word Embeddings
![deep](https://user-images.githubusercontent.com/12748752/150695343-8977b5d0-3cd4-4959-b90e-9fe72d336d42.png)
* **Word Embeddings or Word vectorization is a methodology in NLP to map _words_ or _phrases from vocabulary_ to a corresponding vector of real numbers which used to find word predictions, word similarities/semantics.**

### What is Word Embedding?
* Word embedding is just a fancy name for a [_`feature vector`_](https://ds055uzetaobb.cloudfront.net/brioche/uploads/JERsKXkW4T-screen-shot-2016-05-05-at-123118-pm.png) that represents a word.
* We can take a categorical object (a word in this case) and then map this object to a list of numbers in other words a vector we say we have embedded this word into a vector space. 
* So that's why we call them word embeddings.

### Word Embedding properties
* The operation (text to number) or vectorization is done either on **"word"** or on "**character**" level.
* The process of converting words into numbers are called **Vectorization**.
* This is one of the most important advances in Deep NLP research.
* Word Emeddings allow you to map words into a vector space.
* **Once you can represent something as a vector, you can perform arithmetic on it.** So, this is where the famous **_king - man = queen - woman_**, **_December - Novemeber = July - June_** or **_France - Paris = England - London_** come from.

### Word Embedding Mathematically Representation
* **Embedding mathematically represents a mapping , <a>f: X &rarr; Y,</a> which is a function**. 
* Where the function is -
    * **injective** (which is what we call an **injective function** , each Y has a unique X correspondence, and vice versa)
    * **structure-preserving** ( structure preservation , for example, X1 < X2 in the space to which X belongs, then the same applies to Y1 <Y2 in the space to which Y belongs after mapping).

* _**So for word embedding, the word word is mapped to another space, where this mapping has the characteristics of injective and structure-preserving.**_


### Word Embedding types
* The neural network cannot train the original text data. 
* We need to process the text data into numerical tensors first. 
* This process is also called **_text vectorization_**.
* There are several strategies for text vectorization:
   1. _**Split text into words**_, each word is converted into a vector
   2. _**Split text into characters**_, each character is converted into a vector
   3. Extract _**n-gram**_ of words or characters n-gram to a vector
* There are two main methods for word vectorization:
   1. One-hot Encoding
   2. Word Embedding
* There are two most popular algorithms for finding Word Embeddings-
    - **Word2vac**
    - **GloVe**

### 1. One-hot Encoding 
* Why is it called one-hot? 
   * After each word is one-hot encoded, only one position has an element of 1 and the other positions are all 0.
* **Example:**  **_"the boy is crying"_** (assuming there are only four English words in the world), after one-hot encoding,
   * **_the_** corresponds to (1, 0, 0, 0)
   * **_boy_** corresponds to (0, 1, 0, 0）
   * **_is_** corresponds to (0, 0, 1, 0)
   * **_crying_** corresponds to (0, 0, 0, 1)
* Each word corresponds to a position in the vector, and this position represents the word.

#### Avoid using One-hot Encoding 
* This way requires a very high dimension, because if all vocabularies have **100,000** words, then each word needs to be represented by a vector of length **100,000**.
   * **_the_** corresponds to (1, 0, 0, 0, ..., 0) (length is **100,000**)
   * And so on, to get high-dimensional sparse tensors.

#### Why One-Hot Vectors are bad?
* A main reason is that one-hot word vectors cannot accurately express the similarity between different words, such as the [_cosine similarity_](https://github.com/iAmKankan/Mathematics/blob/main/linearAlgebra.md#cosine-similarity) that we often use. 
* Since the [_cosine similarity_](https://github.com/iAmKankan/Mathematics/blob/main/linearAlgebra.md#cosine-similarity) between one-hot vectors of any two different words is 0, one-hot vectors cannot encode similarities among words.

### 2. Word Embedding
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
