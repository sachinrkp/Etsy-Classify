# Etsy-Classify

##DATASET
More than 5 million active sellers on Etsy's marketplace 
have approximately 100 million current listings for sale. A 
portion of those items are given as training data. The Etsy 
dataset was provided by the company itself and it contains a 
zip files consisting of two file types (i) Parquet (ii) TFRecords
Both these files types have train and test folder consisting of 
train and test files. The parquet files consist only textual data 
whereas TFRecords files have images in it. The overall size of 
the dataset was 14Gb zipped.

##Data Understanding
• The training dataset contains 21 columns whereas, the 
test dataset contains 15 columns. 
• Total records in training dataset 245K and in test 
dataset has 27K records.
• The following product attributes which were to be 
predicted had no missing values in them.
• Top Category ID or Top Category Text has 15 unique 
classes, Bottom Category ID or Bottom Category ID
has 2782 classes and Color ID or color Text has 20 
unique classes.
• The remaining 14 out of 15 columns have missing 
values of different proportions and it was observed that 
these were Missing at random, and some were Missing 
not at random.
• The data in color text column is highly skewed.

###Since dataset is confidential cannot pe published in opensource domain.


##Challenge
Etsy has nearly 100 Million active listings on the etsy.com marketplace for sale from more than 5
million active sellers. You are provided a subset of those products as the training data.
The task is to leverage the training dataset to learn patterns from and to predict the following
attributes on an unseen test dataset given a products’ information:
● top category id
● bottom category id
● color id
The goal is to maximize F1 for each of the classes on each attribute to predict (top category,
bottom category and color). Your approaches and models will be benchmarked against a hidden
test dataset.
Bonus points will be given for submissions that:
● the trained model predicts the three attributes at the same time
● visualize some learned representations or embeddings and show that similar items
cluster together
● compares the performance of pre-trained embeddings taken from hubs or papers with a
fine-tuned model