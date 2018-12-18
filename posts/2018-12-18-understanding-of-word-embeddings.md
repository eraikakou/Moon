Dive into Word Embeddings

## Why do we need Word Embeddings?
In natural language processing tasks there is a need to create a representation for words that capture their meanings, semantic relationships and the different types of contexts they are used in. And all of these are implemented by using Word Embeddings (or Word Vectors) or numerical representations of texts so that computers may handle them. As it turns out, many Machine Learning algorithms and almost all Deep Learning Architectures are incapable of processing strings or plain text in their raw form. They require numbers as inputs to perform any sort of job, be it classification, regression etc. in broad terms. And with the huge amount of data that is present in the text format, it is imperative to extract knowledge out of it and build applications.

## What are Word Embeddings?
In very simplistic terms, Word Embeddings are the texts converted into numbers and there may be different numerical representations of the same text. Let me now define Word Embeddings formally. A Word Embedding format generally tries to map a word using a dictionary to a vector.

## Different types of Word Embeddings
The different types of word embeddings can be broadly classified into three categories:

1. A vector representation of a word may be a **one-hot encoded vector** where 1 stands for the position where the word exists and 0 everywhere else. This is just a very simple method to represent a word in the vector form.

2. Frequency based Embedding

3. Prediction based Embedding

### Frequency based Embedding
There are generally three types of vectors that we encounter under this category.

- **Count Vector:**

In real world applications we might have a corpus which contains millions of documents. And with millions of document, we can extract hundreds of millions of unique words. So basically, the matrix that will be prepared like above will be a very sparse one and inefficient for any computation. So an alternative to using every unique word as a dictionary element would be to pick say top 10,000 words based on frequency and then prepare a dictionary. We may either take the frequency (number of times a word has appeared in the document) or the presence(has the word appeared in the document?) to be the entry in the count matrix M. But generally, frequency method is preferred over the latter.

- **TF-IDF Vector:**

Term frequency-inverse document frequency: This is another method which is based on the frequency method but it is different to the count vectorization in the sense that it takes into account not just the occurrence of a word in a single document but in the entire corpus. So, what is the rationale behind this? Let us try to understand.

Common words like ‘is’, ‘the’, ‘a’ etc. tend to appear quite frequently in comparison to the words which are important to a document. For example, a document A on Lionel Messi is going to contain more occurences of the word “Messi” in comparison to other documents. But common words like “the” etc. are also going to be present in higher frequency in almost every document.

Ideally, what we would want is to down weight the common words occurring in almost all documents and give more importance to words that appear in a subset of documents.

TF-IDF works by penalising these common words by assigning them lower weights while giving importance to words like Messi in a particular document.
- Co-Occurrence Vector
