---
title: "Sequential Word Prediction with LSTM: A 6-gram Model Implementation"
excerpt: "Implemented an LSTM-based 6-gram model to predict the next word in sentences using the 'austen-sense.txt' dataset. Achieved coherent text generation and visualized training progress through loss value plots.<br/>"
---

In this mini project, I implemented an LSTM (Long Short-Term Memory) model to predict the next word in a sentence, akin to building an N-gram model. N-gram models leverage statistical probabilities from a sequence of words to predict the likelihood of the next word based on preceding words. I specifically constructed a 6-gram model using an LSTM neural network, predicting the next word based on the previous 5 words. The training utilized the 'austen-sense.txt' dataset from the Gutenberg Corpus in NLTK.

The project involved preprocessing the dataset by removing noise, including HTML tags, square brackets, special characters, and extra spaces. The NLTK module was employed for data retrieval, and the dataset was tokenized for model training. The LSTM neural network was trained using categorical cross-entropy and the Adam optimizer, with the 6-gram structure as input and output.

Deliverables for this project include a plot illustrating the loss values across epochs during training. Additionally, the LSTM model was utilized to generate a 100-word text, starting with the seed phrase 'his natural shyness was overcome'. This generation process involved predicting the 6th word successively in a loop based on the previous 5 words.

![lstm_plot](https://github.com/devadharshini97/devadharshini.github.io/assets/41442650/7db540f5-9076-4231-97f4-a444ea28f6d0)

The project not only demonstrated proficiency in implementing LSTM models for sequence prediction but also showcased the generation of coherent text based on learned patterns from the training dataset.

![lstm_text](https://github.com/devadharshini97/devadharshini.github.io/assets/41442650/47dcd21d-3a7a-4159-ace7-3a648ddc8b2b)
