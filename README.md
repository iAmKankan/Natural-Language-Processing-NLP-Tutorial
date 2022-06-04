## Index
![deep](https://user-images.githubusercontent.com/12748752/150695343-8977b5d0-3cd4-4959-b90e-9fe72d336d42.png)
* [Natural Language Processing (NLP)](#natural-language-processing-nlp)
* [Why learn NLP?](#why-learn-nlp)
* [Word Embeddings(Word2vec)](https://github.com/iAmKankan/Natural-Language-Processing-NLP-Tutorial/blob/master/word_embedding.md)
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
* [References](#references)
## Natural Language Processing (NLP)
![deep](https://user-images.githubusercontent.com/12748752/150695343-8977b5d0-3cd4-4959-b90e-9fe72d336d42.png)
* _**Natural language processing**_ is a subset of Artificial intelligence that helps computers to understand, interpret, and utilize the human languages. 
<img src="https://user-images.githubusercontent.com/12748752/150695497-d66d6dae-37e6-48d4-8144-a7b8473435c9.png" ALIGN="right" width=50% />

* NLP allows computers to communicate with peoples using human languages. 
* NLP also provides computers with the ability to read text, hear speech, and try to intrepret it. 
* NLP draws several disciplines, including Computational linguistics and computer science, as this attempts to fill the gap in between human and computer communication.
* NLP breaks down language into shorter, more basic pieces, called **_tokens_**(period, words, etc), and attempts to understand the relationships of tokens. 
* This approach often uses higher-level NLP features, such as:
  - **Sentiment analysis:** It identifies the general mood, or subjective opinions, which is stored in large amount of texts, It is more useful for opinion mining.
  - **Contextual Extraction:** Extract structured data from text-base sources.
  - **Text-to-Speech and Speech-to-text:** It transforms the voice into text and vice a versa.
  - **Document Summarization:** Automatically creates a synopsis, condensing large amounts of text.
  - **Machine Translation:** Translates the text or speech of one language into another language.

### Why learn NLP?
![light](https://user-images.githubusercontent.com/12748752/150695340-c086876c-1e29-4493-b03b-cbff51dba02a.png)
* We are in the age of information, we can't even imagine our life without *Google*. 
* We use basic stuffs with Alexa and Siri and we are habitual with these two.
* We use spam filters for filtering spam emails.
* We need spell checker on our Word documents. 
* There were many more examples of real world NLP applications around us.

Let me give you some example like they are built with the use of NLP but we are not aware of it:

   1. Spell Correction(MS Word/any other editor)
   2. Search engines(Google, Bing, Yahoo)
   3. Speech engines(like Siri, Google assistant)
   4. Spam classifiers(All e-mails services)
   5. News feeds(Google, Yahoo!, and so on)
   6. Machine Translation(Google translation)
   7. IBM Watson
<p>   
Building these above applications we need a required, very specific skill set with a great understanding of language and tools to process the language efficiently. So, it's not just hype that makes NLP one of the most niche areas, but it's the kind of application that can be created using NLP(Natural Language Processing) that makes it one of the most unique skills to have.</p><p>
To achieve one of the above applications and other basic NLP preprocessing, there are many open source tools available. Some of them which are made by organizations to build their own NLP applications, while some of the organizations have open-sourced. Here are the small list of NLP tools are available:
</p>

   - GATE
   - Mallet
   - Open NLP
   - UIMA
   - Standford toolkit
   - Gensim
   - **NLTK(Natural Language Tool kit)**
<p>   
Most of the tools are written in Java and have similar functionalities.And Some of them are robust and have a different variety of NLP tools are avaialable. However, when it comes to ease to use and explaination of the concepts, NLTK scores really high.</p><p>
NLTK tool is also a best learning kit because the learning curve of Python(NLTK is written on this) is very fast. NLTK incorporated most of the NLP tasks, it's too elegant and easy to work with. For all these kind of reasons, NLTK became one of the popular libraries in the NLP community.</p>

### Main Approaches of NLP
![light](https://user-images.githubusercontent.com/12748752/150695340-c086876c-1e29-4493-b03b-cbff51dba02a.png)

<img src="https://user-images.githubusercontent.com/12748752/150872225-4f7b267c-0672-44b7-aac3-0851c029250f.png" width=100% />

### Natural Language Processing and Deep Learning
![light](https://user-images.githubusercontent.com/12748752/134754235-ae8efaf0-a27a-46f0-b439-b114cbb8cf3e.png)
* The developments in the field of deep learning that have led to massive increases in performance in NLP.
* **Before deep learning**, the main techniques used in NLP were the _**bag-of-words**_ model and techniques like _**TF-IDF**_, _**Naive Bays**_ and _**Support Vector Machine(SVM)**_.
* In fact, this is a quick, robust, simple system in today standerd.
<img src="https://user-images.githubusercontent.com/12748752/151645612-ce7511a7-13e7-44b2-afe2-30eab70b9980.png" width=60% />

* **Nowadays**, in advanced areas of NLP, we use techniques like _**Hidden Markov Models**_ to do things like 
  * ***speech recognition*** and 
  * ***parts of speech tagging***.

> #### **Problem with Bag of Words**
   * Consider the phrases - ***dog toy*** and ***toy dog***
   * These are different things, but in a Bag of Words Model ordered does not matter, and so these would be treated the same.
> #### **Solution**
   * **Neural Network**- Modeling sentences as sequences and as hierarchy(**_LSTM_**) has led to state of the art improvements over previous go to techniques.
   * **Word Embeddings**- These give words a neural representation so that words can be plugged into a Neural Network just like any other feature vector. 

## References
![deep](https://user-images.githubusercontent.com/12748752/150695343-8977b5d0-3cd4-4959-b90e-9fe72d336d42.png)
* 
