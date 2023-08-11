# A hybrid anonymization pipeline to improve the privacy-utility balance in sensitive datasets for ML purposes

This repository contains the anonymization hierarchies, dataset, results and parameters used in the paper "A hybrid anonymization pipeline to improve the privacy-utility balance in sensitive datasets for ML purposes" presented at the 18th International Conference on Availability, Reliability and Security (ARES 2023).

## Abstract

The modern world is data-driven. Businesses increasingly take strategic decisions based on customer data, and companies are founded with a sole focus of performing machine-learning driven data analytics for third parties. 
External data sources containing sensitive records are often required to build qualitative machine learning models and, hence, perform accurate and meaningful predictions. However, exchanging sensitive datasets is no sinecure. Personal data must be managed according to privacy regulation. Similarly, loss of strategic data can negatively impact the competitiveness of a company. In both cases, dataset anonymization can overcome the aforementioned obstacles.

This work proposes a *hybrid anonymization pipeline* combining masking and (intelligent) sampling to improve the privacy-utility balance of anonymized datasets. The approach is validated via in-depth experiments on a representative machine learning scenario. A quantitative privacy assessment of the proposed hybrid anonymization pipeline is performed and relies on two well-known privacy metrics, namely re-identification risk and certainty. Furthermore, this work shows that the utility level of the anonymized dataset remains acceptable, and that the overall privacy-utility balance increases when complementing masking with intelligent sampling. 
The study further restrains the common misconception that dataset anonymization is detrimental to the quality of machine learning models. The empirical study shows that anonymous datasets – generated by the hybrid anonymization pipeline – can compete with the original (identifiable) ones when they are used as input for training a machine learning model.

## Repository Content

### Datasets

The **Datasets** folder contains the datasets that were used to obtain the results. The datasets are zipped due to size limitations. The **ACSIncome_USA_2018.csv** is the dataset where the target value (PINCP) is a binary value indicating an income higher than 50,000. The **ACSIncome_USA_2018_ub.csv** is the less balanced dataset with the target indicating an income higher than 100,000.

### Hierarchies
The **Hierarchies** folder contains the used hierarchy for each QID attribute.

### Results
The **Results** folder contains the complete set of experiments. The **ACSIncome** folder contains all results executed on the complete dataset, while the **ACSIncome_small** folder contains the results of the reduced dataset having 50,000 records.
Each of those two folders are structured as follows:
```
.
├── Sampling strategy
│   ├── k-value (k5, k10, k20, k40, k80, k160)
│   │   ├── β-value (β0.5, β0.25, β0.125, β0.0625, β0.03125, β0.015625)
│   │   │   ├── arx_stats.csv
│   │   │   ├── certainty.png
│   │   │   ├── journalist_risk.png
│   │   └── f1-....png
│   ├── f1-....csv
└── baselines.csv
```
When not applicable, certain folders are omitted (e.g., k-value in the "RSAMPLE (sampling_only)" and "l_diversity" folders).
The **baseline.csv** file lists the f1-scores when applying the machine learning model on the original S and S' datasets with and without balancing inside the machine learning pipeline.

### params.md

The **params.md** file lists some important parameters used both in the anonymization process and in the machine learning pipeline.
