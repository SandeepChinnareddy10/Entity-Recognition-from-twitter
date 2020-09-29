# Entity-Recognition-from-twitter

The increasing trend of spreading important information in distress can help patients reach out to prospective blood donors in a time bound manner. In the case of countries with low rates of blood donation record, blood donation is largely dependent on the families and friends of patients, usually through the word of mouth or peer to peer networking. The effect of such tweets in an emergency situation is largely limited to a user’s first few degrees of connections. My idea for solving this problem includes an NLP centric approach. In today’s world, linguistic along with handcrafted heuristics can act as the most representative set of signals.

Problem Statement: Entity recognition from Blood donation requests is the identification of the tweets that explicitly or implicitly request for blood donation and extraction of several handcrafted details such as blood group, quantity of blood required, location etc.

In this project, we present a Bidirectional Long Short Term Memory Conditional Random Fields (BiLSTM-CRF) to extract entities such as locations and the blood type etc from Twitter corpus. A BiLSTM model has been implemented to provide the Conditional Random fields with the emission score i.e, the hidden features. We were able to produce results which had a precision of 83%  in the test data in finding the geographical location from a tweet. After generating batches of same length tweets with padding, the LSTM network was used to produce probability distribution over tags for each token in a sentence. 

Building an LSTM network involved:(i) Declaring placeholders(ii) Building layers with computing forward cells and backward cells(iii) Computing predictions(iv) Computing loss and performing optimization(v) Train the network and predict tags

How to run:
1. Download the dataset 'BDC.txt'
2. Run the python notebook 'EBDR-and-NER-BiLSTM-CRF'

Libraries and packages used:
0. PyTorch
1. sys
2. jsonpickle
3. os
4. tweepy
5. csv
6. json
7. re
8. numpy as np
9. punctuation
10. sklearn
11. joblib
12. re

Future work:
1. Addition of an attentioan layer.
2. Implementation using GRU
