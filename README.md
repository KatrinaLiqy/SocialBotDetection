# SocialBotDetection

This project is a replication of the paper [Scalable and Generalizable Social Bot Detection through Data Selection](https://ojs.aaai.org/index.php/AAAI/article/view/5460/5316). (Original paper).

## To replicate our work

* run DataCollecting.ipynb for API calls to collect missing data
* run BotometerEvaluation.ipynb to find Botometer's classification of Twitter accounts sampled in DataCollecting.ipynb
* run DataCleaning.ipynb to convert raw data in json file and tsv file to 2-D arrays in csv formats, where each column represents a raw or derived feature
* run DataCombinationsAndRandomForest.ipynb to create 119 Random Forest models from combinations of the cleaned datasets
* run HyperparameterAnalysis.ipynb to see how class weight and max depth changes the performance of random forest models
* run DataPlot.ipynb to produce histograms of all models' performances on all metrics
* run DataAnalysis.ipynb to find out (1) the best models by rankings based on AUC scores (2) the co-occurences of training datasets in the top 25 models (3) relative ranks of authors' top models (4) the breakdown of how many observations of humans and bots there are (5) figure corresponding to figure 4 on the original paper (6) correlation between rank and standard deviation rank and training size of models.
* run DataAnalysisHeatmap.ipynb to train models on single datasets and test on another in order to see the correlation of datasets
* run ShapAnalysis.ipynb to see and compare the SHAP analysis on ours and their best models
* run ShapAnalysisII.ipynb to see what has happened behind extremely low entries of the heatmap and compare several of them

## Requirements

[pandas](https://pandas.pydata.org/docs/index.html), [scikit-learn](https://scikit-learn.org/stable/index.html), and [joblib](https://joblib.readthedocs.io/en/latest/) are required packages for almost all notebooks.

All generated plots require [seaborn](https://seaborn.pydata.org/).

DataCollecting.ipynb requires [tweepy](https://docs.tweepy.org/en/stable/) version 4.0 or later.

BotometerEvaluation.ipynb requires [Botometer](https://github.com/IUNetSci/botometer-python) (which depends on tweepy version 3.10 or lower... sorry) 