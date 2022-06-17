# 80-Cereals #

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jofaval/80-Cereals/blob/master/notebook.ipynb)

## Table of contents

1. [📁 Data](#-data)
1. [📓 Description](#-description)
1. [✔️ Objectives](#-objectives)
1. [🧱 Tech stack](#-tech-stack)
1. [💹 Algorithms](#-algorithms)
1. [📊 Visualization](#-visualization)
1. [🤓 Conclusions](#-conclusions)
1. [©️ Credits](#-credits)

## 📁 Data
[↑ Back to the table](#table-of-contents)

The data is from a Kaggle Dataset, [80 Cereals](https://www.kaggle.com/datasets/crawford/80-cereals).

## 📓 Description
[↑ Back to the table](#table-of-contents)

These are cereal ratings of american (USA) cereals, rated by, you guessed it, well, there's no direct clue, but Chris Crawford himself said in the dataset description that: "_Possibly from Consumer Reports_", so there's that. It's a good project to tackle, since the dataset it's one of quality, but really small, less than a hundred rows to work with.

This was a mandatory exercise from our A.I. and Big Data's Master, from which upon I extended into further detail. This is a regression project, that I also turned into a classification one, a multilabel classification project.

This notebook shows conclusions, exploration, analysis, researching into some meanings, hyperparameter tuning, algorithm understanding as to better apply them. It's a long one but it's full of little insights about them. This one I'd say is a little more advanced than the previous ones, and had some references that I looked for, as in, other notebooks that explored similar concepts in the Kaggle's Code section. _Yes, it is, exactly the same as the Game Of Thrones one, since I feel the same, it took more effort than expect to output a decent looking notebook_

## ✔️ Objectives
[↑ Back to the table](#table-of-contents)

In no specific order whatsoever:

- Apply all of the knowledge about regression projects and data exploration.
- Apply all of the knowledge about classification projects.
- Deeply explore, analyze and comprehend the dataset and it's meaning.
- Standarize and unify techniques, plot the explainability and maximize the human effort, I took this one personally at times.
- Understand what goes into the rating of a cereal, and what's the preferred type of cereal.
- Improving and polishing my skills as a junior data scientist and data analyst.
- Explore different solutions and it's prons and cons.
- Working with imbalancement and fixing it.
- Learning to work with small datasets.
- Tackle a project that's out of my comfort zone and not give up.

What were some of the main objectives?

- Use regression to predict the rating
- Classify per rating (bad, decent, good), or even by stars (1 - 5 or 1 - 10)
- Create a mapping decoder to know what details each thing belongs to

As secondary objectires there were

- Analyzing the manufacturer and use of sugar, and how that affected their overall rating.
- Visualizing the impact of the nutritional attributes on the calories.

## 🧱 Tech stack
[↑ Back to the table](#table-of-contents)

Python, that's it! R is a programming language that, as for the moment being, I have no experience with, even though it's powerful and broadly used, but I'd dare to say that no more than Python.

And one of the strongest points, if not the most, about Python, are it's libraries, so... the libraries I've used are:

- Pandas, data manipulation with an ease of use and exploration data analysis.
- Numpy, a really strong linear algebra library, used in the project for it's statistics utilities, SciPy may be an alternative, but I have no experience at all with it.
- Matplotlib and Seaborn, both fantastic libraries for data visualization, and they complement each other.
- Scikit-Learn, the library used for Machine Learning and statistics models: Logistic Regression, SVC, Naive Bayes, Random Forest, etc.
- Tensorflow and Keras, the industry standard for Deep Learning, the way to go, not really, it's just that for now I don't have that many experience with PyTorch

## 💹 Algorithms
[↑ Back to the table](#table-of-contents)

The algorithmic part of this project wasn't it's strongest point because of variety, it was consistent, implemented pipelines to reduce as much as possible manual interaction. But only two (kind of three) algorithms were used:

- Linear Regression and Logistic Regression
- Support Vector Machine Regressor

And Polynomials and Principal Component Analysis were applied to the Linear/Logistic regressor as to improve their performance and/or their efficiency. But the resolution to this project was easier than most. Since, when plotted, it was almost a straight line, the dataset had really important features that highly contributed to the explanation of the rating: fiber, potassium, calories, sugar, sodium.

Not that many times is there a project where one single plot visualices as clear as this one did, and the first algorithm you try hits the jackpot. But there was still a need to follow the steps by the book as to guarantee a good conclusion. It is overfitted, but it is a conclusion nonetheless, with more data we had the way to go, with more tuning down the line (pun intended).

Also, since I used supervised models, well, a supervised in which I based all my conclusions, explainability was an option, which is why I knew the most important features.

## 📊 Visualization
[↑ Back to the table](#table-of-contents)

Distribution and correlation plots are all over the map in this notebook, KDEs (Kernel Density Estimate), boxplots, histplots, piecharts.
Tables really helped a lot, an old classic, but effective! And speaking of old classics, barplots were the main metric for algorithmic comparison, with a couple of variations and groupings, but are the simplest while visually clear plots, for the purpose of my comparison.

The comparison visualizations are incomplete, kind of on purpose, they would overflow with redundant useless information, going into too much detail where there was no need. Also beacause I forgot and I was lazy, but later realized that it is not necessary for the purpose of this project. Nor in general, going into too much detail when the overall concept has been grasped will just confuse everyone.

Regression metrics are usually as simple as r2 score, but, as with classification, they're good, really good, but they usually go overheard, so I went ahead and plotted the predictions on a line, and also plotted the predicted regression compared to the real one. The more deviation, the worse it performed.

As aforementioned, the f1 score was "lying" to us, a high score didn't actually represented a model that was performing great, it just represented that on the unbalanced data it didn't miss as much on the majority. Fixing the imbalancement helped greatly, but still, a 50% score could mean that a model only scored well on one label, or that they performed the same on the both labels. So confusion matrix came in the rescue, with a little tuning following Shail Deliwala's (yes! from the GoT dataset, it was a great example of a normalized confusion matrix) notebook, so that the confusion matrix was even clearer to understand and to follow performance-wise.

Concluding: confusion matrices and distribution plots were the main focus for this notebook. Barplots and tables were a comfortable solution to answer some questions.
And, towards the end, the visualization are sort of a report of the performance, the conclusions of the analysis was not the main objective of this project, but what little there is, it's in text form. And plotting a regression is something more usefull that it may seem at first glance given that we already have the rooted score.

## 🤓 Conclusions
[↑ Back to the table](#table-of-contents)

This one took days, the Data Analysis was deeper this time, but the Data Science it's what took more time. My expectations were low given that it was a small dataset, but I spent far more time than I imagined.

I'm really proud of myself because I was able to tackle a project that was unbalanced, unclear at times, mainly because of the vague data description, that required of some exploration and algorithm tuning that I never did before. And mostly, because it required consistency and precision, to be conscious at all times of every little change. I learned a lot about the algorithms used as to understanding why they were working and why they weren't. I concluded with a model that barely changes no matter the seed.

The regression had a perfect score from the beginning, but the classification required a little bit more tuning. Still, this was just a compilation of knowdledge. It was satisfying to say the least.

From start to finish, it took a different turn, a couple of times, and it was sooo worth it! I had a biased result and I did not give up until I cleared that, once I did, I persevered to achieve a resolution that would satisfy myself. There were many aspects to take into account, it had the potential of being really challeing, which it did, but I made it.

As to the model, what seemed to matter the least for the rating of a cereal were:

- Manufacturer
- Shelf
- Type
- Weight, surprisingly
- Cups

And what explained the cereal rating was, by order of importance:

|  feature | importance |
|:--------:|:----------:|
|   fiber  |  48.208716 |
| calories | -33.408625 |
|   carbo  |  25.126372 |
|  protein |  19.639043 |
|  sodium  | -17.437665 |
|  potass  | -11.217806 |
|  sugars  | -10.148532 |
|    fat   |  -8.457040 |
| vitamins |  -5.121197 |

## ©️ Credits
[↑ Back to the table](#table-of-contents)

All of the credits for the datasets goes to [Chris Crawford](https://www.kaggle.com/crawford) and to [Kaggle](https://www.kaggle.com/) a company adquired by Google.