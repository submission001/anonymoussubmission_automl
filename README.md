# Multimodal AutoML Benchmark on Structured Tables with Text Fields

This benchmark contains diverse tabular datasets, each containing numeric/categorical as well as text columns.
The goal is to evaluate the performance of (automated) ML systems for such multimodal supervised learning tasks (classification and regression).
Python code is provided to run different variants of the [AutoGluon](https://github.com/awslabs/autogluon/) AutoML tool on the benchmark.


## Details about the Datasets

The datasets in our benchmark are described in the [multimodal_text_benchmark README](multimodal_text_benchmark/README.md).


## License
The benchmarking datasets are released under this licensing scheme: [CC BY-NC-SA](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode).

We do not own any of the datasets in the benchmark and this benchmark can only be used for noncommercial purposes. Please also refer to the licenses of the original sources for each dataset linked in the [multimodal_text_benchmark README](multimodal_text_benchmark/README.md).


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


## Install AutoGluon

This repository contains a particular version of AutoGluon we previously ran on the benchmark. We recommend installing it in a fresh virtualenv. 
To use this version, you will need to install MXNet first as a prerequisite. It is recommended to use MXNet 1.8 wheel with CUDA 11.0:

```bash

# CPU-only
python3 -m pip install https://aws-mx-pypi.s3-us-west-2.amazonaws.com/1.8.0/aws_mx-1.8.0-py2.py3-none-manylinux2014_x86_64.whl

# CUDA 11 Version
python3 -m pip install https://aws-mx-pypi.s3-us-west-2.amazonaws.com/1.8.0/aws_mx_cu110-1.8.0-py2.py3-none-manylinux2014_x86_64.whl
```

Once you have MXNet, you can install our version of AutoGluon:

```bash
cd autogluon
bash full_install.sh
```

For more information or if you want to run a different version of AutoGluon, please refer to the [AutoGluon website](https://auto.gluon.ai/).

## Run Experiments

Go to [multimodal_text_benchmark/scripts/benchmark](multimodal_text_benchmark/scripts/benchmark) to view how to run the benchmark codes.
