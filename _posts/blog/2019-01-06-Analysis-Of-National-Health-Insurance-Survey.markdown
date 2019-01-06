---
layout: post
title:  "Analysis of National Health Insurance Survey"
date:   2019-01-06 03:00:00
categories: blog
---

##### What is NHIS?

The National Health Interview Survey (NHIS) is a yearly cross-sectional household interview
survey conducted by the Centers for Disease Control and Prevention’s National Center for
Health Statistics. Data is collected from a selected sample of households in US by conducting
face to face interviews. The survey contains data related to demographics, health status and
limitations, injuries, health care access and utilization, health insurance, income and assets.
The survey contains data related to demographics, health status and
limitations, injuries, health care access and utilization, health insurance, income and assets.
The data set contains responses from seven questionnaires corresponding to household, family,
child, injury and disability data.

##### Our Goals:

As a team we wanted to explore the following aspects of the data set:

1 Compare the mental health of individuals who practice meditation and other relaxation
  techniques

2. Identify factors affecting sleep quality among the participants.

3.Analysis of health care and affordability of eye glasses and dental care.

4. Consider the scenario where a business owner wants to explore the data but he/she relies on people with programming skills to help      answer important questions. A more intuitive approach would be for the owner to ask what he/she wants as a text query to a bot and      get all the visualizations. In this project, we have exposed the NHIS dataset via a conversational bot and suggest frameworks by        which this could be generalized for any dataset.

##### Methods:

Based on initial exploratory data analysis , we as a team decided to form certain surrogate variables to quantify our findings.

1. For meditation and relaxation techniques :
    <div class ="honeycombpic">
<img src="https://github.com/parihardeepanshu/parihardeepanshu.github.io/blob/master/assets/img/nhis-yoga.png?raw=true"/>
</div> 

2. For sleep quality:
   <div class ="honeycombpic">
<img src="https://github.com/parihardeepanshu/parihardeepanshu.github.io/blob/master/assets/img/nhis-sleep.png?raw=true"/>
</div>

3. For affordability:
   
   Based on the survey responses, we came across certain measures to detect affordability of dental care and eyeglasses. So we defined a    new feature called affordability which could represent the affordability of the two responses as one . This feature has values 0,1 or    2 based on the person's ability to afford neither , one or both of eyeglasses and dental care. Then, we narrowed the number of          factors affecting affordability by going through the code book and filtering out columns related to vision and dental care for          building the model. As the classes we were trying to predict were more than two, we tried a multinomial logistic regression algorithm    to fit a model based on certain explanatory variables.

##### Results:

Some interesting results were :

1.The negative emotion score was plotted against yoga and meditation separately to analyze the distribution of frequencies of emotion     scores in each of these categories. It was observed that more participants had higher psychological distress level in the non-yoga
  and non-meditation participating groups.
  
2.The chi square test between the frequency of feelings reported vs meditation and yoga (separate), returned a very low p-value,           confirming that they are related.

3.Only 62% of the United States population sleeps healthy amount of hours on average. i.e. between 7 and 9 hours.

4.The Sleepscore devised using the sleep information was plotted with other variables in the dataset giving interesting results about     the correlation between them. For example,
 (a)Factors such as marital status was correlated with the sleep score. People who were married had a better sleep score than people who     were either divorced, widowed or separated.
 (b)There was no correlation between smoking or alcohol habits and the sleep score.
 (c)We found correlation between the citizenship status of an individual and his/her sleep score.
 
5.Private plans were the most used among all health care insurance plans.In those plans PPO (employer -provided health insurance) plans dominated all others.

6.The people under PPO plans were not confident in their ability to find affordable healthcare plans on their own.

7.High costs and loss of job/change of employers were the leading factors for being uninsured
in the past year.

More interesting plots and observations can be found in our ppt [click][link1] and project report. [click][link2]

[link1]:https://github.com/parihardeepanshu/nhis5110/blob/master/NHIS_Presentation.pptx
[link2]:https://github.com/parihardeepanshu/nhis5110/blob/master/NHIS_Report.pdf

##### Code:

Git Link [click][link3]

[link3]:https://github.com/parihardeepanshu/nhis5110
