# Spam Classifier

A Naive Bayes spam classifier built in R using the SpamAssassin public email dataset.

## Overview
Classifies emails as spam or ham based on word frequencies using a Document-Term Matrix and Naive Bayes model.

## Data
Download the SpamAssassin dataset and place the folders inside a `/data` directory:
- easy_ham
- easy_ham_2
- hard_ham
- spam
- spam_2

## Requirements
Install the following R packages:
- tm
- e1071
- caret

## How to Run
Open the .Rmd file and run all chunks in order. Set the file paths in Step 1 to point to your local `/data` folder.

## Results
| Sparsity | Terms | Accuracy | Sensitivity |
|----------|-------|----------|-------------|
| 0.99     | 2616  | 62%      | 45%         |
| 0.95     | 521   | 79%      | 71%         |
| 0.90     | 227   | 88%      | 87%         |
| 0.85     | ~200  | 89%      | 89%         |

## Limitations
The model performs well on the test set but struggles on new plain-text emails because the retained terms are dominated by email header metadata rather than message body content.
