---
<!-- layout: archive -->
title: ""
permalink: /test-page/
author_profile: true
---

This post is about our new line of project(s) that aims to automate data preparation (prep) for ML. I'm presenting a workshop [paper](https://adalabucsd.github.io/papers/2019_DataPrepZoo_DEEM.pdf) at DEEM, SIGMOD 2019 titled *The ML Data Prep Zoo: Towards Semi-Automatic Data Preparation for ML*. It is co-authored with my advisor, Arun Kumar.


Introduction
============================

Data preparation (prep) still remains a major bottleneck for building any real-world ML application. Several surveys of data science practioners have shown that the time spent in data prep can go as high as 80% of their time. Cloud companies have released AutoML platforms such as Google's AutoML Tables and Salesforce's Einstein that automates the entire ML pipeline, everything from preparing the data, selecting the right features and ML algorithms to tuning the knobs of these algorithms. Unfortunaltely, there does not exist any benchmarks to quantify the goodness of automation for data prep in the AutoML platforms. This would require formalizing the major data prep steps and create benchmark labeled datasets to standardize their evaluation on AutoML platforms. 

<img src="/imgs/automl.png" width="800" alt="error">

In this line of project(s), we aim to objectively quantify the key data prep taks by creating a commmon understanding of the data prep taks, understand why exactly these tasks are hard to automate, and create benchmark labeled datasets for them. Our focus is on relational data. Such datasets are typically stored with DB schemas in relational database management systems or as CSV or JSON files. A typical data prep workflow is shown below.


<p style="text-align:center;">
<img src="/imgs/task_steps.png" width="800" alt="error">
</p>


Case Study: ML Feature Type Inference
============================
The very first data prep step is to infer the ML feature types from the DB schema. For instance, age is numeric feature and zipcode is categorical. Attributes such as time since and income has numbers embedded in them, which requires some form of extraction in order to be useful as a feature.  This task is hard to be automated because there exist semantic gap between the db schema and the ml schema. The DB schema is syntactic: it tells us the data type of a column such as integer, real, or string. On the other hand, the ML schema is semanticL it tells us what type of a feature a column is. For instance, ZipCodes are usually stored as integers, but it is a categorical feature. However, A synatic tool like Python Pandas will thus treat it as a numeric feature, which can lead to non-sensical results.
<img src="/imgs/semantic_gap.png" width="800" alt="error"> To bridge this semantic gap, we cast this data prep task as an ml classification problem. In order to do, we need the following 4 things.
<p style="text-align:center;">
<img src="/imgs/4things.png" width="800" alt="error">
<p>
## Label Vocabulary
There is usually not enough information in just the raw data file to identify the class (numeric or categorical ) correctly. Consider the following example. 
<p style="text-align:center;">
<img src="/imgs/vocabulary.png" width="800" alt="error">
</p>
(1) *Income* is actually a numeric feature but some of its values have a string prefix, which requires extraction of values. (2) *CustID* is unique for every customer, hence it can not be generalized for ML. (3) Inspecting only the column *XYZ*, it is difficult to decide if the feature is numeric or categorical. Thus, we created an intuitive 5-class prediction vocabulary by considering 3 more classes to captures different
variety of the columns.

## Features
We replicate the human-level intuition into ML models by extracting signal from the raw CSV files that a human reader would look at. Given a column, in order to identify the feature type, a human reader would look at the attribute (or column) name, some sample values in the column and even descriptive statistics about the column such as number of NaNs or number of distinct values. For instance, just by inspecting the attribute name such as ZipCode, an interpretable string, a human would know that the feature type is categorical. We extract these signals from the raw column and we summarize them in a feature set, which we use to build popular ML models.
<p style="text-align:center;">
<img src="/imgs/features.png" width="800" alt="error">
</p>

## Labeled Dataset
We obtain over 360 real datasets from several sources such as Kaggle and UCI ML Repo. Each column of the CSV file is just one example for our ML task. We collected over 9000 such examples and manually labelled them into either of the classes. This process took about 75 man hours across 4 months. 


## ML models

<p style="text-align:center;">
<img src="/imgs/cnn.png" width="800" alt="error">
</p>

<p style="text-align:center;">
<img src="/imgs/results.png" width="800" alt="error">
</p>

ML Data Prep Zoo Announcement
============================


<p style="text-align:center;">
<img src="/imgs/leaderboard.png" width="800" alt="error">
</p>