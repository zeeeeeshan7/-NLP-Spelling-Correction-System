## Hybrid NLP Spelling Correction System (Python + NLP + GUI)

This project implements an intelligent spelling correction system capable of detecting and correcting both non-word errors (typos like “aspitin”) and real-word errors (context mistakes like “hearth attack” instead of “heart attack”).
It combines probabilistic language models, edit-distance scoring, semantic similarity, and a custom Tkinter GUI to create an interactive, domain-aware spell-checker.

Originally designed for medical text correction, this system uses a hybrid corpus of biomedical abstracts and general English sentences to improve contextual accuracy.

## Project Highlights

Detects both non-word and real-word errors

Hybrid corpora for improved domain & general language coverage

Combines:

Edit distance (Damerau–Levenshtein)

Unigram & bigram language models

Semantic similarity using GloVe embeddings

IDF weighting & POS-tagging

Fully interactive GUI text editor built with Tkinter

Ranks correction candidates based on a weighted scoring system

Handles context-dependent corrections using probabilistic inference

Displays suggestion lists, edit distances, error types, and scoring

## Core NLP Concepts Used
1. Edit Distance (Damerau–Levenshtein)

Used to generate candidate corrections within a 2-edit radius (insert, delete, substitute, transpose).

2. Language Models (Unigrams + Bigrams)

Probabilities are computed from both corpora.
Used to rank contextually plausible corrections.

3. Hybrid Corpus Approach

PubMed 200k RCT (biomedical domain)

Random English Sentences (general domain)

This avoids false positives in both medical and general sentences.

4. Semantic Similarity (GloVe Embeddings)

Cosine similarity ensures the candidate word fits the meaning of its local context.

5. POS-Tagging

Ensures that corrections match the grammatical category (noun → noun, verb → verb).

6. IDF Weighting

Gives more importance to medically relevant or less frequent terms.
