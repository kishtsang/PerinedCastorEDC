![alt text](https://github.com/kishtsang/PerinedCastorEDC/blob/main/Perined%20Birthweight%20Chart%20Logo.png)
# Perined Birthweight Charts for CastorEDC

## Introduction
Fetal growth restriction (FGR) is defined as a condition in which the foetus fails to meet its biologically based growth potential. The aetiology of FGR is variable and can be based on maternal, foetal, placental and genetic factors. Foetuses with FGR are at a higher risk of perinatal  morbidity and is the second most common cause of perinatal mortality. Additionally, long-term consequences associated with FGR include neurodevelopment disorders, cardiovascular and endocrinological diseases.

FGR composes a major global health challenge, affecting nearly 10 percent of all pregnancies and expectations are that this number will be rising further due to the increasing number of infertility treatments, environmental factors and advancing maternal age. Although the impact and consequences of FGR are well understood, FGR is still poorly defined. Therefore, small-for-gestional-age (SGA) is often used as a proxy to identify infants at risk. Although, SGA and FGR are often used interchangeably, they are conceptually different. 

SGA is commonly defined as birthweight below the sex specific 10th percentile of gestational age (GA). For this, reference values are required. In The Netherlands, a prescriptive birthweight chart has been developed by Hoftiezer et al. and has replaced the former descriptive Dutch birthweight population reference. Prescriptive birthweight charts may be beneficial in the identification of infants born SGA and at risk of neonatal and long-term morbidity as was demonstrated in two other studies of this group.

The use of the Dutch birthweight charts have predominantly be focused on clinical use. The Perined organisation has released a mobile application for healthcare professionals to rapidly determine birthweight percentiles according to the charts. In research, however, the use of such an app to determine percentiles in study populations can be cumbersome. Therefore, integration of birthweight charts in commonly used electronic case report forms (eCRFs) may benefit clinical research using these charts. 

Since the Dutch Birthweigth Charts released by Perined depends on three distinct variables: Sex, Gestational Age and Birthweight, a  calculation can be performed to determine the percentile ranges by using conditional statements, comparison and logical operators. For this, cut-off values from the Perined Birthweight charts are used. This code was developed by Kishan Tsang to optimize the use of birthweight charts within perinatal research. By directly implementing birthweight data into the eCRF, identification, management and statistic analysis can be easily optimized for SGA children. This code can be used as an example for other birthweight charts.

## How to use
The code is written for the use within the calculation forms offered by CastorEDC. Unfortunately, CastorEDC only allows a limited amount of 65535 (2^16) characters in this field. Therefore, the chart has been split based on sex. In CastorEDC, a dependency can be added to this calculation so that male patients will only be analyzed within the male chart and vice versa. I have written a "how to" on how to use this calculation in your CastorEDC study.

### Gestational age 
Usually, gestational age is provided in completed weeks and days (e.g. 36+5). For this calculation, however, completed days are used. The easiest way is to use a simple calculation within CastorEDC to calculate your gestational age in days. If you have two distinct variables for weeks and days, this can easily be combined using the: GA_weeks_to_days calculation form provided here.

### Variables
Variables can be recognised by the use of Curly Brackets { }. Since you will probably not use the same variables as mentioned in the code provided here, you will have to change this in order to use the calculation form within your study. I advise to use a powerful text editor such as Sublime Text to find and replace the variables using the Find and Replace All functionality.

### Dependencies


## Other Uses
The functionality of this code can easily be recreated for other birthweight charts

## Terms and Conditions

## License
