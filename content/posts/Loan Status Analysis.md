---
title: "Loan Status Analysis"
date: 2023-2-1T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["Random Forest", "Feature Engineering", 'Finance', 'Cross-Validation']
author: "Yueh-Huan, Ho"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: ""
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: /loan_status.jpg # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: ""
    Text: "test" # edit text
    appendFilePath: true # to append file path to Edit link
---
![Scenario 1: Across columns](/loan_status.jpg)


## Project Description
The main goal of this project is to identify and predict the loan status of lenders.   
To figure out whether the dataset has time series characteristic, two cross-validation methods (**K-fold, TimeSplit**) are also used.  
In this project, RandomForest is the main model to predict and analyze the loan status.  
*(The Dataset for model training includes 916567 rows and 10 columns from 2007 to 2017.)*
<br/><br/>
### Response Variable

* Loan_Stat -> Including 3 status, Fully Paid, Charged Off, and Default
<br/><br/>

### Explanatory Variables
* Annual_Inc -> Annual income  
* Emp_Length -> Employment length  
* Dti ->  The debt-to-income ratio of the borrower  
* Delinq_2yrs -> The number of times the borrower had been 30+ days past due on a payment in the past 2 years  
* Term -> Borrowing term  
* Grade -> History credit grading  
* Inq_Last_6mths -> The borrower’s number of inquiries by creditors in the last 6 months  
* Purpose -> Purpose for borrowing  

<br/><br/>

## Feature Engineering
### loan_stat  
Fully_Paid -> 0  
Defult, Charged-Off -> 1  
### Grade  
A, B, C, D, E, F, D -> 1, 2, 3, 4, 5, 6, 7  
### Purpose  
Debt_Consolidation -> 1  
Other -> 0 
<br/><br/>




```python
#getting dummies for loan_status
data_df['loan_status'] = data_df['loan_status'].str.replace('Charged Off', '1')
data_df['loan_status'] = data_df['loan_status'].str.replace('Default', '1')
data_df['loan_status'] = data_df['loan_status'].str.replace('Fully Paid', '0')

#getting dummies for purpose
data_df.loc[data_df['purpose'] != 'debt_consolidation', 'purpose'] = 0
data_df.loc[data_df['purpose'] == 'debt_consolidation', 'purpose'] = 1
```

<br/><br/>
<br/><br/>
## Cross-Validation
[**Cross-Validation**]![Scenario 1: Across columns](/kfold.jpg) <br/>
<br/>
___
This is a academic project supervised by [**Kao, Ming-Sung**](http://bba.fib.fju.edu.tw/index.php?action=teacher-detail&id=34/) from Fu Jen Catholic University. I'm very grateful to him for his enthusiastic and responsible supervision on the project.

