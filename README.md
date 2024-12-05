# **POLARIZATION ON REDDIT: COMPLEXITY, SENTIMENT, AND POPULARITY**
By Rasmus Høgh Gregersen (s204313), Daniel Damkjær Ries (s214641), Kalle Emil Leander Johansen (s204099), Thor Nørgaard Eriksen (s204618)

## **Overview**
This project analyzes Reddit comments to explore how linguistic complexity, sentiment, and engagement interact in polarizing discussions. Using comments from subreddits like \textit{/r/Israel} and \textit{/r/Palestine}, we examine how readability (LIX score), sentiment (positive, negative, neutral), and popularity (upvotes) influence user interactions. By uncovering these patterns, the project sheds light on the dynamics of divisive online conversations.

## **Key Features**
Scrapes comments from selected subreddits using the PRAW library.
Processes text data to calculate linguistic complexity (LIX score), sentiment, and other metrics.
Clusters comments based on sentiment, upvotes, and readability.
Visualizes results using word clouds, scatter plots, and cluster summaries.

## **Running the code**
To get new data, you will have to set up an app in the developers section of Reddit to get a client id and client secret for the PRAW library in Python. In the data_extract.ipynb these values have to be put in at the top, and in the bottom the desired subreddit and search query can be chosen.

In the data folder, there is already extracted more than 16,000 comments from different relevant subreddits for the Israel/Palestine topic. Also, comments from the "baking" subreddit are included as a baseline. They are saved as subreddit_search-query.csv.

To load the data and run the preprocessing go to data_processing.ipynb and run the cells. Here the LIX and sentiment score are also calculated and added to the dataframe and saved as a new csv. These are saved as subreddit_w_lix_sentiment.csv.

To cluster the data, go to clustering.ipynb and run the cells. Here the preprocessed data is loaded and different types of clustering is applied. The dataframe with assigned clusters are saved as subreddit_clustered.csv. 

Finally, the analysis of the clusters for each subreddit can be accessed in cluster_analysis.ipynb. By choosing subreddit at the top and running the cells below in this notebook, numerical analysis of the clusters and wordclouds are shown. 
