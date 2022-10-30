![alt text](https://github.com/kishtsang/PerinedCastorEDC/blob/main/Perined%20Birthweight%20Chart%20Logo.png)
# Perined Birthweight Charts for CastorEDC
Developed by Kishan Tsang

## Introduction
Fetal growth restriction (FGR) is defined as a condition in which the foetus fails to meet its biologically based growth potential. The aetiology of FGR is variable and can be based on maternal, foetal, placental and genetic factors. Foetuses with FGR are at a higher risk of perinatal  morbidity and is the second most common cause of perinatal mortality. Additionally, long-term consequences associated with FGR include neurodevelopment disorders, cardiovascular and endocrinological diseases.

FGR composes a major global health challenge, affecting nearly 10 percent of all pregnancies and expectations are that this number will be rising further due to the increasing number of infertility treatments, environmental factors and advancing maternal age. Although the impact and consequences of FGR are well understood, FGR is still poorly defined. Therefore, small-for-gestional-age (SGA) is often used as a proxy to identify infants at risk. Although, SGA and FGR are often used interchangeably, they are conceptually different. 

SGA is commonly defined as birthweight below the sex specific 10th percentile of gestational age (GA). For this, reference values are required. In The Netherlands, a prescriptive birthweight chart has been developed by [Hoftiezer et al.](https://pubmed.ncbi.nlm.nih.gov/30576661/) and has replaced the former descriptive Dutch birthweight population reference. Prescriptive birthweight charts may be beneficial in the identification of infants born SGA and at risk of neonatal and long-term morbidity as was demonstrated in two other studies of this group. In the Netherlands, the Birthweight charts are provided by [Perined](https://www.perined.nl).

The use of the Dutch birthweight charts have predominantly be focused on clinical use. Perined has released a mobile application for healthcare professionals to rapidly determine birthweight percentiles according to the charts. In research, however, the use of such an app to determine percentiles in study populations can be cumbersome. Therefore, integration of birthweight charts in commonly used electronic case report forms (eCRFs) may benefit clinical research using these charts. 

Since the Dutch Birthweigth Charts released by Perined depends on three distinct variables: Sex, Gestational Age and Birthweight, a  calculation can be performed to determine the percentile ranges by using conditional statements, comparison and logical operators. For this, cut-off values from the Perined Birthweight charts are used.

## How To
The code is written for the use within the calculation forms offered by CastorEDC. Unfortunately, CastorEDC only allows a limited amount of 65535 (2^16) characters in this field. Therefore, the chart has been split based on sex. In CastorEDC, a dependency can be added to this calculation so that male patients will only be analyzed within the male chart and vice versa. Please follow this How To guide!

### Start - Gestational age 
In general, gestational age is provided in completed weeks and days (e.g. 36+5). For this calculation, however, completed days are used. The easiest way is to use a simple calculation within CastorEDC to calculate your gestational age in days. In this example, I have created two variables for completed weeks and days and combine them using the following calculation to obtain total days. 

```
VAR_GA_DAYS = ({pregnancydurationweeks} * 7) + ({pregnancydurationdays});
```

### Variables
The variables used in the calculation are:

Gestational Age in days
```
VAR_GA_DAYS
```
Birthweight in grams
```
VAR_BIRTHWEIGHT
```

Variables can be recognised by the use of Curly Brackets { }. Since you will probably not use the same variables as mentioned in the code provided here, you will have to change this in order to use the calculation form within your study. I advise to use a text editor such as Sublime Text to find and replace the variables using the "Find" and "Replace All" functionality. 

![alt text]()

### Using the Calculation
Simply copy the Male or Female code from this page to your desired text editor. Replace your variable names accordingly and copy the code in the Calculation template field. Don't click "Save" yet, as we have to build our dependencies.

### Dependencies
Next, since the code is split. A dependency must be added to only execute the calculation for the correct sex. Navigate to dependencies, mark field is dependent on "Yes" and add the correct variable and sex for the code. Before clicking, "Save" make sure that the sex matches your calculation as this can be a major point of fuck up. If you are sure, then click "Save".

The calculation field will automatically check if the provided variables are being used in your study. If not, you will receive a notification. If you receive such a notification, go back to your code and make sure that you have spelled all of the used variables right.

Repeat the steps above for the other sex. 


## Other Uses
The functionality of this code can easily be recreated for other birthweight charts by replacing the cut-off values of the percentiles. Additionally, several other factors as multiparity, ethnicity and type of delivery can be implemented as this is still commonly used in several different birthweight charts in the world. As this code is written in JavaScript, this data can easily be implemented in apps and websites to provide similar functionality for clinical use. In the case of using this code as a template, inspiration or otherwise , please refer to this Github as the original source.

## License
   GNU GENERAL PUBLIC LICENSE
