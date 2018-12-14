# Natural Language Processing and Deep Learning - Group1
_- Reimplementing the cBLSTM Language Models_

### Introduction
This repository contains a partial implementaion of the model presented in [Mousa & Schuller (2017)](http://aclweb.org/anthology/E/E17/E17-1096.pdf) implemented in Python using Keras and TensorFlow.

## Installation
To train the models, you need to download the Stanford IMDB dataset, found [here](http://ai.stanford.edu/~amaas/data/sentiment/), and the pretrained GloVe vectors, found [here](http://nlp.stanford.edu/data/glove.6B.zip). Unpack the dataset and the vectors in the repository folder.

Make sure you have all the necesarry libraries to run it, notably `Keras`, `TensorFlow`, `Nltk`, `Sklearn` and `Numpy`, but Python will let you know if you're missing something.

## Training
To train the **cBLSTM** language models, open up `cBLSTM-Language-Model.py` and make sure the top parameters are set correctly. Here you choose some sizes for the network, whether to train the positive or the negative LM, and chose a filename. Then run the file.

To train the **BLSTM** binary classifier, open up `BLSTM-Binary-Classifier.py` and set the parameters and filename. Then run the file.

Models are saved along the way in the `model` directory. Datasets and embedding matrices are saved in the `data` and can be resued by out commenting their generation in each Python-file.

## Predicting

Open up `Combined-classifier.py` and set the filenames of the three models to be used. All models are assumed to be in the `model` folder. Run the file.

<hr>

### Notes

All of the data preprocessing is included in the `prepros.py`-file and a range of utility functions are included in the `utils.py`, from embedding matrix generation, perplexity calculation, and dataset-splitting and -compiling. 