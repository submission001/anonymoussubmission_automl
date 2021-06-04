# Code and Benchmark of Submission "Multimodal AutoML on Structured Tables with Text Fields"

## Install the Benchmark Suite

```bash
cd multimodal_text_benchmark
# Install the benchmarking suite
python3 -m pip install -U -e .
```

You can do a quick test of the installation by going to the test folder

```bash
cd multimodal_text_benchmark/tests
python3 -m pytest test_datasets.py
```

To access one dataset, try to use the following code:

```python
from auto_mm_bench.datasets import dataset_registry

print(dataset_registry.list_keys())
train_dataset = dataset_registry.create('product_sentiment_machine_hack', 'train')
test_dataset = dataset_registry.create('product_sentiment_machine_hack', 'test')
print(train_dataset.data)
```

## Details about the Datasets

The details of the datasets in our benchmark will be in [multimodal_text_benchmark](multimodal_text_benchmark/README.md).

## License
The benchmarking datasets are released under this licensing scheme: [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode).

We do not own any of the datasets in the benchmark and this benchmark can only be used for noncommercial purpose.


## Install AutoGluon

You will need to install MXNet first as a prerequisite:

### Install MXNet

As a prerequisite, the current version of AutoGluon requires MXNet and it is recommended to use MXNet 1.8 wheel with CUDA 11.0

```bash

# CPU-only
python3 -m pip install https://aws-mx-pypi.s3-us-west-2.amazonaws.com/1.8.0/aws_mx-1.8.0-py2.py3-none-manylinux2014_x86_64.whl

# CUDA 11 Version
python3 -m pip install https://aws-mx-pypi.s3-us-west-2.amazonaws.com/1.8.0/aws_mx_cu110-1.8.0-py2.py3-none-manylinux2014_x86_64.whl
```

```bash
cd autogluon
bash full_install.sh
```

## Run Experiments

Go to [multimodal_text_benchmark/scripts/benchmark](multimodal_text_benchmark/scripts/benchmark) to view how to run the benchmark codes
