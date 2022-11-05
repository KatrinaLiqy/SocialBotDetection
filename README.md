# SocialBotDetection

This project is a replication of the paper [Scalable and Generalizable Social Bot Detection through Data Selection](https://ojs.aaai.org/index.php/AAAI/article/view/5460/5316). (Original paper).

## To replicate our work

* run DataCollecting.ipynb for API calls to collect missing data
* run DataCleaning.ipynb to convert raw data in json file and tsv file to 2-D arrays in csv formats, where each column represents a raw or derived feature
* run DataCombinationsAndRandomForest.ipynb to create 117 Random Forest models from combinations of the cleaned datasets
* run DataAnalysis.ipynb to find out (1) the best models by rankings based on AUC scores (2) the cooccurences of train datasets in the top 20 models (3) the breakdown of how many observations of humans and bots there are (4) 5-fold cross-validation (5) figure corresponding to figure 4 on the original paper (6) correlation between rank and standard deviation rank and training size of models.
* run DataAnalysisHeatmap.ipynb to train models on single datasets and test on another in order to see the correlation of datasets
* run ShapAnalysis.ipynb to see and compare the SHAP analysis on ours and their best models
* run ShapAnalysisII.ipynb to see what has happened behind extremely low entries of the heatmap and compare several of them
