# Machine learning for sub-seasonal pattern-based precipitation prediction
The repository includes codes for a benchmarking sub-seasonal pattern-based precipitation prediction model as well as feature selection using Random Forest model, including two folders:
1) `DataProcess`: create the target data and all possible features used for prediction
- `ClusterSelect.ipynb`/`Cluster_CESM.ipynb`: Derive monthly and seasonal precipitation regional patterns as the prediction target based on K-means clustering analysis, using precipitation data from observation `EOBS` and the ensemble earth system model `CESM` respectively;
- `EOF_slp.ipynb`/'EOF_sst.ipynb'/'eof_u200.ipynb'/'eof_z500.ipynb': pre-process `sea level pressure`, `sea surface temperature`, `U200`, `Z500` from CESM ensemble and conduct EOF analysis to create features;
- `NAO.ipynb`: calculate seas surface temperature anomalies in a North Atlantic and the annual NAO index
2) `FeatureEngineering`:
- `FeatureEngineering.ipynb`: The script collects all types of pre-processed features  and outputs a feature set with all 235 features and corresponding values;
- `feature_selection.ipynb`: The script uses the selected features to run feature selection models -- 1) hyperpatameter selection for the random forest model; 2) feature selection for Recursive feature elimination-Random Forest (REF-RF) and Monte Carlo-Random Forest (MC-RF); 3) model performance evaluation for RFE-RF and MC-RF model; And visualization of the evaluation scores.
# Dataset preparation: Both observation dataset and earth system model data were used for model feature engineering and prediction
- Precipitation: collected from both `EOBS` as observation and `CESM` earth system model simulation;
- Other climate variables: collected from `CESM` earth system model simulation.
- `CESM` dataset refers to https://www.cesm.ucar.edu/;
- `EBOS` dataset refers to https://www.ecad.eu/download/ensembles/download.php

