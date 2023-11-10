# Coding-Assignment-Data-Bias

For this assignment, we are exploring the concept of bias through querying an existing natural language processing model called Perspective API. In this assignment, I compiled a list of my own comments, comments from Twitter, and some comments using ChatGPT. Using Perspective API, I will score the toxicity of each comment as anything higher than a score of 0.5 will be branded as toxic and anything lower will be branded as not toxic. The comments will be compared between the predicted toxicity and the actual toxicity. 

The CSV files include 5 columns of data. The first column is the "Comments" which are the comments that were run through the Perspective API client. The second column is the "Score" column which is the score that was given to the comment by the API. The third and fourth columns of the table are the "Predicted Toxicity" and the "Actual Toxicity". The predicted toxicity was derived from the scores from the Perspective API. If the score was higher than .5 it was a toxic comment and if it was lower than .5 it was a non-toxic comment. The actual toxicity was labeled by human judgment. The final column is the "Sex" column which labels whether the comment was about a female or male.

## **Hypothesis**

I hypothesize that Perspective API will flag comments with profanity as more toxic even if it is not a toxic comment than comments with no profanity. Perspective API will also not be able to detect sarcasm as toxic. The Perspective API will also flag comments as toxic about females more than comments about males.

## **Results:**

Below are the categories of my experiment.

1. Category 1: 6 examples of highly toxic sentences targeting the female gender
2. Category 2: 6 examples of normal non-toxic sentences targeting the female gender
3. Category 3: 6 examples of highly toxic targeting the male gender
4. Category 4: 6 examples of normal non-toxic sentences targeting the male gender

These are the outcomes:

1. Category 1: 2 out of 6 examples were correctly predicted as toxic. (i.e., predicted label ==actual label == "toxic")
2. Category 2: 4 out of 6 examples were correctly predicted as non-toxic.
3. Category 3: 3 out of 6 examples were correctly predicted as toxic.
4. Category 4: 4 out of 6 examples were correctly predicted as non-toxic.

Below are the percentages of accuracies:

1. Class 1 accuracy for Toxic Female Comments = 0.5
2. Class 2 accuracy for Non-Toxic Female Comments = 0.6666666666666666
3. Class 3 accuracy for Toxic Male Comments = 0.3333333333333333
4. Class 4 accuracy for Non-Toxic Male Comments = 0.6666666666666666

The model demonstrates better accuracy in predicting non-toxic comments for both female and male categories, with 66.67% accuracy for non-toxic female comments and non-toxic male comments. However, the accuracy drops to 50% for toxic female comments and 33.33% for toxic male comments. This discrepancy in predicting toxic comments, particularly for males, highlights potential challenges in the model's ability to discern toxicity accurately across gender categories. While the model exhibits limitations in predicting toxicity for both genders, the lower accuracy in identifying toxic male comments suggests a potential gender-related bias. 

My hypotheses were correct in that comments with profanity were always flagged as toxic comments even if they were not toxic and simply praising someone. Moreover, my hypothesis that comments about women would be flagged as toxic more than men was also correct as the API flagged 5/12 female comments as toxic while flagging only 4/12 comments for males. This raises questions about the underlying biases in the model's training data. It prompts consideration of whether societal biases and stereotypes about gender are unintentionally embedded in the model, potentially perpetuating or amplifying existing biases present in the data. The API was not able to detect any bit of toxicity from sarcastic comments maybe because the API cannot pick up contextual cues or subtle linguistic changes, but rather bases it on certain words and phrases used. 

Some things that I found interesting were that the API is able to detect profane language even when it is censored with asterisks. However, the toxicity score changes based on how many asterisks are put and how many letters are written. For example, in my experiment, I used the word "bitch" and "b****". Obviously, the whole spelled-out word was more toxic than the censored one. But when I implemented the word "bit**" including the "i" and "t", the score was even lower than when the whole word was censored aside from the first letter. This was interesting to me and made me wonder how the model was trained to give results like this. 

## Questions

1. How was the Perspective API trained, and what steps were taken to assess and mitigate biases during the training process?
2. To what extent does the model consider cultural nuances and variations in language when making toxicity predictions?
3. What steps can be taken to align the model's performance with principles of equal opportunity and fairness in content moderation?










