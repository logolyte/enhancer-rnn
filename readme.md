# Recurve neural network for identifying enhancers in the human genome

A recursive neural network made with Keras and Tensorflow in Python that can determine if a DNA sequence is an enhancer. The trained is found in the directory "Trained model", along with its training curve. The final accuracy was 0.761. The code for training and evaluating the model is found in the notebook file "enhancer-rnn.ipynb".

The training data consists of DNA sequences with and without enhancers compiled by Liu et al. (https://doi.org/10.1093/bioinformatics/btv604). These are found in enhancers.fasta and nonenhancers.fasta respectively.

This model was made for the final project in the course "Deep Learning - Methods and Applications" given by Umeå University.

## Model structure

 Bayesian optimization was used to find good hyperparameters for the model. The model chosen had one embedding layer, two bidirectional GRU layers, one dropout layer and three layers of alternating batch normalization and dense layers. Binary cross-entropy was used as the loss function during training, with Adam as the optimizer.
