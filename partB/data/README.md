# Dataset: Synthetic Binary Sentiment

## Overview
A synthetically generated binary sentiment dataset designed to mirror the RT-s
snippet sentiment classification task from Wang & Manning (2012).

## Files
- `synthetic_sentiment_train.csv` — 1,200 training examples (600 positive, 600 negative)
- `synthetic_sentiment_test.csv`  — 400 test examples (200 positive, 200 negative)

## Columns
- `text`: raw text snippet (~15 words on average)
- `label`: 1 = positive sentiment, -1 = negative sentiment

## Generation
The dataset is generated inline in `task_2_1.ipynb` using a fixed random seed (42).
No manual download steps are required. Run the notebook from top to bottom to regenerate.

## How It Is Used
- Used in `task_2_1.ipynb` for dataset setup and feature extraction.
- Used in `task_2_2.ipynb` for method implementation and reproduction.
- Used in `task_2_3.ipynb` for result reporting and visualisation.
- Used in `task_3_1.ipynb` for ablation experiments.
- Used in `task_3_2.ipynb` for failure mode analysis.

## Limitations vs. Paper's Dataset
The paper's RT-s dataset has ~21K vocabulary tokens with genuine linguistic variation
(negation, idiom, sarcasm). This synthetic dataset has ~65 unigrams with clean
class-conditional structure, making it easier to classify (resulting in ~99% accuracy
vs the paper's ~78%). Qualitative trends (bigrams help, NBSVM ≥ MNB and SVM) are preserved.
