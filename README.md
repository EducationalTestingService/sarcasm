# Automatic Sarcasm Detection 

***The Shared Task (2nd FigLang Workshop at ACL 2020) is now over. Thanks a lot, participants :)***  

Please refer to `reddit` and `twitter` sub-directories for further references on datasets. 

For Twitter and Reddit, training and testing datasets are provided for sarcasm detection tasks in jsonlines format. 

Each line contains a JSON object with the following fields : 
- ***label*** : `SARCASM` or `NOT_SARCASM`  
- ***id***:  String identifier for sample. This id will be required when making submissions.
	- **ONLY** in test data
- ***response*** :  the sarcastic response, whether a sarcastic Tweet or a Reddit post
- ***context*** : the conversation context of the ***response***
	- Note, the context is an ordered list of dialogue, i.e., if the context contains three elements, `c1`, `c2`, `c3`, in that order, then `c2` is a reply to `c1` and `c3` is a reply to `c2`. Further, if the sarcastic response is `r`, then `r` is a reply to `c3`.

For instance, for the following training example : 

`"label": "SARCASM", "response": "Did Kelly just call someone else messy? Baaaahaaahahahaha", "context": ["X is looking a First Lady should . #classact, "didn't think it was tailored enough it looked messy"]`

The response tweet, "Did Kelly..." is a reply to its immediate context "didn't think it was tailored..." which is a reply to "X is looking...". Your goal is to predict the label of the "response" while also using the context (i.e, the immediate or the full context).

***Dataset size statistics*** :

|         | Train | Test |
|---------|-------|------|
| Reddit  | 4400  | 1800 |
| Twitter | 5000  | 1800 |

For Test, we will be providing you the ***response*** and the ***context***. We will also provide the ***id*** (i.e., identifier) to report the the results.

***Submission Instructions*** : Please follow the given [link](submission_instructions.pdf)

***Main References:***

[A Report on the 2020 Sarcasm Detection Shared Task.](https://www.aclweb.org/anthology/2020.figlang-1.1.pdf) Debanjan Ghosh, Avijit Vajpyee, Smaranda Muresan. Proceedings of the Second Workshop on Figurative Language Processing.

---
***Note***:  Since we have collected our training data from popular social media platforms a large portion of the utterances are on controversial and/or political and social topics. Although we have pre-processed the training data and lightly edited to remove contentious text, many utterances still contain controversial perspectives (of the users) and informal language.  

