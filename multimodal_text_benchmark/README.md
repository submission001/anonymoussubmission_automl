# Datasets in the Benchmark

Here is how to load a particular dataset into a pandas DataFrame. The following code loads the `prod` (i.e. product_sentiment_machine_hack) dataset:

```python
from auto_mm_bench.datasets import dataset_registry

print(dataset_registry.list_keys())  # use these keys to specify which dataset to load

train_dataset = dataset_registry.create('product_sentiment_machine_hack', 'train')
test_dataset = dataset_registry.create('product_sentiment_machine_hack', 'test')
print(train_dataset.data)
```

These commands will also download a local copy of the dataset file, which is either in Parquet or CSV format (both can be easily loaded into pandas DataFrame).

The statistics of the benchmarking datasets are listed in the table below. The list of `keys` are also shown in [scripts/benchmark/benchmark_datasets.txt](scripts/benchmark/benchmark_datasets.txt). You can use these `key` strings to load any of the datasets in the benchmark via the above code. 


| ID       | key |  #Train | #Test | Task | Metric  | Prediction Target |
|----------|-----|---------|-------|------|---------|-------------------|
| prod     | product_sentiment_machine_hack  | 5,091 | 1,273 | multiclass | accuracy | sentiment related to product |
| airbnb   | melbourne_airbnb  | 18,316  | 4,579  | multiclass  | accuracy | price of Airbnb listing |
| channel  | news_channel  | 20,284  | 5,071  | multiclass | accuracy | category of news article |
| wine     | wine_reviews  | 84,123  | 21,031 | multiclass | accuracy | variety of wine |
| imdb     | imdb_genre_prediction | 800 | 200 | binary | roc_auc | whether film is a drama |
| jigsaw   | jigsaw_unintended_bias100K | 100,000 | 25,000 | binary | roc_auc | whether comments are toxic |
| fake     | fake_job_postings2 | 12,725 | 3,182 | binary | roc_auc | whether job postings are fake |
| kick     | kick_starter_funding | 86,052 | 21,626 | binary | roc_auc | will Kickstarter get funding |
| ae       | ae_price_prediction  | 22,662 | 5,666 | regression | r2 | American-Eagle item prices |
| qaa      | google_qa_answer_type_reason_explanation | 4,863 | 1,216 | regression | r2 | type of answer |
| qaq      | google_qa_question_type_reason_explanation | 4,863 | 1,216 | regression | r2 | type of question |
| cloth    | women_clothing_review | 18,788 | 4,698 | regression | r2 | review score |
| mercari  | mercari_price_suggestion100K | 100,000 | 25,000 | regression | r2 | price of Mercari products |
| jc       | jc_penney_products | 10,860 | 2,715 | regression | r2 | price of JC Penney products |
| pop      | news_popularity2 | 24,007 | 6,002 | regression | r2 | news article popularity online |


# Benchmark Creation

The folder [scripts/data_processing](scripts/data_processing/README.md) contains the scripts previously used to create the benchmark version of each dataset from the original data source. 

# Additional Details for each Dataset

## prod

Original data source: Product Sentiment Classification (MachineHack prediction competition)

Link: https://machinehack.com/hackathons/product_sentiment_classification_weekend_hackathon_19/overview


## airbnb

Original data source: Melbourne Airbnb Open Data

Link: https://www.kaggle.com/tylerx/melbourne-airbnb-open-data

## wine

Original data source: 130k wine reviews with variety, location, winery, price, and description (from WineEnthusiast)

Link: https://www.kaggle.com/zynicide/wine-reviews

## imdb

Original data source: IMDB data from 2006 to 2016 - A data set of 1,000 popular movies on IMDB in the last 10 years

Link: https://www.kaggle.com/PromptCloudHQ/imdb-data

**Note:** PromptCloud released the original version of the data from which the version of this dataset in our benchmark
was created.

## jigsaw

Original data source: Jigsaw Unintended Bias in Toxicity Classification (Kaggle prediction competition)

Link: https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification

## fake

Original data source: Fake JobPosting Prediction

Link: https://www.kaggle.com/shivamb/real-or-fake-fake-jobposting-prediction

## kick

Original data source: Funding Successful Projects on Kickstarter

Link: https://www.kaggle.com/codename007/funding-successful-projects

## ae

Original data source: Innerwear Data from American Eagle

Link: https://www.kaggle.com/PromptCloudHQ/innerwear-data-from-victorias-secret-and-others

**Note:** PromptCloud released the original version of the data from which the version of this dataset in our benchmark
was created.

## qaa

Original data source: Google QUEST Q&A Labeling (Kaggle prediction competition)

Link: https://www.kaggle.com/c/google-quest-challenge

## qaq

Original data source: Google QUEST Q&A Labeling (Kaggle prediction competition)

Link: https://www.kaggle.com/c/google-quest-challenge

## cloth

Original data source: Women's E-Commerce Clothing Reviews

Link: https://www.kaggle.com/nicapotato/womens-ecommerce-clothing-reviews

## mercari

Original data source: Mercari Price Suggestion Challenge (Kaggle prediction competition)

Link: https://www.kaggle.com/c/mercari-price-suggestion-challenge

## jc

Original data source: 20,000 product listings from JCPenney

Link: https://www.kaggle.com/PromptCloudHQ/all-jc-penny-products

**Note:** PromptCloud released the original version of the data from which the version of this dataset in our benchmark
was created.


## pop

Original data source: Online News Popularity Data Set

Link: https://archive.ics.uci.edu/ml/datasets/online+news+popularity


## channel

Original data source: Online News Popularity Data Set

Link: https://archive.ics.uci.edu/ml/datasets/online+news+popularity

