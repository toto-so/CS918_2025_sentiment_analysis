cs918_assignment2

Description
-----------
This folder contains the following:
- 'cs918_assignment_2.ipynb' - a jupyter notebook that trains three classical classifiers and a LSTM classifier for sentiment classification and evaluate on the test sets;
- 'CS918 Assignment 2.pdf' - a PDF file that contains a report that summarises the techniques and features used for the classification, as well as the performance results; and
- this README.md.

Please download a zipped file from https://figshare.com/s/fa9b3c0f402767e34e82 and unzip in the cs918_assignment2 folder. The zipped file contains:
- 'semeval-tweets' - a folder that contains tweet datasets, one for training, one for development, and the rest for test;
- 'pickle' - a folder that contains pre-trained data (see below);
- 'opinion-lexicon-English' - a folder that contains lexicons of positive and negative words;
- 'lstm' - a folder that contains trained LSTM model;
- 'plot' - a folder that contains plots of macro f1 scores; and
- glove.6B.100d.txt - a text file for loading GloVe pre-trained word embedding.

Required packages
-----------------
Please install re, numpy, os, sys, emoji, nltk, pickle, scipy, scikit-learn, torch, torchvision, torchaudio, transformers, matplotlib.

Test datasets
-------------
Please add test datasets to the 'semeval-tweets' folder. The dataset must be formatted as TSV with one tweet per row that includes the following values:

    tweet-id<tab>sentiment<tab>tweet-text

where sentiment is one of {positive, negative, neutral}.

CUDA (for LSTM training)
------------------------
If possible, please run on CUDA for efficiency. If CUDA is not available, we run on CPU.

Pickle
------
The pickle (.pkl) files in the 'pickle' folder are as follows:
1. data.pkl - a list of dictionaries of pre-processed datasets
2. feature_vec.pkl - a dictionary of fitted vectorisers for each feature
3. clf.pkl - a dictionary of trained traditional classifiers with the respective feature
4. LR_SVM_C.pkl - a dictionary of C values for logistics regression and svm
See Section 'Boolean variables' if you wish to train from seratch.

Saved LSTM models
-----------------
LSTM models are saved as torch (.pth) files in the 'lstm' folder.

Boolean variables (boo1, boo2, boo3)
------------------------------------
The three boolean variables determine if users prefer pre-trained data or training from scratch.
1. boo1 - Loading pre-processed tweets
2. boo2 - Loading pre-fitted vectorisers
3. boo3 - Loading pre-trained traditional classifiers
Note: We always load pickle for developments in Appendices.

Plots
-----
Plots of macro F1 scores are saved as .png in the 'plot' folder.

Reference
---------
[1] C. Baziotis, ``emoticons.py,'' GitHub repository, 5 December 2017. Accessed: 25 March 2025. [Online]. Available: https://github.com/cbaziotis/ekphrasis/blob/master/ekphrasis/dicts/emoticons.py.

