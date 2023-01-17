## Index
![deep](https://user-images.githubusercontent.com/12748752/150695343-8977b5d0-3cd4-4959-b90e-9fe72d336d42.png)
### _NLP(Natural language processing)_
 * [What is NLP?](#natural-language-processing-nlp)
 * [Why we learn NLP?](#why-learn-nlp)
 * [General NLP tasks](#typical-nlp-tasks)
 * [Why NLP is so hard](#why-it-is-hard)
 * [Main NLP Approaches](#main-approaches-of-nlp)
 * [NLP Roadmap](#nlp-roadmap)
 
### [Text Preprocessing Level 1- Stopwords, Tokens, Stemming, Lammetization](https://github.com/iAmKankan/NaturalLanguageProcessing-NLP/tree/master/Text%20Preprocessing%20Level%23%201)
### [Text Preprocessing Level 2- Bag Of Words, TFIDF, Unigrams, Bigram](https://github.com/iAmKankan/NaturalLanguageProcessing-NLP/tree/master/Text%20Preprocessing%20Level%23%202)
### [Text Preprocessing Level 3- _Word Embeddings(Word2vec, One-hot, The Skip-Gram Mode, CBOW, GLOVE)_](https://github.com/iAmKankan/Natural-Language-Processing-NLP-Tutorial/blob/master/word_embedding.md)
### _NLP and Probability_
 * [_Why we need _Probability_ in NLP_?](https://github.com/iAmKankan/Mathematics/blob/main/probability/README.md)
### [_References_](#references-1)


## Natural Language Processing (NLP)
![deep](https://user-images.githubusercontent.com/12748752/150695343-8977b5d0-3cd4-4959-b90e-9fe72d336d42.png)
#### _**Natural language processing**_ is a subset of Artificial intelligence that helps computers to understand, interpret, and utilize the human languages. 
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

## Typical NLP tasks
![light](https://user-images.githubusercontent.com/12748752/150695340-c086876c-1e29-4493-b03b-cbff51dba02a.png)
| ${\color{Purple}\textrm{Information Retrieval}}$ | ${\color{Purple}\textrm{Find documents based on keywords}}$                                                                    |
|:------------------------|:-------------------------------------------------------------------------------------------------------|
| ${\color{Purple}\textrm{Information Extraction}}$   |${\color{Purple}\textrm{ Identify and extract personal name, date, company name, city..}}$                                        |
| ${\color{Purple}\textrm{Language generation}}$      |${\color{Purple}\textrm{ Description based on a photograph, Title for a photograph}}$                                             |
| ${\color{Purple}\textrm{Text classification}}$      |${\color{Purple}\textrm{ Assigning predefined categorization to documents. Identify Spam emails and move them to a Spam folder}}$ |
| ${\color{Purple}\textrm{Machine Translation}}$      |${\color{Purple}\textrm{ Translate any language Text to another}}$                                                                |
| ${\color{Purple}\textrm{Grammar checkers}}$         |${\color{Purple}\textrm{ Check the grammar for any language}}$ 

### Why learn NLP?
![light](https://user-images.githubusercontent.com/12748752/150695340-c086876c-1e29-4493-b03b-cbff51dba02a.png)
#### Some example like they are built with the use of NLP :

   1. Spell Correction(MS Word/any other editor)
   2. Search engines(Google, Bing, Yahoo)
   3. Speech engines(like Siri, Google assistant)
   4. Spam classifiers(All e-mails services)
   5. News feeds(Google, Yahoo!, and so on)
   6. Machine Translation(Google translation)
   7. IBM Watson

#### Some NLP tools
Most of the tools are written in Java and have similar functionalities. **GATE**, **Mallet**, **Open NLP**, **UIMA**, **Standford toolkit**, **Gensim**, **NLTK(Natural Language Tool kit)**.

## Why it is Hard?
![light](https://user-images.githubusercontent.com/12748752/150695340-c086876c-1e29-4493-b03b-cbff51dba02a.png)
* Multiple ways of representation of the same scenario
* Includes common sense and contextual representation
* Complex representation information (simple to hard vocabulary)
* Mixing of visual cues
* Ambiguous in nature
* Idioms, metaphors, sarcasm (Yeah! right), double negatives, etc. make it difficult for automatic processing
* Human language interpretation depends on real world, common sense, and contextual knowledge

### NLP Roadmap
![light](https://user-images.githubusercontent.com/12748752/150695340-c086876c-1e29-4493-b03b-cbff51dba02a.png)
<img src="https://user-images.githubusercontent.com/12748752/182266135-83fed5d6-1cb4-4f99-83f1-332f5bde9a7a.png" width=60%/>

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

### Sequence Learning
![plum](https://user-images.githubusercontent.com/12748752/126882596-b9ba4645-7001-435e-9a3c-d4416a2543c1.png)
Sequence learning is the study of machine learning algorithms designed for applications that require **sequential data** or **temporal data**.
#### RECURRENT NEURAL NETWORK
* Sequential data prediction is considered as a key problem in machine learning and artificial intelligence
* Unlike images where we look at the entire image, we read **text documents sequentially** to understand the content. 
* The likelihood of any sentence can be determined from everyday use of language.
* The earlier sequence of words (int time) is important to predict the next word, sentence, paragraph or chapter.
* If a word occurs twice in a sentence, but could not be accommodated in the sliding window, then the word is learned twice
* An architecture that does not impose a fixed-length limit on the prior context

**RNN-Language Model**-_Encoding a sentence into a fixed sized vector_-Exploding and vanishing gradients-LSTM-GRU

## References
![deep](https://user-images.githubusercontent.com/12748752/150695343-8977b5d0-3cd4-4959-b90e-9fe72d336d42.png)

