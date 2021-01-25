# Simple-Chatbot-with-Pytorch
Created a chatbot using a Recurent Sequence to sequence model that were trained on movie scripts from the "Cornell movie dialogs Corpus". 

## Data Preprocessing
1. Datasets were imported from the Cornell Movie-dialog Corpus (https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html). This Corpus has 220,579 conversations and  304,713 total statements 
2. The Sentences were grouped into pairs and a vocabulary with over 18,000 words was created from them. 

## Building Model
A Sequence-to-Sequence model was used to create this chatbot. Two RNN were used here; the Encoder and the Decoder. The Encoder takes the input sentence fed into the chatbot and encodes it before feeding it to the decoder which then  creates a reply. 

![Screenshot](seq2seq_ts.png)
image source: https://jeddy92.github.io/JEddy92.github.io/ts_seq2seq_intro/

#Encoder 
The Encoder is a bi-directional multi-layered GRU. Used a bi-directional GRU to be able to encode both future and past context. 

