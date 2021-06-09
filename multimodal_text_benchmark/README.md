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

Link to original data source: https://machinehack.com/hackathons/product_sentiment_classification_weekend_hackathon_19/overview


## airbnb

Link to original data source: 

## wine

Link to original data source: 

## imdb

Link to original data source: 

## jigsaw

Link to original data source: 

## fake

Link to original data source: 

## kick

Link to original data source: 

## ae

Link to original data source: 

## qaa

Link to original data source: 

## qaq

Link to original data source: 

## cloth

Link to original data source: 

## mercari

Link to original data source: 

## jc

Link to original data source: 

## channel

Link to original data source: 

## pop
