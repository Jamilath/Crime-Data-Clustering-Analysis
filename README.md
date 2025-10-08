Crime Data Clustering Analysis
Project Overview
This repository contains the code, data, visualizations, and report for a data analytics project that applies K-means and Hierarchical clustering to group 50 U.S. states based on crime rates (Murder, Assault, Rape) and urban population (UrbanPop). The goal was to identify clusters, compare clustering methods, and draw inferences about crime patterns.
Dataset
The dataset (crime_data.csv) includes 50 U.S. states with four features:

Murder: Murder rates per 100,000 people (range: 0.8–17.4).
Assault: Assault rates per 100,000 people (range: 45–337).
UrbanPop: Percentage of urban population (range: 32–91).
Rape: Rape rates per 100,000 people (range: 7.3–46.0).

Methodology

Data Preprocessing: Standardized features to ensure fair clustering.
K-means Clustering: Applied with k=4 clusters, determined via an elbow plot.
Hierarchical Clustering: Applied with Ward’s method and Euclidean distance, k=4 determined via a dendrogram.
Comparison: Used Adjusted Rand Index (ARI = 0.8849) to assess method similarity.
Mismatch Analysis: Investigated boundary cases (Arkansas, Kentucky).

Results
Four clusters were identified:

Low-crime, rural states (e.g., Idaho, Maine): Low crime rates, low urban population.
High-crime, urban states (e.g., California, New York): High crime rates, high urban population.
Moderate-crime, urban states (e.g., Connecticut, Massachusetts): Moderate crime rates, high urban population.
High-crime, semi-urban states (e.g., Alabama, Georgia): Very high crime rates, moderate urban population.

Key Findings:

Crime patterns are tied to urbanization, with high-crime clusters in urban or semi-urban areas.
Southern semi-urban states face unique crime challenges.
High ARI (0.8849) confirms robust clustering results.
Mismatches (Arkansas, Kentucky) are boundary cases due to intermediate feature values.

Repository Contents

Data Files:
crime_data.csv: Original dataset.
scaled_crime_data.csv: Standardized dataset.
crime_data_kmeans.csv, scaled_crime_data_kmeans.csv: K-means results.
crime_data_hierarchical.csv, scaled_crime_data_hierarchical.csv: Hierarchical results.
combined_clustering.csv: Combined cluster assignments.


Code Files:
preprocess_data.py: Data standardization.
kmeans_clustering.py: K-means clustering and elbow plot.
hierarchical_clustering.py: Hierarchical clustering and dendrogram.
compare_clustering.py: Cluster comparison and scatter plots.
clustering_inferences.py: Cluster state lists and mismatches.
final_clustering_inferences.py: Corrected mismatch analysis.
cluster_size_chart.py: Cluster size bar chart.
additional_visualization.py: UrbanPop vs. Rape scatter plots.
updated_final_clustering_report.py: Final report generation.
mismatch_analysis.py: Mismatch analysis for Arkansas and Kentucky.


Visualizations:
elbow_plot.png: Elbow plot for K-means.
dendrogram.png: Dendrogram for Hierarchical clustering.
cluster_scatter_plots.png: Murder vs. Assault scatter plots.
urbanpop_rape_scatter.png: UrbanPop vs. Rape scatter plots.
cluster_sizes.png: Cluster size bar chart.


Reports:
clustering_inferences.txt: Cluster states and inferences.
mismatch_analysis.txt: Mismatch analysis for Arkansas and Kentucky.
final_clustering_report.txt: Comprehensive report.
clustering_report.tex: LaTeX source for PDF report.
clustering_report.pdf: Compiled PDF report.



How to Use

Run the Code:
Ensure Python dependencies: pandas, scikit-learn, matplotlib, seaborn.
Execute scripts in order: preprocess_data.py, kmeans_clustering.py, hierarchical_clustering.py, compare_clustering.py, clustering_inferences.py, final_clustering_inferences.py, cluster_size_chart.py, additional_visualization.py, mismatch_analysis.py, updated_final_clustering_report.py.


Generate PDF:
Compile clustering_report.tex using a LaTeX editor (e.g., Overleaf) or latexmk -pdf clustering_report.tex to produce clustering_report.pdf.


Review Results:
Check visualizations (*.png) for cluster analysis.
Read final_clustering_report.txt and mismatch_analysis.txt for detailed findings.



Limitations

The choice of k=4 was assumed; elbow plot and dendrogram descriptions could confirm this.
Limited to four features; additional variables (e.g., income, education) could enhance clustering.
Mismatched states (Arkansas, Kentucky) warrant further investigation.

Contact
For questions, contact [Your Name] at [Your Email].
