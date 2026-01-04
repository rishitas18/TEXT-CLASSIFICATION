# TEXT-CLASSIFICATION
Implement some state-of-the-art text classification models with TensorFlow.

# Requirement:

>Python3
>TensorFlow >= 1.4
>
Note: Original code is written in TensorFlow 1.4, while the VocabularyProcessor is depreciated, updated code changes to use tf.keras.preprocessing.text to do preprocessing. The new preprocessing function is named data_preprocessing_v2

# Dataset
You can load the data with

dbpedia = tf.contrib.learn.datasets.load_dataset('dbpedia', test_with_fake_data=FLAGS.test_with_fake_data)

Or download it from Baidu Yun.

# Attention is All Your Need

Paper: Attention Is All You Need

See multi_head.py

Use self-attention where Query = Key = Value = sentence after word embedding

Multihead Attention module is implemented by Kyubyong

# IndRNN for Text Classification

Paper: Independently Recurrent Neural Network (IndRNN): Building A Longer and Deeper RNN

IndRNNCell is implemented by batzener

# Attention-Based Bidirection LSTM for Text Classification

Paper: Attention-Based Bidirectional Long Short-Term Memory Networks for Relation Classification

See attn_bi_lstm.py

# Hierarchical Attention Networks for Text Classification
Paper: Hierarchical Attention Networks for Document Classification

See attn_lstm_hierarchical.py

Attention module is implemented by ilivans/tf-rnn-attention .

# Adversarial Training Methods For Supervised Text Classification

Paper: Adversarial Training Methods For Semi-Supervised Text Classification

See: adversrial_abblstm.py

# Convolutional Neural Networks for Sentence Classification

Paper: Convolutional Neural Networks for Sentence Classification

See: cnn.py

# RMDL: Random Multimodel Deep Learning for Classification

Paper: RMDL: Random Multimodel Deep Learning for Classification

See: RMDL.py See: RMDL Github

# Note: The parameters are not fine-tuned, you can modify the kernel as you want.

# Performance
Model	Test Accuracy	Notes
Attention-based Bi-LSTM	98.23 %	
HAN	89.15%	1080Ti 10 epochs 12 min
Adversarial Attention-based Bi-LSTM	98.5%	AWS p2 2 hours
IndRNN	98.39%	1080Ti 10 epochs 10 min
Attention is All Your Need	97.81%	1080Ti 15 epochs 8 min
RMDL	98.91%	2X Tesla Xp (3 RDLs)
CNN	98.37%	

# Welcome To Contribute

If you have any models implemented with great performance, you're welcome to contribute. Also, I'm glad to help if you have any problems with the project, feel free to raise a issue.
