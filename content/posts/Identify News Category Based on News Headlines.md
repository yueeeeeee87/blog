---
title: "Identify News Category Based on News Headlines (NLP)"
date: 2023-4-29T11:30:03+00:00
# weight: 1
# aliases: ["/first"]
tags: ["NLP", "Transformers", "Bert", "HuggingFace"]
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: false
draft: false
hidemeta: true
comments: false
description: ""
canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: true
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
    image: /news_headline/cover.png # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: ""
    Text: "test" # edit text
    appendFilePath: true # to append file path to Edit link
---
## Project Description
This project focuses on fine-tune a distilbert model to predict news categories using only news headline.
For model demo and downloading the model, please check my HuggingFace Repo🤗. [HuggingFace Repository](https://huggingface.co/Yueh-Huan/news-category-classification-distilbert)


**<center>HuggingFace Demo</center>**![Scenario 1: Across columns](/news_headline/hugging_face.png)



## Data Description
The data is from [Kaggle](https://huggingface.co/Yueh-Huan/news-category-classification-distilbert).\
There are 200, 000 rows and 42 cotagories in our predict column.

## Model Training

**<center>Input preprocessing</center>**

To transform text data into vetors, I first applied TfidfVectorizer to preproess text data.
```python
tfidf = TfidfVectorizer(strip_accents=None,
                        lowercase=True,
                        preprocessor=None,  # applied preprocessor in Data Cleaning
                        tokenizer=word_tokenize,
                        use_idf=True,
                        norm='l2',
                        smooth_idf=True,
                        stop_words= 'english',
                        max_df=0.5,
                        sublinear_tf=True)
```

**<center>Model Loss History</center>**![Scenario 1: Across columns](/news_headline/loss_history.png)
**<center>Accuracy History</center>**![Scenario 1: Across columns](/news_headline/acc_history.png)

## Project Detail
Please refer to this PDF to check the project details.
[Project PDF](/news_headline/MGTA415_final_project.pdf)






For more details about the code of the project, please refer to my [GitHub Repository](https://github.com/yueeeeeee87/News_category_prediction)







