# TASK 1 Topic Extractor
## Overview
This code can be used to extract a topic on a document/article with supervised learning model. The workflow of each model is roughly divided in four parts: preprocessing, feature extraction, train a model, test a model and evaluate model.

## Dependencies
Topic Extractor:
1) Python 3.5
2) pandas=0.22.0
3) nltk 3.2.5
4) regex
5) codecs
6) preprocessor 1.2.3

## Input
to build topic extractor model takes a `.csv` document as input. Each line must consist of three columns: 

    Column 1) article_id: unique id of the article
    Column 2) article_topic: main topic of the article
    Column 3) article_content: content of the article

See `ds_asg_data.csv` for an example.

## How to run \& output

To run this topic extractor model, see the below example.

```
$ python task1Classification.py -h

Options:
h, --help      show this help message and exit

  Train Topic Extraction Model:
    Usage: task1Classification.py -f [YOURFILE] -m -e
    
    -f FILETRAIN  Dataset Location(file must be have article_content and
                  article_topic)
    -m            Train Model and Save Model to classificationTask1.Pikle
    -e            Evaluation Model

  Test Topic Extraction Model:
    Usage: task1Classification.py -d [YOURFILE] -t
    
    -d FILETEST   Dataset Location(file must be have article_content and
                  article_id)
    -t            Test To Predict Topic

```

So for Train Topic Extraction Model example :

```
$ python task1Classification.py -f ds_asg_data.csv -m -e

Preprocessing ............ 
Training Topic Model .......... 
Your Model Save To classificationTask1.pkl

Training Done ........
Evaluation Model ........... 
Topic Model Accuration = 88.48

```

So for Train Topic Extraction Model example :
```
$ python task1Classification.py -d test_article.csv -t

file test =  test_article.csv
Predict Topic ..........

Result for Topic Extraction Predict Saved to resultPredict/predictTestContent.csv.csv
Predict DONE ........ 

```
