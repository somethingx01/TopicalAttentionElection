# TopicalAttentionElection
An opinion dynamic tracing model on dataset II

Downloading large datafiles
-------------
Download dataset

* Epoched Datased
This repository should include preprocessed datasets organized in epochs, which are essential for training and prediction. However, github doesn't allow large files to be upload, so you have to manually download the dataset and place them in the ./datasets/ directory. Please click https://s3-ap-southeast-1.amazonaws.com/datasetandparams/dataset_election_and_params/ElectionDataset.7z to download the ElectionDataset.7z file.

* Tweets
If you are looking for the original tweets, i.e., 452128 tweets as mentioned in Table 1, please download the tweet IDs by https://datasetandparams.s3-ap-southeast-1.amazonaws.com/dataset_election_and_params/ElectionTweetIDs.txt

* UserID (mosaiced) - TweetIDs
If you are looking for the original user-tweet mapping, i.e., 108689 users and their tweets, please download the userID - tweetIDs by https://datasetandparams.s3-ap-southeast-1.amazonaws.com/dataset_election_and_params/Election_userid2tweetids_mosaiceduserid2tweetid Be aware that the userIDs are masked. That is to say, you may need to crawl the tweets to get the true auther/user id. 

* UserID (mosaiced) - FriendIDs (mosaiced)
If you are looking for the original user-friend relationships, i.e., 108689 users and their friends, please download the userID - friendIDs by https://datasetandparams.s3-ap-southeast-1.amazonaws.com/dataset_election_and_params/Election_userid2friendids_relationshipmosaiced


# ElectionParams.7z
The params are essential for setting the settings.py(e.g., Traning_Instance_Count, Testing_Instance_Count) every time you perform training or prediction. Please click https://s3-ap-southeast-1.amazonaws.com/datasetandparams/dataset_election_and_params/ElectionParams.7z to download the ElectionParams.7z file.

Calculate dataset statistics
-------------

# Dataset Statistics:
Run the main_sentiment_instance_counts_epochs.py. Note that the dataset epochs are organized in an time-descending order. That is, SNSTtrain_10 for epoch 0, SNStrain_09 for epoch 1, etc.

## Text Content
For dataset text content purposes, please redirect to https://github.com/somethingx01/TwitterCrawlerUsingIDs.

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
