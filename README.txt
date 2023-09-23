This project is to explore and implement the Doc2vec model.

Similar to word2vec, which is to vectorize the words, the Doc2vec model makes documents/sentences numeric. It is useful for document classification, spam detection, etc. 

There are two algorithms to implement doc2vec. One is Distributed Meomory version of Paragraph Vector (PV-DM), which is linked to CBOW. The idea is to add one extra node (paragraph id) into the input layer. The size of the paragraph id is the same as other word nodes. In reality, we can utilize the pre-trained model directly. I think the mechanism behind it is that the word tokens have already been trained. For each document, the paragraph id is the only unknown node. We calculate it to minimize the cost function. 

Another algorithm is Distributed Bag of Words version of Paragraph Vector (PV-DBOW), which is similar as the skip-gram in word2vec. 

In the code, I applied PV-DM model to the text. The text feature is very simple. The accuracy of the model can't beat others. I think how to generate the features for NLP is important. I will do the test later.

When we have numeric representation for each document (300-dim vectors), we can train the classifier on them. The first we tried is Logistic regression. The accuracy on test file is 86.66%.

To compare the result of BERT and doc2vec, I will apply ANN model on doc2vec results as well. I will update the results in other projects.