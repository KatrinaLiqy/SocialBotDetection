# SocialBotDetection

This project is a replication of the paper [Scalable and Generalizable Social Bot Detection through Data Selection](https://ojs.aaai.org/index.php/AAAI/article/view/5460/5316).

## To replicate our work

* run .ipynb for API calls to collect ? data
* run DataCleaning.ipynb to convert raw data in json file and tsv file to 2-D arrays in csv formats, where each column represents a raw or derived feature
* run DataCombinationsAndRandomForest.ipynb to create 117 Random Forest models from combinations of the cleaned datasets
