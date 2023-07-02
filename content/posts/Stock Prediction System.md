---
title: "Stock Prediction System with Telegram Bot 🤖"
date: 2023-1-24T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["Finance", "Machine Learning", "Telegram API", "SQL"]
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: true
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
    image: /stock_pred/pic.png # image path/url
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
Our topic focuses on constructing a stock forecasting system. This system can
provide the user with the basic information of stock, stock price prediction, K-line chart,
and the individual stock news. In the prediction aspect, our system uses four machine
learning models, including Random Forest, XGBoost, LightGBM, and LSTM. To train
our machine models, we use 250 different technical indicators as the variables and
inputs. In order to make our model become better and more precise, we also used Shap
and Skater the observe the reasoning process of the machine learning and improved our
models by analyzing observation and changing parameters. We evaluate our models by
examing the precision and recall rate and found that LightGBM has the best precision
and recall rate.
 In addition, in the field of data processing, this study uses the network crawler to
extract the share price of listed cabinet companies and combined with MySql access to
individual stock data. Finally, we created a Telegram Bot to present our results to users.
Users of our bot can enter several commands to our bot and our bot will read the
information and return the result to users.

## System Flow Chart
This chart demonstrates the basic flow of our system.
**<center></center>**![Scenario 1: Across columns](/stock_pred/flowchart.png) <br/>

<br/>

## Applicatoin Flow Chart
This chart demonstrates the basic flow of our application for Telegram bot and output.
**<center></center>**![Scenario 1: Across columns](/stock_pred/appflow.png) <br/>

<br/>

## Telegram Bot Demo 🤖
<div style="display: flex; justify-content: center; align-items: center;">
    <img src=/stock_pred/demo1.png alt= “” width="500" height="800">
</div>
<div style="display: flex; justify-content: center; align-items: center;">
    <img src=/stock_pred/demo2.png alt= “” width="500" height="800">
</div>
<div style="display: flex; justify-content: center; align-items: center;">
    <img src=/stock_pred/demo3.png alt= “” width="500" height="800">
</div>
<br/><br/> 
<br/><br/> 
<br/> 

For more details about the code and the structure of this research project, please refer to my [GitHub Repository](https://github.com/yueeeeeee87/Stock_Prediction_System)
___
This is a project supervised by [**Kao, Ming-Sung**](http://bba.fib.fju.edu.tw/index.php?action=teacher-detail&id=34/) from Fu Jen Catholic University. I'm very grateful to him for his enthusiastic and responsible supervision on the project.







