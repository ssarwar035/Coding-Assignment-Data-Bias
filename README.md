# Coding-Assignment-Data-Bias

For this assignment, we are exploring the concept of bias through querying an existing natural language processing model called Perspective API. In this assignment, I compiled a list of my own comments, comments from Twitter, and some comments using ChatGPT. Using Perspective API, I will score the toxicity of each comment as anything higher than a score of 0.5 will be branded as toxic and anything lower will be branded as not toxic. The comments will be compared between the predicted toxicity and the actual toxicity. 

The CSV files includes 5 columns of data. The first column in the "Comments" data and it is the comments that were run through the Perspective API client. The second column is the "Score" column which is the score that was given to the comment by the API. The third and fourth columns of the table are the "Predicted Toxicity" and the "Actual Toxicity". The predicted toxicity was derived from the scores from the Perspective API. If the score was higher than .5 it was a toxic comment and if it was lower than .5 it was a non-toxic comment. The actual toxicity was labeled by human judgement. The final column is the "Sex" column which labels whether the comment was about a female or male.

##Hypothesis
I hypothesize that Perspective API will flag comments with obscenity as more toxic even if it is not a toxic comment than comments with no obscenity. Perspective API will also not be able to detect sarcasm as toxic. The Perspective API will also flag comments about females more than comments about males.

Below are the categories of my experiment.

1. Category 1: 6 examples of highly toxic sentences targeting the female gender
2. Category 2: 6 examples of normal non-toxic sentences targeting the female gender
3. Category 3: 6 examples of highly toxic targeting the male gender
4. Category 4: 6 examples of normal non-toxic sentences targeting the male gender

##Results:



