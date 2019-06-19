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


<p style="text-align:center;">
<img src="/imgs/automl.png" width="800" alt="error">
</p>


In this line of project(s), we aim to objectively quantify the key data prep taks by creating a commmon understanding of the data prep taks, understand why exactly these tasks are hard to automate, and create benchmark labeled datasets for them. Our focus is on relational data. Such datasets are typically stored with DB schemas in relational database management systems or as CSV or JSON files. A typical data prep workflow is shown below.


<p style="text-align:center;">
<img src="/imgs/task_steps.png" width="800" alt="error">
</p>


Case Study: ML Feature Type Inference
============================

<p style="text-align:center;">
<img src="/imgs/semantic_gap.png" width="800" alt="error">
</p>


<p style="text-align:center;">
<img src="/imgs/4things.png" width="800" alt="error">
</p>


<p style="text-align:center;">
<img src="/imgs/vocabulary.png" width="800" alt="error">
</p>


<p style="text-align:center;">
<img src="/imgs/features.png" width="800" alt="error">
</p>


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