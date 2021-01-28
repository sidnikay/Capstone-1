
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


This correlation graph shows that no column is highly correlated to the COVID19 Test Results.
!['Figure 2'](https://github.com/sidnikay/Capstone-1/blob/master/Images/Figure%202.png)



I separated the ages into bins. From what the news has informed us, the elderly generation is the the most affected. However, this data has more people between the ages of 21-40.
['Ages in the DataFrame'](https://public.tableau.com/profile/sidni.johnson#!/vizhome/AgesintheDataFrame/AgesintheDataFrame?publish=yes)



This graph shows the relationship between COVID19 Test Results and the Aged Binns. Since the DataFrame has more data between the ages of 21-40, we would expect more COVID cases in those ages.
['COVID Test Results by Ages'](https://public.tableau.com/views/COVID19resultsbyage/COVID19resultsbyBinnedAges?:language=en&:display_count=y&publish=yes&:origin=viz_share_link)



This chart is demonstrating the overlapping commonalities of symptoms.
['COVID Symptoms that Overlap'](https://public.tableau.com/profile/sidni.johnson#!/vizhome/ColumnsOverlap/COVIDSymptomsthatOverlap?publish=yes)

 With using real-life data, people tend to run into imbalanced classes and this DataFrame was no different. I removed all data that was swab type and test type because it is not pertinent to our model. Before running my Neural Network, I checked the baseline score, which is 0.9820.

I ran 3 Neural Networks with different parameters: Undersampling, Oversampling, and SMOTE. These different parameters are very useful when dealing with imbalanced classes. Undersampling is when you remove data from the majority class in order to balance the classes. Oversampling is generating new samples of the under-represented class. While SMOTE is Oversampling, but it creates synthetic samples from the minority class.

I am measuring the Neural Networks by accuracy, recall, and precision. Accuracy calculates the correctly predicted observations over the total observations. Recall calculates the percentage of total relevant results correctly classified. Precision calculates the percentage of your results which are relevant.

![Figure 1](https://github.com/sidnikay/Capstone-1/blob/master/Images/Figure%201.png)

Based off the scores, I went with Oversampling. Even though accuracy scores was the lowest of the three, the recall score was the best. Ultimately, being able to predict the positive classified scores is most import in medical data.

---

### Conclusions & Considerations
Coronavirus has hit the world very hard. With a vaccine now being distributed, there is hope insight. We received the best results when running our Neural Network by using the Oversampling technique. For Future steps, InfoMedics would like to create an interactive questionnaire that runs a neural network in the background, so that within a few seconds you knew whether you should quarantine without taking a psychical test. We would also like to discover a balanced relationship between accuracy and recall.

---

### Sources Cited:
*[World Health Organization]https://www.who.int/emergencies/diseases/novel-coronavirus-2019/interactive-timeline?gclid=CjwKCAiA9bmABhBbEiwASb35V5XzjGvljqGnIyw1lFlpEkUKDMhM_8bsjNQRw_ZHYMEzy3gTfx74RBoCCAcQAvD_BwE#event-91
*[COVID Timeline]https://www.ajmc.com/view/a-timeline-of-covid19-developments-in-2020
*[Google COVID Results]https://www.google.com/search?sxsrf=ALeKk030EXaNzMLm7c6W4mDmQm9WuWFFZA%3A1611589252796&ei=hOYOYPiUMISu5wLyxpOYCQ&q=total+deaths+from+covid+19+worldwide&oq=total+deaths+worldwide&gs_lcp=CgZwc3ktYWIQARgAMgYIABAHEB4yBggAEAcQHjICCAAyAggAMgYIABAHEB4yBggAEAcQHjICCAAyAggAMgYIABAHEB4yAggAOgQIABBHOgQIABANUNMeWMolYI8yaABwAngAgAFZiAGWAZIBATKYAQCgAQGqAQdnd3Mtd2l6yAEEwAEB&sclient=psy-ab
*[Metrics]https://blog.exsilio.com/all/accuracy-precision-recall-f1-score-interpretation-of-performance-measures/#:~:text=80%25%20accurate.&text=Precision%20%2D%20Precision%20is%20the%20ratio,the%20total%20predicted%20positive%20observations.&text=F1%20score%20%2D%20F1%20Score%20is,and%20false%20negatives%20into%20account
