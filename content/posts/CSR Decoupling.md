---
title: "The Effect of CSR Decoupling on Corporations' Financial Performance"
date: 2023-1-24T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["CSR", "Feature Engineering", 'Finance']
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
    image: /CSR_cover.jpg # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: ""
    Text: "test" # edit text
    appendFilePath: true # to append file path to Edit link
---
## Abstract
This research project mainly focuses on identifying the CSR decoupling behavior for the multi-international firms and utilizing the decoupling indicators to find if there is a relationship between firms' CSR decoupling and financial indicators. 


## Data Sources
The sample used in this study is composed of listed and OTC companies in Taiwan. The data sources include: 
1. **Company performance indicator**s and **operating profiles** of related companies are obtained from the Taiwan Economic Journal (TEJ) database. 
<br/><br/> 
2. **The national CSR scores** are obtained from the Sustainable Development Report, published from 2017 to 2019, which rates the SDG scores of UN member countries each year. The higher the score, the better the country's implementation of SDGs. 
<br/><br/> 
3. **Company CSR scores** are obtained from Refinitiv ESG score, which contains the SDG implementation scores of each company from 2017 to 2019. A score of 0 indicates that the company did not disclose its SDG performance, while a score above 0 indicates the level of the company's SDG implementation. The higher the score, the higher the level of implementation.\
<br/><br/> 
Finally, based on the company name and year, the above data are integrated for subsequent empirical analysis in this study
<br/><br/>

## Response Variable
* **Tobin's Q**

This study uses Tobin's Q as a measure of corporate value. In order to examine how the market reacts to CSR decoupling and how CSR decoupling affects corporate value, this study takes the previous year's Tobin's Q of a company as a lagging variable to measure the relationship between the two.

## Explanatory Variables
* **CSR decoupling score**

When there is a discrepancy between the CSR information disclosed by a company and its actual actions, CSR decoupling occurs. To measure the extent of CSR decoupling in companies, this study rates them on their performance in the Sustainable Development Goals (SDGs). The SDGs consist of seventeen major objectives, and when a company does not disclose information related to a specific objective, we give it a score of zero. If a company discloses information but takes no action on an SDG, we give it a score of one. If a company takes action on an SDG, we give it a score of two to five based on the degree of implementation. To measure the extent of CSR decoupling, this study adds up the scores of the objectives with a score greater than one and divides it by the number of objectives with a score greater than one. The lower the score, the higher the extent of CSR decoupling in the company's CSR report, which means that the company has only disclosed information without actually implementing it. However, objectives with a score of zero are not included in the measurement of CSR decoupling.


<br/><br/> 
<br/><br/> 
[**Project's Flowchart**]![Scenario 1: Across columns](/flow.jpeg) <br/>
<br/> 

For more details about the code and the structure of this research project, please refer to my [GitHub Repository](https://github.com/yueeeeeee87/CSR_decoupling)
___
This is a research project supervised by [**Kao, Ming-Sung**](http://bba.fib.fju.edu.tw/index.php?action=teacher-detail&id=34/) from Fu Jen Catholic University. I'm very grateful to him for his enthusiastic and responsible supervision on the project.







