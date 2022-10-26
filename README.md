# VU-subjectivity-mining-2022

This repository has the code for the final assignment for Subjectivity Mining (as taught at the Vrije Universiteit Amsterdam in 2022). 

Group members: Rorick Terlou, Marije Brandsma, Alice Ye, Dorien Renting

There is code for four components: hard-majority voting ensemble, soft-majority voting ensembe, stacked ensemble and a correlation analysis.

We have not included the code for training (fine-tuning) the three individual models, as this was already part of the previous assignment. The predictions of these models on the test data are included, so the code cn be ran without the need to train these models first. 

**Hard-majority and soft-majority voting ensembles**: See SVE_HVE_ensembles.ipynb. This uses the predictions from the finetuned individual models. This also saves the predictions of the individual models and the HVE and SVE to one csv file (ensemble_output_all_models.csv). 

**Stacked ensemble**: See SGE.ipynb and add_features.ipynb. Run add_features.ipynb first. This saves the features to a csv file for each dataset. SGE.ipynb uses the predictions from the finetuned individual models. It adds the predictions from the meta model to the file with all predictions (ensemble_output_all_models.csv). 

**Correlation analysis**: See correlation_analysis.ipynb. This uses ensemble_output_all_models.csv.


Before running the code, place OLID training and test data, HASOC training data, hatebase lexicon and glove twitter embedding model (100d) in data folder.
