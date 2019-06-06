---
<!-- layout: archive -->
title: ""
permalink: /projects/
author_profile: true
---
##  Project SortingHat


##  Project SpeakQL

Natural language and touch-based interfaces are making data querying significantly easier. But typed SQL remains the gold standard for query sophistication although it is painful in querying environments that are touch-oriented (e.g., iPad or iPhone) and essentially impossible in speech-driven environments (e.g., Amazon Echo). Recent advancements in automatic speech recognition (ASR) raise the tantalizing possibility of bridging this gap by enabling spoken queries over structured data.


In this project, we envision and prototype a series of new spoken data querying systems. Going beyond the current capability of personal digital assistants such as Alexa in answering simple natural language queries over well-curated in-house knowledge base schemas, we aim to enable more sophisticated spoken queries over arbitrary application database schemas.


Our first and current focus is on designing and implementing a new speech-driven query interface and system for a useful subset of regular SQL. Our goal is near-perfect accuracy and near-real-time latency for transcribing spoken SQL queries. Our plan to achieve this goal is by synthesizing and innovating upon ideas from ASR, natural language processing (NLP), information retrieval, database systems, and HCI to devise a modular end-to-end system architecture that combines new automated algorithms with user interactions.


More details about the [project](https://adalabucsd.github.io/speakql)

##  Project Hamlet++


While almost all ML toolkits assume that the input data for ML is a single table, many relational datasets in real-world advanced analytics applications are multi-table, typically connected by key-foreign key dependencies (KFKDs). This forces data scientists to source the extra base tables in order to join with the main table. Ealier work show that the features brought in by such joins can often be ignored without affecting ML accuracy significantly, i.e., we can “avoid joins safely.” This has at least two major implications. First, it could help reduce the runtimes of ML and feature selection methods. Second, it could reduce the burden of data sourcing, since data scientists can ignore certain tables altogether. However, the earlier work applied to only the linear classifiers. <br> 


In this work, we verify if their results hold for three popular high-capacity classifiers: decision trees, non-linear SVMs, and ANNs. We conduct an extensive experimental study using both real-world datasets and simulations to analyze the effects of avoiding KFK joins on such models. Our results show that these high-capacity classifiers are surprisingly and counter-intuitively more robust to avoiding KFK joins compared to linear classifiers. <br>


More details about the [project](https://adalabucsd.github.io/hamlet)