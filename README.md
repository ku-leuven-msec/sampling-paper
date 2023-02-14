# sampling-paper

This repository contains the anonymization hierarchies, dataset and parameters used in the paper "Improving the privacy-utility balance with advanced sampling techniques".

## Abstract

The modern world is data-driven. Businesses increasingly make strategic decisions based on customer data, and companies are founded with a sole focus of performing data analytics (e.g. machine learning) for third parties. 
In most cases, data from external sources is required in order to perform accurate and meaningful predictions. This data is often of a sensitive nature, containing personal data in which case the GDPR regulation should be respected or sensitive company data that could undermine the competitive advantages of the respective company when leaked. In both cases, dataset anonymization can serve as a means to overcome these obstacles.
This work combines two well-known techniques for data anonymization, namely (1) the application of privacy models and (2) data sampling. Privacy models such as $k$-anonymity ensure that an individual can no longer be linked to one specific record in the dataset, while sampling further decreases the risk of a successful re-identification attack by reducing the certainty of potential attackers. A privacy assessment of the proposed data anonymization strategy is presented, both in terms of anonymity level (e.g. $k$-value) as in terms of the risk of a record being re-identified and the certainty of an attacker. Furthermore, this work ensures that not only the privacy level but also the utility level of the anonymized dataset remains desirable. An extensive test methodology is presented that applies the anonymized datasets in the context of a machine learning use case.  The utility of the anonymized data is measured by assessing the quality of the machine learning model created with the anonymized data.

## Repository Content

### Datasets

The **Datasets** folder contains the datasets that were used to obtain the results. The datasets are ziped due to size limitations. The **ACSIncome_USA_2018.csv** is the dataset where the target value (PINCP) is a binary value indicating an income higher than 50,000. The **ACSIncome_USA_2018_ub.csv** is the less balanced dataset with the target indicating an income higher than 100,000.

### Hierarchies
The **Hierarchies** folder contains the applied hierarchy for each QID column. Each hierarchy has the same name of the corresponding column.

### params.md

The **params.md** file lists some important parameters used both in the anonymization process and in the machine learning pipeline.