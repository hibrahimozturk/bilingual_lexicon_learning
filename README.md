## Download Links
* Wikipedia comparable corporas https://linguatools.org/tools/corpora/wikipedia-comparable-corpora/ 
* Wikipedia corpora english-italian download link: https://www.dropbox.com/s/jjkfn7v19tnxnww/wikicomp-2014_enit.xml.bz2?dl=0
* Python gensim word2vec italian language model http://hlt.isti.cnr.it/wordembeddings/skipgram_wiki_window10_size300_neg-samples10.tar.gz
* Python gensim word2vec english language model https://drive.google.com/file/d/0B7XkCwpI5KDYNlNUTTlSS21pQmM/edit
* Python fasttext english language model https://dl.fbaipublicfiles.com/fasttext/vectors-english/wiki-news-300d-1M.vec.zip
* Python fasttext italian language model  https://www.dropbox.com/s/orqfu6mb9cj9ewr/it.tar.gz?dl=0

## Python packages

* nltk
* google-cloud-translate
* numpy
* gensim (word2vec)
* fasttext
* pytorch
* matplotlib
* scikit-learn

## Dataset

[English word, italian word]

* Total words:    15278
  * Training set:   11590
  * Validation set: 2939
  * Test set:       749


We pair each english word with true translation and wrong translation.

* After filtering words not included in word2vec
  * Training pairs   : 20977
  * Validation pairs : 5322
  * Testing pairs    : 1381

## Experiments

### adam/earlyfusion/first
Test accuracy: 86.96596669080377 precision: 0.8593530239099859 recall 0.8842257597684515 f1 0.8716119828815977

### adam/earlyfusion/lrelu
Test accuracy: 88.26937002172339 precision: 0.8598639455782313 recall 0.914616497829233 f1 0.8863955119214586

### adam/earlyfusion/no-bn-lrelu
Test accuracy: 90.65894279507603 precision: 0.9194029850746268 recall:0.8914616497829233 f1: 0.9052167523879501

### adam/shallow2-3/all-bn-lrelu
Test accuracy: 83.7074583635047 precision: 0.8218232044198895 recall:0.8610709117221418 f1: 0.8409893992932863

## Todo

* [x] Tokens will be extracted from corpora
* [x] Pairs will be generated by google translate
* [x] Training, validation and test sets will be splitted
* [x] python word2vec for it and en will be installed 
* [x] pytorch special dataloader will be implemented  
* [x] models will be trained on pytorch  
* [x] evaluation will be implemented  
