# Disinformation Dynamics on Twitter (X)

This project analyzes how disinformation spreads on the social media platform X (formerly Twitter) using the Truthseeker23 dataset. It includes over 134,000 tweets and 21,000 retweet interactions, with nearly half labeled as false information.

## Project Overview

Using **NetworkX** for social network analysis and **VADER** for sentiment analysis, this study uncovers how false information propagates faster within tightly connected communities, amplified by influential users and negative sentiment.

The analysis explores graph structures, sentiment impact, and the speed of disinformation spread through the network.

The analysis integrates several techniques, including:

- Construction and visualization of retweet interaction graphs  
- Calculation of centrality measures (degree, betweenness, eigenvector) to identify influential nodes  
- Community detection and modularity analysis to understand cluster-based propagation  
- Sentiment scoring of tweets using VADER to assess emotional tone and its impact on spread  
- Temporal analysis of tweet and retweet timestamps to compare diffusion speed of false vs. true information  
- Logistic regression modeling to explore relationships between network metrics, sentiment, and likelihood of disinformation spread

## Usage

The core analysis is implemented in the Jupyter notebook `Truthseeker23.ipynb`.  

**Note:** To run this notebook, the Truthseeker23 dataset is required. The dataset must be cleaned and preprocessed as outlined in the notebook before executing the script.

## Dataset Credit

This project uses the Truthseeker23 dataset:

S. Dadkhah, X. Zhang, A. G. Weismann, A. Firouzi, and A. A. Ghorbani.  
2023. *The Largest Social Media Ground-Truth Dataset for Real/Fake Content: TruthSeeker.*  
IEEE Transactions on Computational Social Systems, 99, 1–15 (Oct. 2023).  
[https://www.unb.ca/cic/datasets/truthseeker-2023.html](https://www.unb.ca/cic/datasets/truthseeker-2023.html)

## License

This project is licensed under the MIT License — see the (License) file for details.
