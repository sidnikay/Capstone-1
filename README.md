
# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Final Project: COVID Predictability

### Problem Statement
Predicting COVID-19 test results could be easy, with a simple questionnaire. Just asking a patient a few poignant questions could save the hospitals millions of dollars. We at InfoMedics, are attempting to devise a method that could do such that. With our questionnaire, we try to predict whether or not a person will have a positive or negative test from a few simple questions.

---
### Background Research
A virus was found on December 31, 2018, in Wuhan, China by the World Health Organization as known as WHO. By January 9, 2019, it was determined to be the novel coronavirus. Within thirty days of it being found, Wuhan, China goes under quarantine. The virus was named COVID-19 on February 11. Due to our ability to travel country to country swiftly, the virus spread rapidly to other countries. By March 11, WHO declares a pandemic. California becomes the first state in the United States to issue a Stay-at-Home order on March 18 causing other states to follow suit quickly after. The coronavirus has taken over 2.13 million people's lives worldwide, with no end in sight.

---
### Datasets Used

*['df_clean'](../data/df_clean.csv)

---

### Analysis Summary
The initial DataFrame had 93,995 rows of data and 46 columns, unfortunately, there was a lot of missing data. So after data cleaning and feature engineering, I end up with 73,339 rows of data and 55 columns.

['Ages in the DataFrame']('https://public.tableau.com/profile/sidni.johnson#!/vizhome/AgesintheDataFrame/AgesintheDataFrame?publish=yes')



['COVID Test Results by Ages']('https://public.tableau.com/views/COVID19resultsbyage/COVID19resultsbyBinnedAges?:language=en&:display_count=y&publish=yes&:origin=viz_share_link')


Since I am working with a Neural Network, I turned all of my object datatypes into 1s and 0s. With using real-life data, people tend to run into imbalanced classes and this DataFrame was no different. My company is testing patients based off a questionnaire, information such as swab type and type of test are not pertinent to our model. I am testing for a positive or negative COVID test, so I checked the baseline score before starting my model. I had 0.9820 0s(Negative) and 0.018 1s(Positive).

I ran 3 Neural Networks with different parameters: Undersampling, Oversampling, and SMOTE. These different parameters are very useful when dealing with imbalanced classes. Undersampling is when you remove data from the majority class in order to balance the classes. Oversampling is generating new samples of the under-represented class. While SMOTE is Oversampling, but it creates synthetic samples from the minority class.

I am measuring the Neural Networks by accuracy, recall, and precision. Accuracy calculates the correctly predicted observations over the total observations. Recall calculates the correctly predicted positive observations to the all observations in actual class - yes. Precision calculates the correctly predicted positive observations to the total predicted positive observations.

![Figure 1]()

Based off the scores, I went with Oversampling. Even though accuracy scores was the lowest of the three, the recall score was the best. Ultimately, being able to predict the positive scores is most import in medical data. 

---

### Conclusions & Considerations
Coronavirus has hit the world very hard
InfoMedics is attempting to use a simple questionnaire to prescreen patients. With this information, we are trying to eliminate the need for tests. Oversampling the data has worked best for neural networks. Since we used a neural network there is not much interpretability. I would like to create an interactive questionnaire that runs a neural network in the background, so that within a few seconds you knew whether you should quarantine without taking a psychical test.

---

### Sources Cited:
*
*
*
*
