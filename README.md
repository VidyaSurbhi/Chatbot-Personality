# Chatbot-Personality
Chatbot personality: the sum of any human-like characteristics the bot is programmed to display. Using machine-learning, theano, sentiment-analysis, cnn, lstm, personality-insights, convolutional-neural-networks, opinion-mining, cnn-keras, lstm-neural-networks, personality-profiling, personality-traits.


Deep Learning-Based Document Modeling for Personality Detection from Text
This code implements the model discussed in Deep Learning-Based Document Modeling for Personality Detection from Text for detection of Big-Five personality traits, namely:

Extroversion
Neuroticism
Agreeableness
Conscientiousness
Openness
Requirements
Python 2.7
Theano 0.7 (Tested)
Pandas 18.0 (Tested)
Pre-trained GoogleNews word2vec vector
Preprocessing
process_data.py prepares the data for training. It requires three command-line arguments:

Path to google word2vec file (GoogleNews-vectors-negative300.bin)
Path to essays.csv file containing the annotated dataset
Path to mairesse.csv containing Mairesse features for each sample/essay
This code generates a pickle file essays_mairesse.p.

Example:

python process_data.py ./GoogleNews-vectors-negative300.bin ./essays.csv ./mairesse.csv
Training
conv_net_train.py trains and tests the model. It requires three command-line arguments:

Mode:
-static: word embeddings will remain fixed
-nonstatic: word embeddings will be trained
Word Embedding Type:
-rand: randomized word embedding (dimension is 300 by default; is hardcoded; can be changed by modifying default value of k in line 111 of process_data.py)
-word2vec: 300 dimensional google pre-trained word embeddings
Personality Trait:
0: Extroversion
1: Neuroticism
2: Agreeableness
3: Conscientiousness
4: Openness
