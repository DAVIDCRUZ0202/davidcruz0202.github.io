---
layout: post
title: Notes on Making NN Predictions and Cleaning Data
subtitle: reflections on a second cross-functional project, with technical takeaways
gh-repo: https://github.com/DAVIDCRUZ0202/DS/tree/dc_work
gh-badge: [star, fork, follow]
---

I recently had the opportunity to work with another cross-functional team. We were assigned the task of building a price prediction application for homeowners looking to rent out their properties. The project was completed in a one-week timeframe, during which we successfully delivered on the main product's features. 

From a DS view, this was a great chance for me to practice my machine learning skills. This was a regression problem, as we wanted to predict a price, which is a float, otherwise known as a continuous variable. 

Studying the industry, we wanted to model our predictor to be trained off of recent and current pricing of rentals. The plan was to utilize AirBnB's API to gather information about rental prices. This turned out to be a dead-end. Due to restrictions, AirBnB (at the time) was not allowing access to their API, meaning that we ran into a major issue when it came to searching for live data.
 
Our solution was to turn to historical records. Thankfully, there are a variety of sources which document the historical pricing of rentals. Through diligent data sluething and research, we compiled a vast dataframe of rental properties, with their historical prices and all sorts of statistical measures to go along with it. Check out my github link above or this [readme](https://github.com/DAVIDCRUZ0202/DS/blob/dc_work/README.md) to dig deeper into the research done on this.

For model implementation, I approached various solutions. I used a linear regression model (Different than Logistic Regression!) for standard regressive practice. I also implemented a Sequential model. This implementation of a sequential model was one of my first stabs at using neural networks in practice. I built a model with three layers: two of layers with a 64 node density , and an output layer with 1 node (we are predicting one value.)

Experimenting with different optimizers and preprocessing techniques really helped solidify my understanding of what makes neural networks function. one of my favorite topics which I dug into was the concept of (Rectifiers)[https://en.wikipedia.org/wiki/Rectifier_(neural_networks)] in neural networks. Rectifiers are some of the most important activation functions to understand. It's interesting to read into some of the variants which have been developed and applied. When applied by a unit in a NN, these are called ReLu's or Rectified linear units. It's also good to research potential problems when using rectifier functions. One of the most important topics when it comes to using ReLu activation functions is the potential vanishing gradient effect. (Read here for more information on vanishing gradients.)[https://en.wikipedia.org/wiki/Vanishing_gradient_problem]

I loved working on this project , mainly because I was able to focus on more strict data science-type problems , rather than more broad software engineering techniques. The field of machine learning is vast and ever-growing, and I'm just getting settled into my role of being an eternal learner. I love what I've been studying so far, and I'm looking forward to the next project.