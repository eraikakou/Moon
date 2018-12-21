Dive into Word Embeddings

## Why do we need Word Embeddings?
In natural language processing tasks there is a need to create a representation for words that capture their meanings, semantic relationships and the different types of contexts they are used in. And all of these are implemented by using Word Embeddings (or Word Vectors) or numerical representations of texts so that computers may handle them. As it turns out, many Machine Learning algorithms and almost all Deep Learning Architectures are incapable of processing strings or plain text in their raw form. They require numbers as inputs to perform any sort of job, be it classification, regression etc. in broad terms. And with the huge amount of data that is present in the text format, it is imperative to extract knowledge out of it and build applications. 

## What are Word Embeddings?
In very simplistic terms, Word Embeddings are the texts converted into numbers and there may be different numerical representations of the same text. Let me now define Word Embeddings formally. A Word Embedding format generally tries to map a word using a dictionary to a vector. (Actually Word Embeddings are numerical representations of texts so that computers may handle them.)

## Different types of Word Embeddings
The different types of word embeddings can be broadly classified into three categories:

1. A vector representation of a word may be a **one-hot encoded vector** where 1 stands for the position where the word exists and 0 everywhere else. This is just a very simple method to represent a word in the vector form.

2. Frequency based Embedding

3. Prediction based Embedding

### Frequency based Embedding
There are generally three types of vectors that we encounter under this category.

- **Count Vector:**

Consider a Corpus C of D documents {d1,d2…..dD} and N unique tokens extracted out of the corpus C. The N tokens will form our dictionary and the size of the Count Vector matrix M will be given by D X N. Each row in the matrix M contains the frequency of tokens in document D(i). Now, a column can also be understood as word vector for the corresponding word in the matrix M. Here, the rows correspond to the documents in the corpus and the columns correspond to the tokens in the dictionary. Now there may be quite a few variations while preparing the above matrix M. The variations will be generally in-

1. The way dictionary is prepared.

Why? Because in real world applications we might have a corpus which contains millions of documents. And with millions of document, we can extract hundreds of millions of unique words. So basically, the matrix that will be prepared like above will be a very sparse one and inefficient for any computation. So an alternative to using every unique word as a dictionary element would be to pick say top 10,000 words based on frequency and then prepare a dictionary.

2. The way count is taken for each word.

We may either take the frequency (number of times a word has appeared in the document) or the presence(has the word appeared in the document?) to be the entry in the count matrix M. But generally, frequency method is preferred over the latter.

- **TF-IDF Vector:**

Term frequency-inverse document frequency: This is another method which is based on the frequency method but it is different to the count vectorization in the sense that it takes into account not just the occurrence of a word in a single document but in the entire corpus. So, what is the rationale behind this? Let us try to understand.

Common words like ‘is’, ‘the’, ‘a’ etc. tend to appear quite frequently in comparison to the words which are important to a document. For example, a document A on Lionel Messi is going to contain more occurences of the word “Messi” in comparison to other documents. But common words like “the” etc. are also going to be present in higher frequency in almost every document.

Ideally, what we would want is to down weight the common words occurring in almost all documents and give more importance to words that appear in a subset of documents.

TF-IDF works by penalising these common words by assigning them lower weights while giving importance to words like Messi in a particular document.

**TF** = (Number of times term t appears in a document)/(Number of terms in the document). It denotes the contribution of the word to the document i.e words relevant to the document should be frequent. 

**IDF** = log(N/n), where, N is the number of documents and n is the number of documents a term t has appeared in. Ideally, if a word has appeared in all the document, then probably that word is not relevant to a particular document. But if it has appeared in a subset of documents then probably the word is of some relevance to the documents it is present in.

- **Co-Occurrence Vector / Co-Occurrence Matrix with a fixed context window:**

The big idea – Similar words tend to occur together and will have similar context.

**Co-occurrence** – For a given corpus, the co-occurrence of a pair of words say w1 and w2 is the number of times they have appeared together in a Context Window.

**Context Window** – Context window is specified by a number and the direction. (and for calculating the co-occurrence only these words will be counted)

Variations of Co-occurrence Matrix

Let’s say there are V unique words in the corpus. So Vocabulary size = V. The columns of the Co-occurrence matrix form the context words. The different variations of Co-Occurrence Matrix are-

1. A co-occurrence matrix of size V X V.

Now, for even a decent corpus V gets very large and difficult to handle. So generally, this architecture is never preferred in practice.

2. A co-occurrence matrix of size V X N,

where N is a subset of V and can be obtained by removing irrelevant words like stopwords etc. for example. This is still very large and presents computational difficulties. But, remember this co-occurrence matrix is not the word vector representation that is generally used. Instead, this Co-occurrence matrix is decomposed using techniques like PCA, SVD etc. into factors and combination of these factors forms the word vector representation.

Let me illustrate this more clearly. For example, you perform PCA on the above matrix of size VXV. You will obtain V principal components. You can choose k components out of these V components. So, the new matrix will be of the form V X k.

And, a single word, instead of being represented in V dimensions will be represented in k dimensions while still capturing almost the same semantic meaning. k is generally of the order of hundreds.

So, what PCA does at the back is decompose Co-Occurrence matrix into three matrices, U,S and V where U and V are both orthogonal matrices. What is of importance is that dot product of U and S gives the word vector representation and V gives the word context representation.

**Advantages of Co-occurrence Matrix**

- It preserves the semantic relationship between words. i.e man and woman tend to be closer than man and apple.
- It uses SVD at its core, which produces more accurate word vector representations than existing methods.
- It uses factorization which is a well-defined problem and can be efficiently solved.
- It has to be computed once and can be used anytime once computed. In this sense, it is faster in comparison to others.
 

**Disadvantages of Co-Occurrence Matrix**

- It requires huge memory to store the co-occurrence matrix.
But, this problem can be circumvented by factorizing the matrix out of the system for example in Hadoop clusters etc. and can be saved.
