# Text Classification Model Comparison

This repository compares the performance of different machine learning models for text classification using various vectorization techniques and algorithms.

## XGBoost Results

| S.NO. | Vectorization | Max Depth | Max Sample Split Size | Test AUC | Precision Score |
|-------|---------------|-----------|-----------------------|----------|-----------------|
| 1     | BOW           | 2         | 435                   | 0.9031   | 96.10%          |
| 2     | TFIDF         | 2         | 455                   | 0.8963   | 96.00%          |
| 3     | AVG W2V       | 1         | 530                   | 0.8795   | 95.82%          |
| 4     | TFIDF W2V     | 1         | 530                   | 0.8712   | 95.08%          |

## Random Forest Results

| S.NO. | Vectorization | Max Depth | Max Sample Split Size | Test AUC | Precision Score |
|-------|---------------|-----------|-----------------------|----------|-----------------|
| 1     | BOW           | 12        | 115                   | 0.8697   | 95.42%          |
| 2     | TFIDF         | 10        | 135                   | 0.8665   | 95.79%          |
| 3     | AVG W2V       | 10        | 135                   | 0.8935   | 96.59%          |
| 4     | TFIDF W2V     | 10        | 165                   | 0.8681   | 94.99%          |

## Decision Tree Results

| S.NO. | Vectorization | Max Depth | Max Sample Split Size | Test AUC | Precision Score |
|-------|---------------|-----------|-----------------------|----------|-----------------|
| 1     | BOW           | 3         | 10                    | 0.6958   | 91.90%          |
| 2     | TFIDF         | 4         | 20                    | 0.7169   | 91.54%          |
| 3     | AVG W2V       | 3         | 2                     | 0.7515   | 93.59%          |
| 4     | TFIDF W2V     | 4         | 50                    | 0.7528   | 91.69%          |

## K-Nearest Neighbors (KNN) Results

| S.NO. | Model               | Featurization | Best K | Test AUC | Precision Score | Accuracy | F1-Score |
|-------|---------------------|---------------|--------|----------|-----------------|----------|----------|
| 1     | Brute Force (10K)   | BOW           | 6863   | 0.9025   | 96.04%          | 82.50%   | 88.79%   |
| 2     | Brute Force (100)   | BOW           | 45     | 0.6408   | 87.74%          | 70.13%   | 80.81%   |
| 3     | Brute Force (10K)   | TFIDF         | 9860   | 0.9207   | 96.81%          | 84.40%   | 90.07%   |
| 4     | Brute Force (100)   | TFIDF         | 35     | 0.5211   | 84.52%          | 65.48%   | 77.81%   |
| 5     | Brute Force (100)   | AVG-W2V       | 97     | 0.8822   | 95.59%          | 79.67%   | 86.71%   |
| 6     | Brute Force (100)   | TFIDF-W2V     | 91     | 0.8522   | 94.31%          | 77.16%   | 85.07%   |
| 7     | KD-Tree (100)       | BOW           | 71     | 0.7538   | 92.12%          | 68.48%   | 78.44%   |
| 8     | KD-Tree (100)       | TFIDF         | 37     | 0.5965   | 86.94%          | 58.57%   | 70.73%   |
| 9     | KD-Tree (100)       | AVG-W2V       | 97     | 0.8822   | 95.59%          | 79.67%   | 86.78%   |
| 10    | KD-Tree (100)       | TFIDF-W2V     | 91     | 0.8522   | 94.31%          | 77.16%   | 85.07%   |

## Logistic Regression Results

| S.NO. | Model    | C Value | Penalty | Test AUC | Precision Score |
|-------|----------|---------|---------|----------|-----------------|
|       | BOW      | 0.02    | L1      | 0.9500   | 97.52%          |
|       |          | 7       | L2      | 0.9255   | 96.71%          |
|       | TFIDF    | 0.02    | L1      | 0.9583   | 97.85%          |
|       |          | 50      | L2      | 0.9393   | 96.99%          |
|       | AVG W2V  | 0.08    | L1      | 0.9074   | 95.96%          |
|       |          | 0.05    | L2      | 0.9075   | 95.97%          |
|       | TFIDF W2V| 0.001   | L1      | 0.8831   | 95.33%          |
|       |          | 700     | L2      | 0.9303   | 97.01%          |

## LSTM Results

| S.NO. | Architecture                                | Epochs | Test Accuracy |
|-------|----------------------------------------------|--------|---------------|
| 1     | Keras LSTM (100)                             | 10     | 89.67%        |
| 2     | Keras LSTM (50)                              | 10     | 90.13%        |
| 3     | Keras LSTM (50) + Dropouts                   | 10     | 90.38%        |
| 4     | TensorFlow LSTM (128,32) + Dense (32,1) + Dropouts | 100    | 84.72%        |
| 5     | TensorFlow LSTM (128,64,32) + Dense (32,1) + Dropouts | 30     | 89.72%        |

## Naive Bayes Results

| S.NO | Vectorizer | Best Alpha | Test AUC | F1 Score |
|------|------------|------------|----------|----------|
| 1    | BOW        | 200        | 0.9015   | 91.82    |
| 2    | TFIDF      | 300        | 0.8936   | 91.95    |

## Linear SVM Results

| S.NO | Model | Alpha Value | Penalty | Test AUC | Precision Score |
|------|-------|-------------|---------|----------|-----------------|
| 1    | BOW   | 0.001       | L1      | 0.8991   | 95.70%          |
|      |       | 0.1         | L2      | 0.9322   | 96.95%          |
| 2    | TFIDF | 0.001       | L1      | 0.9000   | 83.98%          |
|      |       | 0.1         | L2      | 0.9462   | 97.04%          |
| 3    | AVG W2V | 0.001     | L1      | 0.8974   | 95.63%          |
|      |       | 0.01        | L2      | 0.9013   | 96.11%          |
| 4    | TFIDF W2V | 0.001   | L1      | 0.8760   | 95.53%          |
|      |       | 0.01        | L2      | 0.8777   | 95.34%          |

## RBF SVM Results

| S.NO | Model    | Alpha Value | Gamma   | Test AUC | Precision Score |
|------|----------|-------------|---------|----------|-----------------|
| 1    | BOW      | 0.001       | 0.00001 | 0.8841   | 96.
