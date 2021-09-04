# Anomaly

Description: Amazon web services is utilized by a large amount of people. Sometimes malicious attackers or curious individuals target these services. This can overload the system architecture. In AWS dataset, CPU utilization, disk writes, and network counts are measured. Due to the sparcity of certain time frames, I located the most attributes that are measured at the same exact time: CPU, ELB and network. This allows a merge without a high number of NaN entries. On a side note, ELB is elastic load balance measurement. This assists with over load of the current server. Based on these three attributes, do spikes in each attribute show anomalous behavior?

Location: Data Science Graduate Course at KU

Dates: Oct 23, 2018 to Oct 25, 2018

## Goal
Determining if CPU utilization, elastic load balance and/or network usage spike (a.k.a., anomaly detection).

## Data
Amazon Web Services Cloud Watch logs normalized to contain CPU and network utilization as well as the elastic load balance.

## Analysis
* Used Google Facets to locate empty values
* Within Python and Jupyter Notebooks, I normalized the values scale (0 to 1).
* Developed LOF and Isolation Forests model
* Visualized clusters with 2D and 3D scatter plots via matplotlib

## Results
LOF provides a score based on density. With the recorded CPU, ELB and networking measurements in March, a few outliers can be seen. This is shown in the data. Isolation Forests need more tweaking due to this data. By plotting the default function, only one cluster is seen as benign. Since this is unsupervised learning, altering the parameters leads to learning about the data layout.

## Repository Contents

| Directory | Description |
| --- | ----------- |
| Data | Contains all of the datasets used in this project. |
| Notebooks | Notebooks used for visualing the data. |


