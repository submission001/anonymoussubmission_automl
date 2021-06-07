# Dataset of "Multimodal AutoML on Structured Tables with Text Fields"

For loading the dataset, using the following code. The following loads the `prod` dataset mentioned in the paper.

```python
from auto_mm_bench.datasets import dataset_registry

print(dataset_registry.list_keys())
train_dataset = dataset_registry.create('product_sentiment_machine_hack', 'train')
test_dataset = dataset_registry.create('product_sentiment_machine_hack', 'test')
print(train_dataset.data)
```

The statistics  of the benchmarking datasets are given as follows. The list of `keys` are also shown in [benchmark/benchmark_datasets.txt](benchmark/benchmark_datasets.txt).

| ID       | key |  #Train | #Test | Task | Metric  | Task | Prediction Target |
|----------|------|---------|-------|------|--------|------|-------------------|
| prod     | product_sentiment_machine_hack  | 5,091 | 1,273 | multiclass | accuracy |  sentiment related to product |
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

# How to generate these datasets

Go to [scripts/data_processing](scripts/data_processing/README.md) to check the details.
