---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Research Interests
======
* Natural Language Processing
* Anomaly Detection
* Data Mining
* Deep Learning
* Machine Learning

Education
======
* **Amirkabir University of Technology** (Tehran Polytechnic), Tehran, Iran
  * B.Sc, Computer Engineering, 2016 - 2020 (expected)
  * Advisor: Prof. Saeedeh Momtazi
  * Bachelor’s Thesis: ”Implementation of a Persian Fake News Detection System and a Fake News Crawler Tool”.
  * GPA: **3.86** / 4
  
* **Mofid High School**, Tehran, Iran
  * B.Sc, Computer Engineering, 2016 - 2020 (expected)
  * High School Diploma in Mathematics and Physics, 2012 - 2016
  * GPA: **19.67** / 20


Research and Work Experience
======
* Fake News Detection System, Bachelor’s Thesis (April 2020 - present)
  Implemented a Persian fake news detection system using state-of-the-art architectures such as BERT for sentence embedding and Convolutional neural
networks for text classification. Also, a Persian fake news crawler was developed for scraping fake news from Persian news agencies websites - Python

* Anomaly Detection in Graph (September 2020 - present)
  Research on anomaly detection on graph data using variational autoencoders
  (VAE). In this study, nodes of the graph were represented by features vectors
  extracted with different graph embedding algorithm, and our proposed model
  can detect abnormal nodes in the graph - Python
  * Under supervision of Prof. AmirHaeri
  
* Question Recommendation System (May 2019 - November 2019)
  * Research Intern at IPM Brain Engineering Center
  This was my first project in NLP during my undergraduate studies. The goal
  was to develop a recommendation system using common text similarity metrics
  and static word embedding methods for recommending medical questions in the
  realm of Ophthalmology - Python
  * Under supervision of Prof. Lashgari
  
* SOP Company, as an Android Developer (October 2018 - October 2019)
  * Responsible for designing and developing a mHealth (mobile health) application
    and defining software requirements.
  
* Papillon Company, as Android Developer Intern (June 2017 - August 2017)

Notable Projects
======

* Information Retrieval
  A news search engine with the capability of crawling news, boolean searching,
  and vector space searching was developed. Clustering and classification algorithms were used for enhancing the search results and the speed of the search
  engine - Python
* Principles of Computational Intelligence
  Implemented an RBF neural network which trained by ES (Evolutionary Strategy) algorithm instead of backpropagation to update the weights and it used to
  solve regression and classification problems - Python
* Principles and Applications of Artificial Intelligence
  Implemented an interactive video based on foreground and background subtraction using MOG2 and KNN algorithms - Python
* Algorithm Design
  Detecting community structures using label propagation with weighted coherent
  neighborhood propinquity - Java

Technical Skills
======
* Programming & Scripting Language
  Python, Java, C, C#
  
* Machine Learning Tools
  * TensorFlow
  * Keras
  * GNU Octave
  * scikit-learn
* Web Development
  * HTML
  * CSS
  * JavaScript
  * Vue.js
  * Node.js
* Database Systems
  * MySQL
  * SQLite
* Mobile Development
  * Android
  * React Native

Publications
======
 * **M. Samadi**, M. Musavian, S. Momtazi, *”Deep Contextualized Text Representation and Learning for Persian Fake News Detection”*, **ACM Transactions on Asian Language Information Processing** (submitted), September 2020.
 * **M. Samadi**, *Question Recommendation System Based on the Pair Similarity* - technical report, September 2019.
  
Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
