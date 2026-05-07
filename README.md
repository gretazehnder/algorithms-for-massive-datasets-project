# Market basket analysis on IMDB dataset

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/gretazehnder/algorithms-for-massive-datasets-project/blob/main/market_basket_analysis.ipynb)

## Overview

This project implements a market basket analysis system on the [IMDB Top 1000 Movies and TV Shows Dataset](https://www.kaggle.com/datasets/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows). Each movie is modeled as a transaction (basket) and the actors listed in the `Star1`–`Star4` fields are treated as items. The goal is to discover frequent co-acting patterns using scalable frequent itemset mining algorithms.

## Algorithms

Three algorithms are implemented and compared:

- **Apriori** — baseline algorithm using the antimonotonicity property to prune candidates
- **PCY** (Park–Chen–Yu) — extends Apriori with hash-based candidate pruning to reduce memory usage
- **SON** (Savasere–Omiecinski–Navathe) — partition-based approach designed to scale in distributed environments

## Repository structure

```
algorithms-for-massive-datasets-project/
├── market_basket_analysis.ipynb   # Main notebook (runnable on Google Colab)
├── algorithms_report.pdf          # Project report
└── README.md
```

## Requirements

The notebook is designed to run on Google Colab. The following libraries are used:

- `pandas`
- `mlxtend`
- `matplotlib`
- `collections`, `itertools`, `math`, `time` (Python standard library)

## Dataset

The dataset is downloaded directly in the notebook via the Kaggle API. It is released under the Public Domain license.
