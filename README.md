# employee-clustering-analysis
Unsupervised learning project analyzing employee data to identify clusters based on compensation, years of experience, and job mobility. Includes cluster profiling, insights, and recommendations for HR strategy.

Overview
This project performs unsupervised learning on employee data to identify natural clusters and patterns based on salary (CTC), years of experience, and job update behavior. The goal is to understand workforce distribution, role-specific compensation, and employee growth patterns.

Dataset
Contains anonymized employee records from multiple companies.
Key features:
ctc_capped – Employee compensation (capped)
YOE_capped – Years of experience (capped)
job_position – Employee role/title
company_hash – Anonymized company identifier
no_of_ctc_update – Number of compensation updates
Manual flags for designation, class, and tier (used for evaluation)
Methodology
1. Data Preprocessing
Removed manual cluster flags to avoid bias.
Encoded categorical variables (frequency encoding for company and job position).
Log-transformed skewed salary data (ctc_capped) to normalize distributions.
Standard scaled features for clustering.
2. Clustering Analysis
Hopkins Statistic: 0.983 → strong clustering tendency.
Elbow Method: Optimal number of clusters = 5.
K-Means Clustering:
Cluster labels assigned to all employees.
WCSS = 362,131.63 (compact clusters)
BCSS = 405,340.06 (well-separated clusters)
Hierarchical Clustering: Dendrogram inspected for natural breakpoints.
PCA: Reduced dimensions to 2 components for visual inspection.
Cluster Profiles
Cluster	Avg CTC (₹)	Avg YOE	Avg CTC Updates	Top Job Positions	Key Insight
0	9.2 L	10 yr	1.09	FullStack, Frontend, Other	Mid-level professionals, largest group (33%)
1	13.1 L	9.6 yr	2.34	Backend, FullStack, Unknown	Active job switchers, good salary growth (20%)
2	34.4 L	18 yr	1.12	Engineering Leadership, FullStack, Other	Senior leaders, highest salaries (15%)
3	16.8 L	10.2 yr	1.0	Backend, Unknown, FullStack	Stable mid-level backend professionals (26%)
4	8.1 L	9 yr	1.54	Unknown, Backend, Other	Lowest salary group, smallest cluster (6%)
Additional Observations:

Salary and experience distributions vary widely across clusters.
Cluster 2 contains highly experienced senior leaders.
Cluster 1 shows employees with frequent compensation updates, indicating potential job changes.
Most employees fall into mid-experience and mid-salary clusters.
Insights & Recommendations
Insights
Data Scientists and Engineering Leadership roles tend to have higher CTC compared to other roles.
Mid-level developers (Cluster 0 & 3) make up the majority of the workforce.
Frequent job movers (Cluster 1) indicate areas where retention strategies may be needed.
Highly experienced senior leaders (Cluster 2) are small in number but account for the highest salaries.
Some clusters overlap, highlighting the diversity of employee experience-salary combinations.
Recommendations
HR Strategy: Focus retention programs for Cluster 1 employees to reduce turnover.
Salary Benchmarking: Use Cluster 2 as reference for senior-level compensation planning.
Role-Specific Insights: Tailor career growth and compensation policies for different clusters.
Recruitment & Upskilling: Hire or train mid-level employees to prepare them for senior leadership roles.
Future Analytics: Include additional features (performance rating, tenure, department) to refine clusters.
Technologies & Libraries
Python: pandas, numpy, matplotlib, seaborn
Scikit-learn: KMeans, StandardScaler, PCA
Yellowbrick: KElbowVisualizer
SciPy: hierarchical clustering





