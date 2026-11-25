# Movie Recommendation and Ranking: Top-N Ranking with a Deep Interest Network

Collaborative project with Han Han (orginal repo: https://github.com/Hannnnnnn404/CSC580-Final-Project).

**My contributions:**
- Implemented item-based collaborative filtering as baseline
- Designed time-based train/test splits for deep interest network to prevent look-ahead leakage
- Built ranking evaluation framework
- Outlining the online A/B test design (coming soon!)

## Problem
Recommend the top-N movies a user is most likely to engage with next, and test whether a sequence-aware model beats a simple baseline

## Data
MovieLens 1M (1M+ ratings, ~6K users, ~4K movies)

## Approach
- **Baseline:** item-based collaborative filtering (CF/Item_Based_Similarity_CF.py)
- **Model:** Deep Interest Network (DIN), which weights a user's past interactions by relevance to each candidate item (DIN/train.py)
- **Evaluation:** time-based splits so the model never trains on "future" interactions (Evaluation/Evaluation.py)

## Results
| Metric      | Baseline (item CF) | DIN  |
|-------------|--------------------|------|
| Precision@5 | 0.65               | 0.70 |
| NDCG@5      | 0.65               | 0.71 |
| MAP         | 0.54               | 0.58 |


