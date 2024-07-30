# Lexical Substitution with Contextual and Non-Contextual Embeddings in NLP

This project demonstrates lexical substitution using both non-contextual and contextual word embeddings, evaluated on the Stanford Word Substitution Benchmark (SWORDS).

## Project Overview

This project showcases a hands-on approach to lexical substitution by implementing and comparing various NLP techniques:

- **Non-Contextual Embeddings**: FastText, Word2Vec, WordNet
- **Contextual Embeddings**: XLM-RoBERTa

The aim is to generate substitute words for given target words within specific contexts and evaluate the performance of each method.

## Methodology

For a given context and a target word to be replaced, the following NLP techniques were used:

1. **Pre-trained word embeddings**: Using FastText, Word2Vec, and GloVe to find nearest words by cosine similarity.
2. **WordNet hierarchy**: Finding nearly synonymous words.
3. **Pre-trained transformer language models**: Predicting candidates using masked language modeling with XLM-RoBERTa.

### Data Preprocessing and Filtering

The generated candidate words were filtered and normalized using the following steps:
- Discarding non-alphanumeric artifacts
- Stripping whitespace
- Replacing underscores with spaces
- Lowercasing all words
- Lemmatizing using spaCy

### Evaluation

The models were evaluated based on the number of valid substitutes generated for each context in the test set. A substitute was considered correct if it received at least two positive votes in the ground truth data.
