# Distributional Semantics - Estimating Word Similarity

## Overview

This project focuses on learning word representations using distributional semantics techniques to estimate the similarity between term pairs. The goal is to develop both sparse and dense representations of words using a Wikipedia-based corpus and evaluate their effectiveness in capturing word similarities.

The similarity between words is assessed using cosine similarity, with the expectation that semantically similar words (e.g., desk, table) should have higher similarity scores compared to less related words (e.g., desk, wall).

## Tasks Implemented

### Task 1: Sparse Representation (Bag of Words - BoW)
Implemented a sparse vector representation using either:
- TF-IDF (Term Frequency-Inverse Document Frequency)
- Positive Pointwise Mutual Information (PPMI)

Computed cosine similarity between term pairs using the constructed representations.

### Task 2: Dense Representation (Word Embeddings)
Implemented dense vector representations using either:
- Word2Vec (Skip-gram or CBOW)
- GloVe (Global Vectors for Word Representation)

Trained embeddings from scratch using the provided Wikipedia dataset.
Calculated cosine similarity between term pairs.

## Dataset Used
**WikiText-103**
- A large-scale Wikipedia corpus consisting of over 100 million tokens.
- Used to train word representations without pre-trained embeddings.

## Example Term Pair Similarity File
- Contains 150+ term pairs with human-annotated similarity scores (ranging from 0 to 1).
- Used for model evaluation—ensuring that the computed similarity scores align with human judgments.

## Test Data
- Contains a new set of term pairs (without similarity scores).
- The goal is to compute cosine similarities for these pairs using both sparse and dense representations.
- Some terms include multi-word phrases, rare words, and ambiguous terms.

## Technologies Used
- Python
- Google Colab (for model training and evaluation)

### Libraries:
- **NLTK (Natural Language Toolkit)** – for text preprocessing
- **Gensim** – for Word2Vec and GloVe implementation
- **Scikit-learn** – for TF-IDF vectorization and cosine similarity computation
- **NumPy & Pandas** – for data handling and similarity calculations

# Multi-Class Multi-Label Movie Genre Classification

### Overview
This project focuses on multi-class multi-label classification of movie genres based on their plot synopses. The dataset consists of human-written and AI-generated movie plot summaries, and each movie is labeled with one or more genres from the following nine categories:

- Comedy
- Cult
- Flashback
- Historical
- Murder
- Revenge
- Romantic
- Sci-Fi
- Violence

Since each movie can belong to multiple genres, this task is classified as a multi-class, multi-label classification problem.

### Tasks Implemented

**Task 1: Traditional Deep Learning Approach**
- Implemented a Long Short-Term Memory (LSTM) or BiLSTM network.
- Used word embeddings (e.g., Word2Vec, GloVe, or FastText) for feature representation.
- Addressed class imbalance using techniques like class weighting and oversampling/undersampling.
- Optimized hyperparameters (dropout rate, learning rate, batch size) for better performance.

**Task 2: Fine-Tuning Pretrained Transformers**
- Fine-tuned a pretrained model (one of the following):
  - BERT (google-bert/bert-base-uncased)
  - T5 (google-t5/t5-base)
  - RoBERTa (FacebookAI/roberta-base)
- Implemented multi-label classification using sigmoid activation.
- Used TPUs available in Google Colab to accelerate training.
- Experimented with different learning rates, batch sizes, and tokenization strategies.

## Setup and Usage

1. **Clone the repository:**
   ```sh
   git clone <repository_url>
   cd <repository_directory>
   ```

2. **Install required libraries:**
   ```sh
   pip install -r requirements.txt
   ```

3. **Download the WikiText-103 dataset:**
   Follow the instructions provided [here](https://blog.einstein.ai/the-wikitext-long-term-dependency-language-modeling-dataset/) to download the dataset.

4. **Run the scripts:**
   Use Google Colab notebooks provided in the repository for training and evaluating the models.

## Evaluation
The evaluation process involves comparing the computed cosine similarity scores with human-annotated similarity scores to measure the effectiveness of the word representations.

## Contributions
Contributions are welcome! Please submit a pull request or open an issue for any changes or suggestions.

## License
This project is licensed under the MIT License.

## Contact
For any questions or inquiries, please contact Garry2546.
