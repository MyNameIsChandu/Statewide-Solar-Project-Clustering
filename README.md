🌞 Statewide Solar Project Clustering Analysis
📌 Project Overview

This project analyzes statewide solar installation data to understand regional solar adoption patterns. Using unsupervised machine learning (K-Means clustering), counties are segmented based on solar capacity, energy production, storage size, and project volume.

The goal is to transform raw solar project data into actionable insights that can support policy planning, infrastructure development, and renewable energy investment decisions.

📊 Dataset Overview

Total Records: 218,115

Total Columns: 17

Data Type: Mixed (Numerical + Categorical)

Key Columns:

Project and timeline details (Project ID, Interconnection Date)

Geographic information (City, County, Zip, Utility, Division)

Technical features:

Estimated PV System Size (kWdc)

PV System Size (kWac)

Estimated Annual PV Energy Production (kWh)

Energy Storage System Size (kWac)

Number of Projects

🛠 Data Preprocessing

Selected key numerical features relevant to solar capacity and deployment:

PV system sizes

Energy production

Storage capacity

Project count

Aggregated data at the county level to enable regional analysis.

Applied log transformation to reduce right-skewness and handle extreme values.

Scaled features using Min-Max Scaling to ensure equal contribution in distance-based clustering.

Explicit missing value imputation was not performed, as aggregation reduced sparsity in selected features.

🔍 Exploratory Data Analysis (EDA)

Analyzed missing value patterns, identifying structured missingness in storage-related fields.

Examined distributions of numerical features, observing strong right-skewness.

Performed correlation analysis, confirming strong relationships between system size and energy production.

Conducted regional analysis, revealing uneven solar adoption across counties.

EDA findings directly motivated feature transformation and scaling.

📈 Data Visualization

Missing value heatmaps

Histograms of solar system size and energy production

Scatter plots showing system size vs energy output

Correlation heatmaps of numerical features

Bar charts of top counties by solar project count

PCA-based cluster visualization

🤖 Model Selection

The problem was treated as an unsupervised learning task due to the absence of labeled outcomes.

K-Means clustering was selected for its:

Simplicity and interpretability

Efficiency on large numerical datasets

Suitability after scaling

Model evaluation methods:

Elbow Method (supporting analysis)

Silhouette Score (final decision)

The silhouette score peaked at k = 2, indicating optimal cluster separation.

📌 Key Insights
🔹 Cluster 0 – Residential Solar Counties (23 Counties)

Smaller PV system sizes

Lower annual energy output

Very high number of installations

Dominated by residential, rooftop, and small-business solar

Ideal for home battery programs and community solar initiatives

🔹 Cluster 1 – Commercial & Utility Solar Counties (39 Counties)

Much larger PV system sizes

High annual energy generation

Fewer installations but significantly higher capacity

Represents commercial, municipal, and utility-scale solar

Ideal for grid-scale storage and industrial solar projects

✅ Conclusion

Statewide solar adoption shows clear regional segmentation.

Solar deployment is uneven, with residential-heavy and utility-scale regions.

System size strongly drives energy production.

Unsupervised clustering successfully converted raw solar data into meaningful regional insights.

The project demonstrates the effectiveness of K-Means clustering for renewable energy analysis.

🚀 Future Scope

Add time-based analysis to study solar adoption trends over years.

Use finer geographic resolution (city or ZIP-level clustering).

Compare multiple clustering algorithms (Hierarchical, DBSCAN, GMM).

Incorporate policy, demographic, and socio-economic factors.

Build predictive models to forecast future high-growth solar regions.

🧰 Tools & Technologies Used

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

K-Means Clustering

PCA
