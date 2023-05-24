# cs6910Assignment3
# Aksharantar Transliteration using RNN
This repository contains an implementation of a Recurrent Neural Network (RNN) for transliterating words from English to Hindi, specifically using the Aksharantar dataset. Two versions of the transliteration model are included: one with attention mechanism and another without attention.

# Dataset
The Aksharantar dataset, consisting of English words and their corresponding Hindi transliterations, was used for training and evaluation. 

# Model Architecture
The transliteration model consists of an encoder-decoder architecture. The Encoder class is responsible for encoding the input word into a hidden state, while the Decoder class decodes the hidden state to generate the transliterated output. These classes can be found in the respective files.

The Seq2Seq class utilizes the Encoder and Decoder classes to perform the transliteration task. It combines both components and handles the training and inference processes.

# Repository Structure
## attention: Folder containing the version of the model with attention mechanism.
## no_attention: Folder containing the version of the model without attention mechanism.
