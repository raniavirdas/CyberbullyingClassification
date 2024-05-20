# Predict Multi Cyberbullying Tweets
## Background
Twitter is an online social networking and microblogging service that allows its users to send and read text-based messages. However, many Twitter users use the social network to do bad things such as criticizing, racism, and even bullying others. 
This project aims to predict cyberbullying tweets using multiclassifier.
## Exploratory Data Analysis
1. What happened?
<p align="center">
    <img src="https://github.com/raniavirdas/CyberbullyingClassification/assets/91519107/fb42820f-8569-4a66-b75d-8d4a0f64e275" alt="what">
</p>
There are 6 types of cyberbullying with the same number of tweets
<p>
2. What words are often used in cyberbullying?
<p align="center">
    <img src="https://github.com/raniavirdas/CyberbullyingClassification/assets/91519107/aadb6f54-5125-4e52-811a-ac052c785756" alt="wordcloud fix">
</p>
Most of many users type in words like bully, school, muslim, girl, idiot, dumb, nigger, fuck when they cyberbully on twitter
<p>
3. What words are often used in gender & religion cyberbullying?

<p align="center">
    <img src="https://github.com/raniavirdas/CyberbullyingClassification/assets/91519107/7d5167fa-496f-4f3d-9d6e-af6e4f5471d3" alt="gender">
</p>

<p align="center">
    <img src="https://github.com/raniavirdas/CyberbullyingClassification/assets/91519107/2f6fef3c-4719-494b-ab27-849b998b91b6" alt="religion">
</p>

Most of many users type in words like joke, rape, and gay when they did gender cyberbully on twitter. Meanwhile, the word muslim is the word that is most often mentioned when Twitter users carry out religion cyberbullying
<p>

4. What words are often used in age & ethnic cyberbullying?

<p align="center">
    <img src="https://github.com/raniavirdas/CyberbullyingClassification/assets/91519107/527b1d20-41df-40f7-96b4-9d11fbe926ec" alt="age">
</p>

<p align="center">
    <img src="https://github.com/raniavirdas/CyberbullyingClassification/assets/91519107/f4495bcd-99bd-4839-9e35-714c3972edeb" alt="ethnic">
</p>

Users often tweet with ridicule in the form of bully and school when doing age cyberbullying. Meanwhile, when mocking certain ethnicities, tweeter users often use the words fuck, nigger, and dumb
<p></p>
5.  What words are often used in other & not cyberbullying?

<p align="center">
    <img src="https://github.com/raniavirdas/CyberbullyingClassification/assets/91519107/03ee7bb6-157e-44ae-b322-722d9b104aac" alt="other">
</p>

<p align="center">
    <img src="https://github.com/raniavirdas/CyberbullyingClassification/assets/91519107/12efbaf8-e10a-4ebc-af48-d38755df418e" alt="not bully">
</p>

Users who do not justify cyberbullying behavior tweet by including the word bully in the sentences they type. As well as for users who do cyberbullying with other categories. Not only that, the word fuck is also typed when other users are cyberbullying in other categories
## Pre-processing
I removed stopwords, case folding, stemming, and lemmatizer words as follows.
|tweet_text|cyberbullying_type|clean_tweet|
|:-|:-|:-|
|In other words #katandandre, your food was cra...|not_cyberbullying|word food crapilici|
## Features Engineering
I did TDIDF method on feature extraction
## Model Development & Evaluation
- Model: I use Logistic Regression, Support Vector Machine, and Multinomial Naïve Bayes classifier
- Evalualtion: I used a cv score with the best parameters and the result was that SVC produced the best performance with a cv score of 0.833 with a penalty parameter of the error term of 1
## Conclusion
The support vector machine is the best machine learning model for predicting cyberbullying tweets with 83% of accuracy. It has a weighted average precision percentage of 82%. Even so, the sensitivity obtained is 83%. It means that about 17% of positive cases missed the model's predictions


