# Gensim
## Difinition
* Gensim is billed as a Natural Language Processing package that does ‘Topic Modeling for Humans’.  
* Topic modeling, it is a technique to extract the underlying topics from large volumes of text. Gensim provides algorithms like LDA and LSI and the necessary sophistication to build high-quality topic models.
* It is a great package for processing texts, working with word vector models (such as Word2Vec, FastText etc) and for building topic models.
* It lets you handle large text files without having to load the entire file in memory.
* It is a great package for processing texts, working with word vector models (such as Word2Vec, FastText etc) and for building topic models.
* it lets you handle large text files without having to load the entire file in memory.

## How it works?
* In order to work on text documents, Gensim requires the words (aka tokens) be converted to unique ids. In order to achieve that, Gensim lets you create a Dictionary object that maps each word to a unique id.
* By converting your text/sentences to a [list of words] and pass it to the corpora.Dictionary() object.
* gensim handlecan handle input text typically in 3 different forms:
  * As sentences stored in python’s native list object
  * As one single text file, small or large.
  * In multiple text files.
