# Circular-trade-Fraud-Detection
This project focuses on leveraging multi-graph representation techniques for fraud detection. The dataset given is iron dealers data which contains information about invoices between sellers and buyers and the value of transaction. Each row in the dataset represents one invoice and contains the following information

## Methodology
- **Directed Graph Construction**: The multi-graph is converted into a directed graph with edge weights.
- **Suspicion Score Calculation**: We calculate the amount of fraudulence using a function that derives suspicion scores based on the count of 2-cycles and 3-cycles, as well as the trading amount between pairs of traders. These scores are stored using hash functions on corresponding cycle nodes.
- **Undirected Graph Construction**: An undirected graph is then constructed based on suspicion scores and the number of 2-cycles and 3-cycles between nodes.
- **Node Embeddings and Clustering**: Node2Vec is utilized to learn embeddings for nodes in the undirected graph. The DBSCAN algorithm is applied to identify dense regions of nodes, indicating potential fraudulent behavior.

### Results 
