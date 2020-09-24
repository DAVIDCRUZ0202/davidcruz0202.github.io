---
layout: post
title: An Analysis of MMA Weight Classes and their Common Characteristics
published: true
date: '2020-05-01'
---



 Is there a relationship between weight class and knockouts? How much of a difference does your weight have on your overall stamina? I set out to answer these questions, as well as explore some other characteristics that differ between weight classes in the competitive sport of Mixed Martial Arts.
  

 If you're a horse jockey, chances are that you don't desire to have the build of a NFL Linebacker. An athlete in perfect shape to be a sumo wrestling champion would not have the same outlook if he were to compete in a swimming race. As with all sports, the MMA world is no different.

To research this topic, I utilized the site Kaggle, which has readily available data sets on the world's largest and most active MMA Organization, the [UFC](https://www.kaggle.com/rajeevw/ufcdata#raw_total_fight_data.csv). For my graphs, I worked with a data set which includes raw fight stats from 1993 to 2019. Over the course of 27 years, The UFC has had over 5000 professional fights. Instead of working with one data set of that size, I divided the data into different subsets. I made separate data sets for 3 main classes: Lightweight (146lb - 155lb), Middleweight (171lb - 185lb), and Heavyweight (206lb – 265lb).
 
## The Graphs

 I refined and manipulated the data set 'raw_total_fight_data.csv' in order to discover the following information. This first graph shows us the total number of fights each weight class held, as well as their total number of KO/TKO's, and Submissions. By far, the Lightweight division is the most common weight class. Light and Middle weight classes also hold an advantage over the Heavyweights when it comes to Submissions.

![Graph1](https://raw.githubusercontent.com/DAVIDCRUZ0202/DAVIDCRUZ0202.github.io/master/img/graph_1.PNG){: .center-block :}

_"Total Fights" includes all types of finishes, as well as all of the fights that went to decision, draw, etc._

 Although they have half as many fights under their category, the heavyweight division crushes the other two divisions as far as their KO/TKO percentage, flat out doubling the other weight classes statistics, as shown in the graph below.

![Graph2](https://raw.githubusercontent.com/DAVIDCRUZ0202/DAVIDCRUZ0202.github.io/master/img/graph_2_new.PNG){: .center-block :}

 All of that power comes at a price. This third graph shows us how many strikes in total, per fight, are attempted, per competitor. As your weight class goes up, the amount of attempted strikes goes down. This reaffirms the idea that the bigger you are, the less stamina you conserve with each attempted strike. Heavier weight classes compensate for this loss of stamina through sheer strength, opting to "finish" their fights much more often rather than going for a decision.

![Graph3](https://raw.githubusercontent.com/DAVIDCRUZ0202/DAVIDCRUZ0202.github.io/master/img/graph_3.PNG){: .center-block :}

 Regardless of how the fight concludes, all forms of victory are valid and get the job done. MMA is as much a sport of technical advantage as it is phyiscal talent. I've only scratched the surface of potential insights one can gather from studying this data, and I look forward seeing and reading to other explorations on this topic.
