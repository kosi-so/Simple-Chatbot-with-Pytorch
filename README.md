# Simple Chatbot with Pytorch
Created a chatbot using a Recurent Sequence to sequence model that were trained on movie scripts from the "Cornell movie dialogs Corpus". 

## Data Preprocessing
1. Datasets were imported from the Cornell Movie-dialog Corpus (https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html). This Corpus has 220,579 conversations and  304,713 total statements 
2. The Sentences were grouped into pairs and a vocabulary with over 18,000 words was created from them. 

## Building Model
A Sequence-to-Sequence model was used to create this chatbot. Two RNN were used here; the Encoder and the Decoder. The Encoder takes the input sentence fed into the chatbot and encodes it before feeding it to the decoder which then  creates a reply. 

![Screenshot](seq2seq_ts.png)
image source: https://jeddy92.github.io/JEddy92.github.io/ts_seq2seq_intro/

### Encoder 
The Encoder is a bi-directional multi-layered GRU. Used a bi-directional GRU to be able to encode both future and past context. 
The Encoder takes the input statement and encodes it, this encoded vector is then passed into the Decoder. 

### Decoder 
The Decoder generates the response to the input statement. It takes the encoded vector from the Encoder as input to generate the words that will serve as the response of the chatbot. 

## Training Model
A Negative Log likelihood is used to calculate the training loss. Adam Optimizer is used to update the parameters of the model. 
Gradients clipping and Teacher forcing were used to facilitate the training process. 

## Evaluation 
Evaluation here means how to get the chatbot to give responses when you input a sentence. Greedy Decoding is used to get the decoder output (word) with the highest softmax value for each timestep. 

## Testing Chatbot
Below is a breif conversation with the chatbot 

![Screenshot](Chatbot_chat.PNG)

# Acknowledgement
1. Yuan-Kuei Wu’s pytorch-chatbot implementation: https://github.com/ywk991112/pytorch-chatbot
2. Sean Robertson’s practical-pytorch seq2seq-translation example: https://github.com/spro/practical-pytorch/tree/master/seq2seq-translation
3. FloydHub’s Cornell Movie Corpus preprocessing code: https://github.com/floydhub/textutil-preprocess-cornell-movie-corpus
4. Chatbot Tutorial by Matthew Inkawhich https://pytorch.org/tutorials/beginner/chatbot_tutorial.html#define-training-procedure
