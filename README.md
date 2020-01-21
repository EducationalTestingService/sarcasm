# Automatic Sarcasm Detection 

Please refer to each of the following sub-directories for further references on datasets. 

For Twitter and Reddit, training and test datasets are provided for sarcasm detection tasks. For both datasets, the training data is provided in json format where each training utterance contains the following fields: 
- ***label*** : `SARCASM` or `NOT_SARCASM`
- ***response*** :  the sarcastic response, whether a sarcastic Tweet or a Reddit post
- ***context*** : the conversation context of the ***response***
	- Note, the context is an ordered list of dialogue, i.e., if the context contains three elements, `c1`, `c2`, `c3`, in that order, then `c2` is a reply to `c1` and `c3` is a reply to `c2`. Further, if the sarcastic response is `r`, then `r` is a reply to `c3`.

---
For instance, for the following example : 

`"label": "SARCASM", "response": "Did Kelly just call someone else messy? Baaaahaaahahahaha", "context": ["X is looking a First Lady should . #classact, "didn't think it was tailored enough it looked messy"]`

The response tweet, "Did Kelly..." is a reply to its immediate context "didn't think it was tailored..." which is a reply to "X is looking...". Your goal is to predict the label of the "response" while also using the context (i.e, the immediate or the full context).

- **Twitter** : constructed a data set of 5,000 English Tweets balanced between the `SARCASM` and `NOT_SARCASM` classes.
-  **Reddit** : it is a dataset of 4,400 Reddit posts balanced between the `SARCASM` and `NOT_SARCASM` classes.

The test data (for both Twitter and Reddit) will include only the `response` and the `context` but no label. Gold sarcasm labels will be released after the evaluation period. 

---
Note:  Since we have collected our training data from popular social media platforms a large portion of the utterances are on controversial and/or political and social topics. Although we have pre-processed the training data and lightly edited to remove contentious text, many utterances still contain controversial perspectives (of the users) and informal language.  


