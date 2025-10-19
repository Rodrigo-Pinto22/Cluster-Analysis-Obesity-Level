# Cluster-Analysis

🧠 Cluster Analysis Project

This project aims to explore and compare different clustering methodologies — both hierarchical and non-hierarchical — applied to a simulated dataset related to lifestyle and obesity factors.
The analysis includes experiments with several distance metrics, linkage criteria, and evaluation indices, such as the Silhouette coefficient and Adjusted Rand Index (ARI).

📘 Overview

Clustering is an unsupervised learning approach used to identify natural groupings within data.
In this study, various algorithms are applied to simulated human data, where individuals are characterized by anthropometric and behavioral variables (e.g., weight, height, diet habits, and water intake frequency).
The objective is to evaluate the effectiveness and coherence of different clustering techniques under multiple configurations.

⚙️ Project Structure
📂 ClusterAnalysis/
│
├── 📄 README.md                # Project documentation
├── 📓 ClusterAnalysis.ipynb     # Main Jupyter Notebook with the full experiment
├── 📁 data/
│   └── obesity_simulated.csv    # Synthetic dataset used in the analysis
│
│
└── 📄 requirements.txt          # Python dependencies

🧩 Dataset Description

The dataset was manually simulated to represent three main groups of individuals:

Group	Description	Example Characteristics
Healthy	Normal weight, high water and vegetable consumption	Weight 55–70 kg, Height ~1.70 m
Overweight	Moderate excess weight, average habits	Weight 70–90 kg, moderate caloric intake
Obese	High weight, poor diet habits	Weight > 95 kg, low water/vegetable consumption
Variables Included:

Sex (categorical)

Age (years)

Weight (kg)

Height (m)

Family_History_Obesity (binary)

Freq_Water_Intake (1–4 scale)

Freq_Vegetable_Intake (1–4 scale)

Freq_Caloric_Food_Intake (1–4 scale)

🔬 Methodology

The analysis follows a systematic experimental design composed of three main stages:

1️⃣ Hierarchical Methods

Linkage criteria: single, complete, average, centroid, and ward

Distance metrics: euclidean, cityblock

Evaluation:

Silhouette Score

Adjusted Rand Index (ARI)

Heatmaps are generated to visually compare performance across all method–distance combinations.

2️⃣ Non-Hierarchical Methods

K-Means clustering

Determination of the optimal number of clusters via:

Elbow Method

Silhouette Score comparison

Comparison of results with hierarchical methods.

3️⃣ Visualization and Validation

Scatter plots with cluster centroids (real vs calculated)

Dendrograms for hierarchical clusters

Heatmaps comparing silhouette and ARI

Summary tables averaging metrics per method

📈 Evaluation Metrics
Metric	Description
Silhouette Score	Measures how similar an object is to its own cluster compared to others
ARI (Adjusted Rand Index)	Compares predicted clusters with true simulated groups
Cophenetic Correlation	Evaluates how faithfully the dendrogram preserves pairwise distances
Elbow Method	Estimates the optimal number of clusters by minimizing intra-cluster variance
💻 Technologies Used

Python 3.11+

Libraries:

numpy, pandas, matplotlib, seaborn

scipy, scikit-learn

jupyter (for interactive analysis)

🚀 Execution Instructions
1️⃣ Clone the repository:
git clone https://github.com/yourusername/ClusterAnalysis.git
cd ClusterAnalysis

2️⃣ Install dependencies:
pip install -r requirements.txt

3️⃣ Launch the Jupyter Notebook:
jupyter notebook ClusterAnalysis.ipynb

🧪 Results Summary

Ward linkage with Euclidean distance generally produced the most stable and coherent clusters and with the highest Silhouette

Distance metrics such as Minkowski showed comparable results but were more sensitive to outliers.

The Complete linkage method also achieved consistent results for smaller datasets.

The analysis confirmed the simulated group structure (Healthy, Overweight, Obese) and demonstrated the interpretability and stability of hierarchical clustering methods when properly parameterized.

📚 References

Kaufman, L., & Rousseeuw, P. J. (1990). Finding Groups in Data: An Introduction to Cluster Analysis. Wiley.

Jain, A. K. (2010). Data Clustering: 50 Years Beyond K-Means. Pattern Recognition Letters, 31(8), 651–666.

Rokach, L., & Maimon, O. (2005). Clustering Methods. In Data Mining and Knowledge Discovery Handbook. Springer.

Hennig, C. (2015). What Are the True Clusters? Pattern Recognition Letters, 64, 53–62.

Xu, D., & Tian, Y. (2015). A Comprehensive Survey of Clustering Algorithms. Annals of Data Science, 2(2), 165–193.

🧭 Future Improvements

Expand dataset with more variables (e.g., exercise frequency, BMI, diet score)

Evaluate clustering stability across random sampling

Explore PCA, t-SNE, or UMAP for low-dimensional visualization

✍️ Authors

[Rodrigo Pinto]
Master’s Student in Data Science
[university of Aveiro]
📧 [rodrigoaspinto@ua.pt]