# Classifying-Disaster-Tweets
Use three different techniques to classify a tweet as either a 'Disaster Tweet' or 'Non-Disaster Tweet'.

Description

Twitter has become an important communication channel in times of emergency. The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies).

But, it’s not always clear whether a person’s words are actually announcing a disaster. Take this example the following tweet: "On the plus side LOOK AT THE SKY LAST NIGHT IT WAS ABLAZE"

The author explicitly uses the word “ABLAZE” but means it metaphorically. This is clear to a human right away, especially with the visual aid. But it’s less clear to a machine.

The challenged is to build a machine learning model that predicts which Tweets are about real disasters and which one’s aren’t. You’ll have access to a dataset of 10,000 tweets that were hand classified. 

Disclaimer: The dataset for this competition contains text that may be considered profane, vulgar, or offensive.


Dataset Description

Each sample in the train and test set has the following information:
The text of a tweet, A keyword from that tweet (although this may be blank!), The location the tweet was sent from (may also be blank)

Files
train.csv - the training set
test.csv - the test set
sample_submission.csv - a sample submission file in the correct format

Columns
id - a unique identifier for each tweet
text - the text of the tweet
location - the location the tweet was sent from (may be blank)
keyword - a particular keyword from the tweet (may be blank)
target - in train.csv only, this denotes whether a tweet is about a real disaster (1) or not (0)

Evaluation

You are predicting whether a given tweet is about a real disaster or not. If so, predict a 1. If not, predict a 0.

Submissions are evaluated using F1 between the predicted and expected answers.

F1 is calculated as follows:
𝐹1=2∗𝑝𝑟𝑒𝑐𝑖𝑠𝑖𝑜𝑛∗𝑟𝑒𝑐𝑎𝑙𝑙𝑝𝑟𝑒𝑐𝑖𝑠𝑖𝑜𝑛+𝑟𝑒𝑐𝑎𝑙𝑙

where:

𝑝𝑟𝑒𝑐𝑖𝑠𝑖𝑜𝑛=𝑇𝑃𝑇𝑃+𝐹𝑃

𝑟𝑒𝑐𝑎𝑙𝑙=𝑇𝑃𝑇𝑃+𝐹𝑁

and:

True Positive [TP] = your prediction is 1, and the ground truth is also 1 - you predicted a positive and that's true!
False Positive [FP] = your prediction is 1, and the ground truth is 0 - you predicted a positive, and that's false.
False Negative [FN] = your prediction is 0, and the ground truth is 1 - you predicted a negative, and that's false.
