# ML System Design – Enhancing Ad Ranking with User Clustering

This project demonstrates how user clustering can improve a social media ad ranking system. Using simulated user behavior data from a fictional platform called ConnectHub, it builds an unsupervised learning pipeline that groups users based on their ad interaction patterns.

The resulting cluster_id feature is designed to be integrated into the ad ranking model to improve Click-Through Rate (CTR) and conversion rate.

***1. Overview***

Traditional ad ranking systems rely heavily on individual user features such as demographics or recent clicks.
This project adds a new dimension by grouping users into behavioral clusters, allowing the ranker to learn from similar users and make more informed predictions.

Goals

- Cluster users based on engagement metrics (CTR, reactions, time spent, etc.)

- Add cluster_id as a new feature for the ad ranker

- Evaluate its impact through A/B testing on key ad KPIs

***2. Project Structure***
- user_profiling.ipynb      # Main notebook: data processing, clustering, and analysis
- README.md                 # Project documentation

***3. How to Run***

Open user_profiling.ipynb in Google Colab.

Mount Google Drive and unzip the dataset:

from google.colab import drive
drive.mount('/content/drive')
!unzip "/content/drive/MyDrive/user_profiles-1.zip" -d /content/unzipped_folder


Run all cells in order to reproduce preprocessing, PCA, clustering, and visualizations.

Outputs include:

- PCA projections

- Elbow method plot

- Cluster feature comparison tables

- Heatmaps showing user behavior differences

***4. Results***

Optimal number of clusters: 5

Highest-value group: Cluster 3 (Power Users / Influencers) – highest CTR and engagement

Practical use: Add cluster_id to the ad ranker to improve targeting efficiency and ad performance

***5. Tech Stack***

Language: Python

Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

Compute Environment: Google Colab

Storage: Google Drive

***6. Acknowledgments***

Thanks to Arman Kharwal for providing this dataset and to Notion for offering an intuitive platform for documenting this project.
