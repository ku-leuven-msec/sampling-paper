# anonymization parameters (ARX)
* k-value's = {5, 10, 20, 40, 80, 160}
* sample sizes = {0.015625,0.03125,0.0625,0.125, 0.25, 0.50}
* suppression limit = 1.0
* quality metric = Loss with arithmetic mean aggregation
* generalization/suppresion weight = 0.5
* QID = ["AGEP","COW","SCHL","MAR","OCCP","POBP","SEX","RAC1P"]

# machine learning parameters (sklearn)
* model = GradientBoostingClassifier
* loss = exponential
## categorical attributes pipeline
* ordinal encoding with unknown value set to -1
## numerical attributes pipeline
* transformation of ranges to mean values
* standard scaler
