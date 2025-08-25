# The XGBoost Berm Breakwater Recession Prediction tool

Welcome to The XGBoost Berm Breakwater Recession Prediction tool, a web-based application developed using machine learning and the XGBoost method. This tool provides accurate and efficient predictions of berm breakwater recession based on a comprehensive dataset and carefully selected input parameters.

## Overview

This project is designed to predict the recession of berm breakwaters using the XGBoost machine learning model. The model uses a dataset split into 70% for training, 15% for validation, and 15% for testing, achieving R-squared statistics of 0.99 for training and 0.97 for testing. For more details, refer to the article by Zarbipour et al. (2025).

## Data Range and Parameters

The model uses the following dimensionless input parameters:

- **Rec/Dn50**: 0.12 – 25.4 (Output)
- **H0√T0p**: 5.8 – 35.8 (Input)
- **H0**: 1.1 – 6 (Input, units: m)
- **fg**: 1 – 1.8 (Input)
- **h/Dn50**: 7.2 – 26.5 (Input)
- **hb/Hs**: 0 – 3.1 (Input)

The model does not apply the effect of the dimensionless parameter *fn*, where *N* (number of waves) is set to 3000. The *fn* parameter, as presented by Akbari et al. (2022), accounts for the effect of previous waves on berm breakwater recession.

## Model and Prediction Approach

The XGBoost method was chosen for its high predictive accuracy and efficiency with large datasets, particularly suited for regression tasks and capturing complex non-linear relationships. A Bootstrap approach is employed to estimate prediction uncertainty by repeatedly sampling the training data with replacement and training multiple XGBoost models. The standard deviation of the predictions quantifies variability, and a 95% confidence interval is calculated as `prediction ± 1.96 × standard deviation`. An upper bound prediction (`prediction + standard deviation`) is also provided for conservative estimates, approximately at the 84th percentile.

For detailed guidance, refer to the [User & Technical Manual](https://coastalhydlab.ir/software/xgb-bbrp/manual).

## Downloads

- [Download the Software](https://coastalhydlab.ir/software/xgb-bbrp/download)
- [Download User & Technical Manual](https://coastalhydlab.ir/software/xgb-bbrp/manual)

## About

Programmed by Pouya Zarbipour. For questions or feedback, please contact [pouyazarbipour@gmail.com](mailto:pouyazarbipour@gmail.com).

## Disclaimer

This tool aims to improve berm breakwater recession prediction and enhance design reliability. Please refer to the User & Technical Manual for information on intended use and limitations.
