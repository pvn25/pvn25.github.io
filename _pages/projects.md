---
<!-- layout: archive -->
title: ""
permalink: /projects/
author_profile: true
---
##  Project SortingHat

Data preparation time still remains a major roadblock for real-world ML applications, since it is ususally handled fully manually by data scientists. The grunt work of data prep involves diverse tasks such as identifying features types for ML, standardizing and cleaning feature values, and feature transformations. This reduces data scientists’ productivity and raises costs. It is also an impediment to industrial-scale AutoML platforms that build ML models on millions of datasets.



To tackle this challenge, we envision a new line of research to dramatically reduce the human effort need in data prep for ML: using ML to automate data prep for ML. We abstract specific ML data prep tasks and cast them as applied ML tasks. We present the ML Data Prep Zoo, a community-led repository of benchmark labeled datasets, and pre-trained ML models for ML data prep tasks.



In this project, we apply the above philosophy on a ubiquitous data prep issue when applying ML over relation data: ML Schema Extraction. Datasets are typically exported from DBMSs into tools such as Python and R as CSV files. This creates a semantic gap between attribute types in a DB schema (such as strings or integers) and feature types in a ML schema (such as numeric or categorical). Hence, the data scientist is forced to manually extract the ML schema. SortingHat cast this task as ML classification problem and allow users to quickly dispose of easy features, and repriortize their effort towards features that need more human attention.


More details about the project can be found [here](https://adalabucsd.github.io/sortinghat).

##  Project SpeakQL

Natural language and touch-based interfaces are making data querying significantly easier. But typed SQL remains the gold standard for query sophistication although it is painful in querying environments that are touch-oriented (e.g., iPad or iPhone) and essentially impossible in speech-driven environments (e.g., Amazon Echo). Recent advancements in automatic speech recognition (ASR) raise the tantalizing possibility of bridging this gap by enabling spoken queries over structured data.


In this project, we envision and prototype a series of new spoken data querying systems. Going beyond the current capability of personal digital assistants such as Alexa in answering simple natural language queries over well-curated in-house knowledge base schemas, we aim to enable more sophisticated spoken queries over arbitrary application database schemas.


Our first and current focus is on designing and implementing a new speech-driven query interface and system for a useful subset of regular SQL. Our goal is near-perfect accuracy and near-real-time latency for transcribing spoken SQL queries. Our plan to achieve this goal is by synthesizing and innovating upon ideas from ASR, natural language processing (NLP), information retrieval, database systems, and HCI to devise a modular end-to-end system architecture that combines new automated algorithms with user interactions.


More details about the project can be found [here](https://adalabucsd.github.io/speakql).

##  Project Hamlet++


While almost all ML toolkits assume that the input data for ML is a single table, many relational datasets in real-world advanced analytics applications are multi-table, typically connected by key-foreign key dependencies (KFKDs). This forces data scientists to source the extra base tables in order to join with the main table. Ealier work show that the features brought in by such joins can often be ignored without affecting ML accuracy significantly, i.e., we can “avoid joins safely.” This has at least two major implications. First, it could help reduce the runtimes of ML and feature selection methods. Second, it could reduce the burden of data sourcing, since data scientists can ignore certain tables altogether. However, the earlier work applied to only the linear classifiers. <br> 


In this work, we verify if their results hold for three popular high-capacity classifiers: decision trees, non-linear SVMs, and ANNs. We conduct an extensive experimental study using both real-world datasets and simulations to analyze the effects of avoiding KFK joins on such models. Our results show that these high-capacity classifiers are surprisingly and counter-intuitively more robust to avoiding KFK joins compared to linear classifiers. <br>


More details about the project can be found [here](https://adalabucsd.github.io/hamlet).