# Word Embedding

Word Embeddings are numeric representations of words in a lower-dimensional space, that capture semantic and syntactic information. They play a important role in Natural Language Processing (NLP) tasks.

# Need for Word Embedding?
- To reduce dimensionality.
- To use a word to predict the words around it.
- Helps in enhancing model interpretability due to numerical representation.
- Inter-word semantics and similarity can be captured.

# Word2Vec

Word2Vec is a neural approach for generating word embeddings. It belongs to the family of neural word embedding techniques and specifically falls under the category of distributed representation models. It is a popular technique in natural language processing (NLP).

- Represent words as continuous vector spaces.
- Aim: Capture the semantic relationships between words by mapping them to high-dimensional vectors.
- Words with similar meanings should have similar vector representations. Every word is assigned a vector. We start with either a random or one-hot vector.

# Artificial Neural Networks
Artificial Neural Networks (ANNs) are computer systems designed to mimic how the human brain processes information. Just like the brain uses neurons to process data and make decisions, ANNs use artificial neurons to analyze data, identify patterns and make predictions. These networks consist of layers of interconnected neurons that work together to solve complex problems.

# Loss Functions
A loss function is a mathematical way to measure how good or bad a model’s predictions are compared to the actual results. It gives a single number that tells us how far off the predictions are. The smaller the number, the better the model is doing.

# Optimizers
Optimizers are algorithms or methods used to minimize an error function(loss function)or to maximize the efficiency of production. Optimizers are mathematical functions which are dependent on model’s learnable parameters i.e Weights & Biases.

# CBOW
Continuous Bag of Words (CBOW) is a type of neural network architecture used in the Word2Vec model. The primary objective of CBOW is to predict a target word based on its context, which consists of the surrounding words in a given window. Given a sequence of words in a context window, the model is trained to predict the target word at the center of the window.

- Feedforward neural network with a single hidden layer.
- The input layer, hidden layer, and output layer represent the context words, learned continuous - vectors or embeddings, and the target word.
- Useful for learning distributed representations of words in a continuous vector space.

# Skipgram
The Skip-Gram model learns distributed representations of words in a continuous vector space. The main objective of Skip-Gram is to predict context words (words surrounding a target word) given a target word. This is the opposite of the Continuous Bag of Words (CBOW) model, where the objective is to predict the target word based on its context. It is shown that this method produces more meaningful embeddings.

