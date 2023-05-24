
# Aksharantar Transliteration using Attention Mechanism
This repository contains an implementation of a Recurrent Neural Network (RNN) model for transliterating words from English to Hindi, specifically using the Aksharantar dataset. The model in this version incorporates the attention mechanism, which enhances the transliteration performance.

# Dataset
The Aksharantar dataset, consisting of English words and their corresponding Hindi transliterations, was used for training and evaluation. The dataset can be found here.

# Model Architecture
The transliteration model with attention mechanism improves upon the traditional encoder-decoder architecture. Attention allows the model to focus on different parts of the input word while generating the transliteration. This mechanism enables the model to better align and aligns the source and target sequences, resulting in improved accuracy.

The Encoder class is responsible for encoding the input word into a hidden state, while the Attention dynamically computes the attention weights. The Decoder class combines the attention context with the hidden state to generate the transliterated output.

The Seq2Seq class utilizes the Encoder, Attention, and Decoder classes to perform the transliteration task. It combines all the components and handles the training and inference processes.

# Training:
choose the hyperparameters accordingly and run the cells sweep_config = { 'method': 'bayes', 'metric': {'goal': 'maximize', 'name': 'val_accuracy'}, 'parameters': {'embedding_size': {'values': [128, 256, 512]}, 'hidden_size': {'values': [128, 256, 512]}, 'beam_search':{'values':[1,2,3,4,5]}, 'dropout': {'values': [0.1, 0.2, 0.3, 0.4]}, 'dec_num_layers':{'values': [1,2,3]}, 'batch_size': {'values': [128,256,512]}, 'cell_type': {'values': ['LSTM','GRU','RNN']}, 'epochs' :{'values':[10,20,30,40]}, 'enc_num_layers': {'values': [1,2,3]}

            }}
def train_func(): var1 = wandb.init() var2 = var1.config if(var2.cell_type=="RNN"): var2.epochs = 10 training_function(input_size_encoder ,var2.embedding_size, var2.dropout, var2.cell_type, var2.hidden_size, var2.enc_num_layers, var2.enc_num_layers,var2.epochs,num_decoder_tokens,num_decoder_tokens,var2.batch_size,var2.beam_search)

import wandb wandb.login(key='1ee7845713d1303ac1abff70cf959518e1ae311c') wandb.init(project="cs6910_RNN_attention")
