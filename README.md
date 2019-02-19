# [Quora Insincere Questions Classification](https://www.kaggle.com/c/quora-insincere-questions-classification)
## Best solution
|rank   |solution             |kernel         |author                   |
|-------|---------------------|---------------|-------------------------|
|1st|[1st Place Solution](https://www.kaggle.com/c/quora-insincere-questions-classification/discussion/80568)|kernel|Psi|
|3rd|[3rd Place Solution](https://www.kaggle.com/c/quora-insincere-questions-classification/discussion/80495)|[kernel](https://www.kaggle.com/wowfattie/3rd-place)|Guanshuo Xu|
|5th|5th Place Solution|[kernel](https://www.kaggle.com/jiangm/5th-place-solution)|padeof|
|7th|[7th Place Solution](https://www.kaggle.com/c/quora-insincere-questions-classification/discussion/80561)|kernel|yufuin|

## Overview
#### fork-of-bilstm-attention-kfold-clr-extra-features(with myself finetune).ipynb
* Private Score: `0.69825`
* Public Score: `0.69058`
* I trust my local f1-score rather than lb score, and the following tips only improve my local scores.
1. Use the mean average over three embeddings: `glove`, `wiki-news`, `paragram`
2. Use `pos_weight=0.78` in the BCELoss function to deal with the imbalance of sincere and insincere question numbers
3. Make the learning rate of the RNN layer equal to `0.25` times the fully connected layer
4. Use all `training` sets and `test` sets to fit tokenizer
5. Use the model checkpoint of the highest val-score to make prediction


####  fork-from-bilstm-attention-kfold-0115-81a8d9 (the public kernel score 0.700).ipynb
* Private Score: `0.70235`
* Public Score: `0.69729`
* I didn't change anything for the original 0.700 public kernel.