# Alphabet Soup: Deep Learning Challenge

## Overview

Alphabet Soup, a nonprofit organization, is looking for a tool to help select funding applicants with the best chances of success in their ventures. This project involves building a binary classifier using deep learning to predict whether applicants will be successful in their use of funding.

The dataset provided contains information on over 34,000 organizations that have received funding. Based on this data, the model will help Alphabet Soup make informed decisions on future applicants.
## Data Preprocessing

- The dataset contains information about organizations that received funding in the past.
- The **target variable** is `IS_SUCCESSFUL`, which indicates whether an applicant successfully used the funds.
- Features include:
  - `APPLICATION_TYPE`
  - `CLASSIFICATION`
  - `ASK_AMT`
  - `AFFILIATION`
  - `USE_CASE`
  - `ORGANIZATION`
  - `STATUS`
  - `INCOME_AMT`
  - `SPECIAL_CONSIDERATIONS`

- The columns `EIN` and `NAME` were removed because they are identifiers that don't contribute to the prediction model.

- **One-hot encoding** was applied to categorical variables to convert them into numerical format suitable for a neural network.

## Model Architecture

### Initial Model

The initial model consisted of two hidden layers:
- **Hidden Layer 1**: 80 neurons, ReLU activation
- **Hidden Layer 2**: 30 neurons, ReLU activation
- **Output Layer**: 1 neuron, Sigmoid activation for binary classification.

### Optimized Model

The optimized model introduced improvements to the initial model:
- **Hidden Layer 1**: 100 neurons, ReLU activation
- **Hidden Layer 2**: 50 neurons, ReLU activation
- **Hidden Layer 3**: 25 neurons, ReLU activation
- **Output Layer**: 1 neuron, Sigmoid activation.

## Results

- **Initial Model Accuracy**: 72.70%
- **Optimized Model Accuracy**: 72.94%

Despite optimizations, the model did not reach the target accuracy of 75%.

## Conclusion

While the deep learning model shows promise in predicting funding success with an accuracy of 72.94%, further enhancements are needed to meet the target accuracy of 75%. Incorporating alternative machine learning models, such as **Random Forest** or **XGBoost**, could potentially yield better results for structured/tabular data.

## Bonus

As part of the bonus section, several additional optimizations and evaluations were explored:
- **Increase in Neurons**: More neurons were added to hidden layers.
- **Added Hidden Layers**: Additional layers were introduced to increase complexity.
- **Model Performance Evaluation**: The optimized model showed a slight improvement in accuracy, though further optimizations may be needed to reach 75% accuracy.
