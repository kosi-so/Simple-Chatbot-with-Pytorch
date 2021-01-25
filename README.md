# Simple-Chatbot-with-Pytorch
Created a chatbot using a Recurent Sequence to sequence model that were trained on movie scripts from the "Cornell movie dialogs Corpus". 

## Data Preprocessing
1. Datasets were imported from the Cornell Movie-dialog Corpus (https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html). This Corpus has 220,579 conversations and  304,713 total statements 
2. The Sentences were grouped into pairs and a vocabulary with over 18,000 words was created from them. 

## Building Model
A Sequence-to-Sequence model was used to create this chatbot. Two RNN were used here; the Encoder and the Decoder. The Encoder takes the input sentence fed into the chatbot and encodes it before feeding it to the decoder which then  creates a reply. 

