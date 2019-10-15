# 1 Movie Plot Synopsis with Tags
## 1.1 Context
Abstract Social tagging of movies reveals a wide range of heterogeneous information about
movies, like the genre, plot structure, soundtracks, metadata, visual and emotional experiences.
<br>
Such information can be valuable in building automatic systems to create tags for movies. Au-
tomatic tagging systems can help recommendation engines to improve the retrieval of similar
<br>
movies as well as help viewers to know what to expect from a movie in advance. In this pa-
per, we set out to the task of collecting a corpus of movie plot synopses and tags. We describe a
<br>
methodology that enabled us to build a fine-grained set of around 70 tags exposing heterogeneous
characteristics of movie plots and the multi-label associations of these tags with some 14K movie
plot synopses. We investigate how these tags correlate with movies and the flow of emotions
<br>
throughout different types of movies. Finally, we use this corpus to explore the feasibility of infer-
ring tags from plot synopses. We expect the corpus will be useful in other tasks where analysis of
<br>
narratives is relevant.
## 1.2 Content
Please find the paper here: https://www.aclweb.org/anthology/L18-1274
<br>
This dataset was published in LREC 2018@Miyazaki, Japan.<br>
Keywords Tag generation for movies, Movie plot analysis, Multi-label dataset, Narrative texts
More information is available here http://ritual.uh.edu/mpst-2018/ <br>
Please use the following BibTex to cite the work.<br>

@InProceedings{KAR18.332, author = {Sudipta Kar and Suraj Maharjan and A. Pastor López-
Monroy and Thamar Solorio},
title = {{MPST}: A Corpus of Movie Plot Synopses with Tags},<br>
book- title = {Proceedings of the Eleventh International Conference on Language Resources and Eval-
uation (LREC 2018)},<br> year = {2018}, month = {May}, date = {7-12}, location = {Miyazaki, Japan},

editor = {Nicoletta Calzolari (Conference chair) and Khalid Choukri and Christopher Cieri and
Thierry Declerck and Sara Goggi and Koiti Hasida and Hitoshi Isahara and Bente Maegaard and
Joseph Mariani and Hélène Mazo and Asuncion Moreno and Jan Odijk and Stelios Piperidis and
Takenobu Tokunaga}, publisher = {European Language Resources Association (ELRA)}, address
= {Paris, France}, isbn = {979-10-95546-00-9}, language = {english} }

## 1.3 Acknowledgements
We would like to thank the National Science Foundation for partially funding this work under
award 1462141. We are also grateful to Prasha Shrestha, Giovanni Molina, Deepthi Mave, and
Gustavo Aguilar for reviewing and providing valuable feedback during the process of creating
tag clusters <br>

## 1.4 Problem Statement
Predict tags for a movie using synopsis
### 2 Machine learning problem
### 2.0.1 Data
https://www.kaggle.com/cryptexcode/mpst-movie-plot-synopses-with-tags/activity
<br>
## 2.0.2 Data overview-
Its consist of movie id , movie title, synopsis,tags,source

## 2.1 Type of Machine Learning Problem

It is a multi-label classification problem Multi-label Classification: Multilabel classification as-
signs to each sample a set of target labels. This can be thought as predicting properties of a data-
point that are not mutually exclusive, such as topics that are relevant for a document.
<br>
## 2.1.1 Performance metric
<li>1.Micro-Averaged F1-Score (Mean F Score) : The F1 score can be interpreted as a
weighted aver- age of the precision and recall, where an F1 score reaches its best value
at 1 and worst score at 0. The relative contribution of precision and recall to the F1
score are equal. The formula for the F1 score is: 2F1 = 2 * (precision * recall) / (preci-
sion + recall) In the multi-class and multi-label case, this is the weighted average of the
F1 score of each class.</li>
<li>2.Micro f1 score’: Calculate metrics globally by counting the total true positives, false
negatives and false positives. This is a better metric when we have class imbalance.
’Macro f1 score’: Calculate metrics for each label, and find their unweighted mean.
This does not take label imbalance into account</li>
