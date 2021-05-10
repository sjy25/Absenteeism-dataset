# Absenteeism-data


# Overview
Absenteeism refers to the failure to report for or remain at work as scheduled, regardless of the reason. This is usually unplanned e.g. sick leave, but can also be planned e.g. strike. While the occasional absence of an employee does not pose a problem,prolonged absenteeism can  especially when an employee doesn't show up to work unexpectedly for extended periods of time. Vahtera et. al (2001) found that 1 day sick leaves were more likely to be taken on Mondays and Fridays compared to other weekdays. Extended weekend absences were also more common in men, in young employees, and in those in lower socioeconomic classes.

Using a dataset from Brazil (https://archive.ics.uci.edu/ml/datasets/Absenteeism+at+work)on medical related absenteeism, this project comprises two parts namely:

(i) Exploratory data analysis 

-data was analyzed at two levels, namely at aggregated at the level of the individual (where possible), and at record level

-explored and visualized relationships between time absent,reasons for absence and factors such as Body Mass Index (BMI), day of the week

(ii) Machine learning model to predict time absent based on factors such as day of the week and BMI

-conducted data pre-processing, which included identifying outliers

-tested two models, namely linear regression and decision tree regressor

-evaluated the models using MAE and MAD scores 

-tuned the model using feature selection and improved MAE and MAD scores


## Dataset
The dataset comprises 740 records of health related absenteeism at work from July 2007 to July 2010 at a courier company in Brazil for 36 individual employees. The reasons for absenteeism were classified into 28 categories, taking reference from the International Code of Diseases (ICD) by the World Health Organization. The dataset also includes reasons for absenteeism not part of the international classification of diseases, such as medical follow-up, medical or dental consultation, physical examination and physiotherapy. 

The reasearch paper this data was collected for:

Martiniano, A., Ferreira, R. P., Sassi, R. J., & Affonso, C. (2012). Application of a neuro fuzzy network in prediction of absenteeism at work. In Information Systems and Technologies (CISTI), 7th Iberian Conference on (pp. 1-4).


================Legend for categories of absenteeism====================

ICD

1 Certain infectious and parasitic diseases  
2 Neoplasms  
3 Diseases of the blood and blood-forming organs and certain disorders involving the immune mechanism  
4 Endocrine, nutritional and metabolic diseases  
5 Mental and behavioural disorders  
6 Diseases of the nervous system  
7 Diseases of the eye and adnexa  
8 Diseases of the ear and mastoid process  
9 Diseases of the circulatory system  
10 Diseases of the respiratory system  
11 Diseases of the digestive system  
12 Diseases of the skin and subcutaneous tissue  
13 Diseases of the musculoskeletal system and connective tissue  
14 Diseases of the genitourinary system  
15 Pregnancy, childbirth and the puerperium  
16 Certain conditions originating in the perinatal period  
17 Congenital malformations, deformations and chromosomal abnormalities  
18 Symptoms, signs and abnormal clinical and laboratory findings, not elsewhere classified  
19 Injury, poisoning and certain other consequences of external causes  
20 External causes of morbidity and mortality  
21 Factors influencing health status and contact with health services.

Non ICD

22 Patient follow-up
23 medical consultation
24 blood donation 
25 laboratory examination
26 unjustified absence
27 physiotherapy
28 dental consultation

## Summary of results

-while some results of earlier studies were replicated (e.g. higher absenteeism among young people), the differences were not significant, likely due to a lack of statistical power associated with small sample size. 

-However, at the record level, a significant difference was found between time absent on monday vs tues, which is consistant with earlier studies

-a Power analysis conducted suggested that the mimimum sample size for each group should be around 64, in order  to see any possible significant difference between two groups. This will be useful to guide future studies. 

-between the two machine learning models, the decision tree regressor had lower MAE and MAD scores (after feature selection).

## Limitations and Future directions
Limitations include the small sample size (data from only 36 unique individuals), which could explain the lack of statistical power when data was analyzed at aggregated level 

A larger sample size should be used in future studies, with more unqiue individuals represented. this will also contribute to a more robust machine learning model. 

It will also be interesting to collect data to compare pre and post covid absenteeism. For example, one could investigate whether absenteeism for medical reasons was lower during the pandemic given people were working from home

