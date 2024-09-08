# Predicting Death Event in Heart Failure Patients using Machine Learning

This project involves predicting death events in patients using machine learning techniques. The dataset utilized is the "heart_failure_clinical_records_dataset.csv," which contains various clinical features of patients along with the target variable DEATH_EVENT. The dataset includes the following features:


** age: ** Age of the patient

** anaemia: ** Whether the patient has anaemia (1: Yes, 0: No)

** creatinine_phosphokinase: ** Level of creatinine phosphokinase in the blood

** diabetes: ** Whether the patient has diabetes (1: Yes, 0: No)

** ejection_fraction: ** Percentage of blood pumped out of the heart with each heartbeat

** high_blood_pressure: ** Whether the patient has high blood pressure (1: Yes, 0: No)

** platelets: ** Platelet count in the blood

** serum_creatinine: ** Serum creatinine level in the blood

** serum_sodium: ** Serum sodium level in the blood

** sex: ** Gender of the patient (1: Male, 0: Female)

** smoking: ** Whether the patient is a smoker (1: Yes, 0: No)

** time: ** Follow-up period

** DEATH_EVENT: ** Target variable indicating if the patient died during the follow-up period (1: Yes, 0: No)


** Clustering Analysis **


The project applies several clustering techniques to the dataset to identify patterns and clusters within the data. The following clustering methods were used:

** K-Means Clustering: **

K-Means was applied to the dataset after scaling the features.
The optimal number of clusters was determined using the Elbow method.
Results showed that K-Means clustering creates spherical clusters, but did not significantly differentiate between high and low-risk patient groups based on the DEATH_EVENT rates.

** Kernel K-Means Clustering: **

Kernel K-Means was performed after applying Kernel PCA for dimensionality reduction.
This method transforms the data into a higher-dimensional space to find non-linear clusters.
Kernel K-Means identified clusters with more pronounced differences in DEATH_EVENT rates compared to K-Means and EM, suggesting potential clinical significance.


** Expectation Maximization (EM) Clustering: **

EM clustering was used to identify clusters based on a mixture of Gaussian distributions.

The clusters from EM were found to be similar to those from K-Means, with no substantial differences in the DEATH_EVENT rates.


** Evaluation Metrics **
Silhouette Score: Used to measure the quality of clustering:

K-Means: 0.1179

Kernel K-Means: 0.3398 

EM: 0.1183

Kernel K-Means achieved the highest silhouette score, indicating better-defined clusters compared to K-Means and EM.

** Clinical Significance **

K-Means: Both clusters had similar DEATH_EVENT rates, indicating that K-Means did not distinguish high-risk groups effectively.

Kernel K-Means: Identified a cluster with a higher DEATH_EVENT rate, suggesting better potential for predicting high-risk patients.

EM: Similar to K-Means, with minimal differences between clusters.

** Conclusion **

Kernel K-Means clustering showed the most promise in differentiating patient groups based on the risk of death. The other clustering methods did not reveal as clear distinctions. The insights from this project could help in identifying high-risk patient groups and potentially guide further research or clinical interventions.

