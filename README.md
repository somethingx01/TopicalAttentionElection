# TopicalAttentionElection
An opinion dynamic tracing model on dataset II

=============
Downloading large datafiles
-------------
Download dataset

#ElectionDataset.7z 
This repository should include preprocessed datasets organized in epochs, which are essential for for training and prediction. However, github doesn't allow large files to be upload, so you have to manually download the dataset and place them in the ./datasets/ directory. Please click https://s3-ap-southeast-1.amazonaws.com/somethingx86dynamics/dataset_election_and_params/ElectionDataset.7z to download the ElectionDataset.7z file.

#ElectionParams.7z
The params are essential for setting the settings.py(e.g., Traning_Instance_Count, Testing_Instance_Count) every time you perform training or prediction. Please click https://s3-ap-southeast-1.amazonaws.com/somethingx86dynamics/dataset_election_and_params/ElectionParams.7z to download the ElectionParams.7z file.

-------------
Download saved model

#model
'model' is the file name. 'model' is the trained and saved model, you can load it to reproduce the experiment results. Click https://s3-ap-southeast-1.amazonaws.com/somethingx86dynamics/dataset_election_and_params/model to download the 'model' file. You should place it in the ./save/0/ directory so that the default 'prediction' function in train.py can detect it. 

-------------
Calculate dataset statistics

#Dataset Statistics:
Run the main_sentiment_instance_counts_epochs.py. Note that the dataset epochs are organized in an time-descending order. That is, SNSTtrain_10 for epoch 0, SNStrain_09 for epoch 1, etc.

=============
Training and prediction
-------------
Training

#A Quick Start
If your machine is not eligible for a training (CUDA 7.0+ with 8G+GPURAM, 100G RAM), then loading a trained model ( by commenting train() ) and performing prediction would be suggested, whether on CPU or GPU.

-------------
Prediction

#Predict an epoch from trained models:
The defult code is predicting EPOCH_10.

#Understandable Topics:
