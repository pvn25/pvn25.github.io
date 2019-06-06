---
<!-- layout: archive -->
title: ""
permalink: /projects/
author_profile: true
---
##  Project SortingHat


##  Project SpeakQL


##  Project Hamlet++


While almost all ML toolkits assume that the input data for ML is a single table, many relational datasets in real-world advanced analytics applications are multi-table, typically connected by key-foreign key dependencies (KFKDs). This forces data scientists to source the extra base tables in order to join with the main table. Ealier work show that the features brought in by such joins can often be ignored without affecting ML accuracy significantly, i.e., we can “avoid joins safely.” This has at least two major implications. First, it could help reduce the runtimes of ML and feature selection methods. Second, it could reduce the burden of data sourcing, since data scientists can ignore certain tables altogether. However, the earlier work applied to only the linear classifiers. <br> 


In this work, we verify if their results hold for three popular high-capacity classifiers: decision trees, non-linear SVMs, and ANNs. We conduct an extensive experimental study using both real-world datasets and simulations to analyze the effects of avoiding KFK joins on such models. Our results show that these high-capacity classifiers are surprisingly and counter-intuitively more robust to avoiding KFK joins compared to linear classifiers. <br>