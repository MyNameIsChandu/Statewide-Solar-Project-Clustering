# Statewide Solar Project Clustering Analysis

## 📌 Project Overview
This project analyzes statewide solar project data to understand regional solar adoption patterns.  
Using unsupervised learning techniques, counties are segmented based on solar system capacity, energy production, storage adoption, and project volume. The goal is to identify meaningful regional clusters that can support data-driven planning, policy-making, and investment decisions in the renewable energy sector.

---

## 📊 Dataset Overview
- The dataset contains **218,115 solar project records** with **17 features**.
- Includes technical, geographic, and operational attributes such as:
  - PV system size (kWdc & kWac)
  - Estimated annual energy production (kWh)
  - Energy storage system size
  - Number of projects
  - City, county, utility, and division information
- Data represents **statewide solar installations** across multiple regions.

---

## ⚙️ Data Preprocessing
- Selected **key numerical features** relevant to solar capacity and deployment:
  - Estimated PV System Size (kWdc)
  - PV System Size (kWac)
  - Estimated Annual PV Energy Production (kWh)
  - Energy Storage System Size (kWac)
  - Number of Projects
- Aggregated data at the **county level** to enable regional analysis.
- Applied **log transformation** to handle right-skewed distributions and reduce the impact of extreme values.
- Scaled features using **Min-Max Scaling** to ensure equal contribution in distance-based clustering.
- No explicit missing value imputation was performed, as aggregation naturally reduced sparsity.

---

## 🔍 Exploratory Data Analysis (EDA)
- Identified **high right-skewness** in system size, energy production, and project count.
- Observed **strong positive correlations** between system capacity and energy generation.
- Found **uneven solar adoption** across counties, with a small number of regions dominating installations.
- EDA results directly motivated **feature transformation, scaling, and clustering**.

---

## 📈 Data Visualization
- Histograms to analyze feature distributions.
- Correlation heatmap to understand relationships between numerical variables.
- Scatter plots to examine system size vs energy production.
- Bar charts to highlight top counties by solar project count.
- PCA-based 2D visualization to interpret clustering results.

---

## 🤖 Model Selection
- The problem was treated as an **unsupervised learning task** due to the absence of labeled outcomes.
- **K-Means clustering** was chosen for its efficiency and interpretability on large numerical datasets.
- The **Elbow Method** was used as an initial reference but was inconclusive.
- **Silhouette Score** was used for final model evaluation.
- The highest silhouette score was observed at **k = 2**, indicating optimal cluster separation.

---

## 💡 Key Insights
- Counties naturally separate into **two distinct solar adoption patterns**.
- **Cluster 0 – Residential Solar Counties**:
  - Smaller PV system sizes
  - Lower energy output per system
  - Very high number of installations
  - Dominated by residential and small-business solar
- **Cluster 1 – Commercial & Utility Solar Counties**:
  - Much larger PV system sizes
  - High annual energy generation
  - Fewer but more powerful installations
  - Dominated by commercial, municipal, and utility-scale solar
- Solar deployment is **highly uneven across regions**.
- Energy storage adoption remains limited and concentrated in high-capacity regions.

---

## ✅ Conclusion
This project demonstrates how unsupervised learning can transform raw solar installation data into actionable regional insights. By segmenting counties into residential-focused and utility-scale solar regions, the analysis provides a clear framework for targeted solar expansion, storage planning, and renewable energy policy decisions.

---

## 🚀 Future Scope
- Perform **time-based analysis** to study solar adoption trends over the years.
- Use **finer geographic resolution** (city or ZIP-level clustering).
- Compare results with other clustering techniques such as Hierarchical Clustering and DBSCAN.
- Incorporate **policy, economic, and demographic factors**.
- Build predictive models to **forecast future high-growth solar regions**.

---

## 🛠️ Technologies Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- K-Means Clustering
- PCA

---

## 📬 Contact
For questions or collaboration, feel free to connect via GitHub.
