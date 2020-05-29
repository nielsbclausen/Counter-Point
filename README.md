# CounterPoint

I built a programme that allows for a user to input an article and recieve a couple of articles arguing the opposing point.
This matters as we increasingly see more polarised political discourse.

You can reach me at:
* [clausen1996@gmail.com]()

### Executive Summary

With an increasing amount of political discourse no longer looking to seek the common ground but instead concentrating on our political divides, I hope to create a system that allows for individuals to have more varied reading habbits and a more well rounded understanding of topics at hand. Commercially, most news platforms that collect articles for their users (think apple news) may find this tool a healthy addition to their platforms and may find a competitive market edge in the process. 

In order to fulfil this goal I first found a labeled dataset from the Univeristy of Michigan consisting of just over 21 thousand articles. The dataset labeled each article with a primary and secondary topic as well its political bias (democrat or republican). 
Using Newspaper3K I webscrpaed the text of each article (as the dataset only provided the url) and, after some cleaning of the scraped texts, I used NLTK for some Natural Language (Pre)Processing. Once my data was ready I used the Scikit Learn library to test different classifiers with a Support Vector Machine employing a Gaussian RBF Kernel coming out on top. 

This classifier is very good at predicting the political inclination of a text (left leaning, right leaning or neutral). Hence the model is able to predict the political inclination of a previously unseen text. This prediction is used to then recommend previously analysed atricles that oppose the unseen, user inputed article.