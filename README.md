# Mask-Wearing Prediction Project
#### Usage details
- It is important to use the data and code that is provided without altering it for the code to run seamlessly.

### Texas A&M Mask-Wearing Attitudes Survey Dataset

## Overview

The Texas A&M Mask-Wearing Attitudes Survey Dataset provides insights into the attitudes and behaviors of Texas A&M University students regarding mask wearing during the early stages of the COVID-19 pandemic. The dataset comprises responses from a comprehensive survey designed to measure various aspects of mask wearing, including perceived benefits and risks, social norms, perceived behaviors of others, and the presence of choice in wearing masks.

## Dataset Details

- **Survey Questions**: The dataset contains responses to 155 questions, each addressing specific aspects of mask wearing. The second row in the data file includes the detailed question statement and response options provided in the survey.
- **Output Variable**: The primary output variable is derived from the question: "How often do you wear a mask around people who do not live in your home?" Responses range from "Never" (1) to "Always" (5), providing insights into individuals' mask-wearing frequency.
- **Data Size**: The training data comprises responses from 479 individuals, while an additional 100 individuals are included in the test data for model evaluation.

## Purpose

This dataset serves as a valuable resource for understanding the factors influencing mask-wearing behavior among college students, particularly in the context of the COVID-19 pandemic. By analyzing the survey responses and building predictive models, researchers can gain insights into the determinants of mask-wearing frequency and develop strategies to promote and encourage responsible mask-wearing practices among the student population.

## Potential Applications

- **Public Health Interventions**: Insights from this dataset can inform the development of targeted public health campaigns aimed at promoting mask wearing and increasing adherence to recommended guidelines.
- **Policy Decisions**: Policymakers can use the findings from this dataset to implement evidence-based policies and interventions to improve mask-wearing behavior within the university community.
- **Research**: Researchers can leverage this dataset to explore the relationship between various psychosocial factors and mask-wearing behavior, contributing to the broader understanding of health behavior during pandemics.

**Data**


![Covid Data Distribution](https://github.com/Sidhartht1607/Covidmask_wearing_prediction/blob/main/Untitled.png?raw=true)


## Results


We have used three models: Forward Selection, Bagging, and LDA. Forward Selection and Bagging are regression models we cannot directly compare to a classification model such as LDA. In Regression models, we mainly use the Test Mean Squared Errors to compare the models between them and for classification we calculate the misclassification rate (We have still provided test MSE for LDA). So, to compare we have used a heatmap to assess the predicted values. 

![Results](https://github.com/Sidhartht1607/Covidmask_wearing_prediction/blob/main/covid%20results.PNG?raw=true)

When comparing models using Test MSE as a metric, Bagging has the lowest score of 0.588, while LDA and Forward Selection follow closely with Test MSE scores of 0.63 and 0.637 respectively. It's worth noting that LDA is a classification model, so we can measure its performance in terms of misclassification rate, which in this case is 43%. Forward

Selection, on the other hand, provides an Adj. R2 score. The Heatmap shows the predicted values for different models, which we can compare to the true test data response
variable (y_test).

However, the Heatmap ranges from 0 to 5, which means that none of the true response values in y_test can be below 1 since y_test ranges from 1 to 5. This constraint does not apply to the regression models, which can predict values ranging from 0 to 5 and can also produce float values. However, this does not apply to LDA, as it only predicts the class.
