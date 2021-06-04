# Dataset

# Generate statistics

```
python3 get_dataset_analytics.py
```

## Jigsaw Unintended Bias in Toxicity Classification

Kaggle link: https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification/data.

The task in Kaggle competition is to classify whether the user comment contains toxic information.

To preprocess the dataset, we used the following commands:

```
kaggle competitions download -c jigsaw-unintended-bias-in-toxicity-classification
unzip jigsaw-unintended-bias-in-toxicity-classification.zip -d jigsaw-unintended-bias-in-toxicity-classification
python3 process_jigsaw.py
```

## Product Sentiment Analysis
MachineHack link: https://www.machinehack.com/hackathons/product_sentiment_classification_weekend_hackathon_19/overview

The task is to analyze sentiment of the user's comments on the product.

```
mkdir -p machine_hack_product_sentiment
wget https://automl-mm-bench.s3.amazonaws.com/machine_hack_product_sentiment/all_train.csv -O machine_hack_product_sentiment/all_train.csv
```

## Google Quest QA

```
kaggle competitions download -c google-quest-challenge
unzip google-quest-challenge.zip -d google-quest-challenge
python3 process_google_quest_qa.py
```

## Women Clothing Review

```
python3 process_women_clothing_review.py
```

## Airbnb Price Prediction

Download the data from S3
```
wget -O cleansed_listings_dec18.csv https://autogluon-text-data.s3.amazonaws.com/multimodal_text/melbourne-airbnb/cleansed_listings_dec18.csv
python3 process_airbnb.py
```


## Mercari Price Suggestion Challenge

Source: https://www.kaggle.com/c/mercari-price-suggestion-challenge/data

```
kaggle competitions download -c mercari-price-suggestion-challenge
unzip mercari-price-suggestion-challenge.zip -d mercari-price-suggestion-challenge
sudo apt-get install p7zip-full
cd mercari-price-suggestion-challenge
7z x train.tsv.7z
7z x test.tsv.7z
cd ..
python3 process_mercari_price_suggestion.py
```

## AE Innerwear Price Prediction

Source: https://www.kaggle.com/PromptCloudHQ/innerwear-data-from-victorias-secret-and-others

```
wget -O ae_com.csv.zip https://automl-mm-bench.s3.amazonaws.com/ae_com.csv.zip
unzip ae_com.csv.zip
python3 process_ae_price_prediction.py

```

## JC Penny

Source: https://www.kaggle.com/PromptCloudHQ/all-jc-penny-products
Download and then run
```
python3 process_jc_penney.py
```

## Kickstarter Funding

https://www.kaggle.com/codename007/funding-successful-projects?select=train.csv

```
python3 process_kicksarter.py
```

## IMDB

https://www.kaggle.com/PromptCloudHQ/imdb-data?select=IMDB-Movie-Data.csv

```
python3 process_imdb_genre.py
```

## News Popularity

https://archive.ics.uci.edu/ml/datasets/online+news+popularity

```
python3 process_news_popularity.py
```

## Wine Review
https://www.kaggle.com/zynicide/wine-reviews (winemag-data-130k-v2.csv)


## Fake Jobs
https://www.kaggle.com/shivamb/real-or-fake-fake-jobposting-prediction

```
python3 process_fake_jobs.py
```

