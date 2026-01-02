# Disinformation Dynamics on Twitter (X)

This project investigates the structural and temporal mechanisms of disinformation propagation on the social platform X (formerly Twitter). Leveraging the Truthseeker23 dataset (134k+ tweets, 8.8M+ projected edges), this research quantifies how emotional valence and network topology accelerate the spread of false information.

## Summary

- Propagation Speed: Disinformation spreads nearly twice as fast as real news, with a mean retweet rate of 0.0083 vs 0.0044 retweets per day.
- Echo Chambers: The study confirmed a high "modularity" (0.833), meaning disinformation is almost entirely contained within isolated, tightly-knit communities, rarely crossing over into broader network clusters.
- Influence Gap: Fake tweets are significantly more "central" to their networks, exhibiting a 60% higher connectivity rate than real tweets, suggesting they leverage key influential hubs to gain traction.
- Emotional Drivers: Negative sentiment (found in 54% of fake tweets) was identified as a primary catalyst for network amplification and increased virality.

## Project Overview

### 1. Network Structure & Community Detection

I constructed a model representing the interactions between authors and tweets to map the flow of information. Using the Louvain algorithm, I partitioned the network into over 113,000 distinct communities to measure how "insular" disinformation clusters are compared to the rest of the network.

### 2. Influence & Centrality Modeling

I applied multiple metrics to identify the "super-spreaders" of the network:

Degree Centrality: To measure immediate reach.
K-Clique Analysis: To identify the core "inner circles" where disinformation is most dense.
Bipartite Projection: To connect tweets based on shared authorship, revealing how specific actors dominate certain narratives.

### 3. Sentiment & Temporal Analysis

Linguistic Scoring: Used VADER to quantify the emotional tone of 134k+ tweets, correlating negative sentiment with higher retweet rates.
Velocity Calculations: Created a custom metric to track the speed of spread relative to the time of posting, allowing for a direct comparison of "virality decay" between real and fake information.

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
