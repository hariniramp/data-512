# Project Goal
The goal of this project is to conduct an exploratory data analysis on the [Wikipedia talk corpus](https://figshare.com/projects/Wikipedia_Talk/16731) for potential sources of bias. The 2 datasets I aim to analyze are the ones concerning [Toxicity](https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Toxicity/4563973) and [Aggression](https://figshare.com/articles/dataset/Wikipedia_Talk_Labels_Aggression/4267550).
I chose these 2 datasets because both these datasets have been annotated similarly (on scales of -2 to 2, -2 being the most aggressive/toxic and 2 being the least aggressive/toxic). Thus, comparison is made more convenient.
Since these datasets have been annotated by human crowdworkers, I aim to uncover some potential areas of bias in the dataset. 

All data, documentation, and code is published in this GitHub repository. 

# Dependencies
The dependencies used in analysis of the dataset are as follows:

  * nltk
  * matplotlib
  * wordcloud
  * os
  * pandas
  * numpy
  * urllib
  * string
 
# Interesting Findings
1. My first question was: 

**Are members of a specific group more likely to label a comment as toxic/aggressive than others? Eg: a higher percentage of females likely to label a comment as aggressive than males.**

![Aggressive comments labelling by gender](https://github.com/hariniramp/data-512/blob/main/data-512-a2/Visualizations/stacked_bargraph_aggression_gender.png)

![Aggressive comments labelling by education level](https://github.com/hariniramp/data-512/blob/main/data-512-a2/Visualizations/stacked_bargraph_aggression_education.png)

From my analysis, it was apparent that the curators of the dataset had done their best to mitigate bias in this regard by moderating the dataset to contain a fairly equal proportion 
of annotators from all groups across attributes like gender, age, education level and native English speaking ability. This is seen in the graphs above where the dataset is fairly equally
distributed across all groups for people who labelled comments as aggressive and non-aggressive.

2. My second analysis concerned the question: 

**Do labellers disagree more about some hostile speech than others (toxic vs aggressive language)? How can we quantify this disagreement and what type of comments invoke disagreements in labellers?**

I visualized disagreement in labels using histograms and the standard deviation in crowdworkers' scores. The disagreement was much higher in the Aggression dataset than the Toxicity one.
This is definitely a potential source of bias in the dataset. 

![Disagreement in Aggressive Comments' Labels](https://github.com/hariniramp/data-512/blob/main/data-512-a2/Visualizations/histogram_disagreement_aggression.png)

I also tried a word cloud imaging to understand what kind of language is associated with different datasets. I found many swear words and as a result am displaying the tamest 
word cloud below. It was for the toxicity dataset comments that were most agreed upon by labellers.

![Wordcloud visualization](https://github.com/hariniramp/data-512/blob/main/data-512-a2/Visualizations/wordcloud_toxic_agreements.png)

3. My final analysis addressed this question: 

**Is the population of labellers representative of the world’s population?**

Upon visualizing, I realized that the population distribution of the labellers was not at all representative of the world's population and this was a major way in which bias
can potentially leak into the dataset. A pie chart below shows the major imbalance in one of the attributes' distribution (gender). This was true of both datasets.

![Gender imbalance in labellers of Aggression dataset](https://github.com/hariniramp/data-512/blob/main/data-512-a2/Visualizations/pie_gender_aggression.png)

# Data Files, Code & Analysis
## Data
I was unable to add more than one file to the 'Data' folder because of the sheer size of the .csv files. However, upon running the code, one can recreate these datasets without much difficulty.

## Output
The final visualizations can be found in the Visualizations folder [here](https://github.com/hariniramp/data-512/tree/main/data-512-a2/Visualizations)

## Analysis
All analysis is performed in a [Jupyter notebook]() with method explanations, observations and comparisons in Markdown cells.

## Interesting Background
[Wikipedia DeTox project Research](https://meta.wikimedia.org/wiki/Research:Detox) 

[Dataset description and schemas](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release) 

[Overview of Google’s Conversation AI project](https://conversationai.github.io/) 

[Perspective Hacks Gallery](https://github.com/conversationai/perspectiveapi/wiki/perspective-hacks)
 
# Reproducibility
This repository contains a Jupyter notebook that is entirely reproducible. One can download it and run it from start to finish to reproduce it. Each code chunk is preceded
by a description of what the code chunk does for added clarity. For any further questions, mail the author at hramprasad98@gmail.com

# License and Terms of Use
This project is licensed under the [MIT License.](https://github.com/hariniramp/data-512/blob/main/data-512-a2/LICENSE)
