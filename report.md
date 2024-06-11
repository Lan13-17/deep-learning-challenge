# Module 21 Report Template

## Overview of the analysis: Explain the purpose of this analysis.

This analysis serves to review the model's target's and features, as well as analyse its optimization and performance. We will go over what features the model uses for its target, what changes were made compared to the initial model, and which optimization had the best performance.


## Data Preprocessing:

The model is looking to correctly identify whether a company will effectively use their money should they be funded. In the model we take a look at application type, affiliation, government classification, income, organization type/status, requested amount of funding, what they'll use it for, and any special considerations.

The name and EIN columns were dropped, the application data was aggregated into the top 8 types and the rest were binned together, lastly the classification types were aggregated into the top 5 types and the rest were binned together.


## Compiling, Training, and Evaluating the Model:

The best model (second optimization) had the following changes made to it:
- Additionally dropped status and special considerations column
- Kept the top 8 application types and put the rest as others
- Put all classification types whose value_count < 10 as others
- Increase training size to 85%
- Added two additional hidden layers
- Changed number of neurons to 40, 20, 10, 1
- Changed layers to leaky relu, leaky relu, leaky relu, tanh, sigmoid
- Decreased epochs to 50

Reached 0.7312 accuracy with a loss of 0.5533.

Target model performance was 0.75, so we are short by 0.0188.


## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

Overall this model falls short of the target performance by 0.0188, still this model is slightly better in terms of accuracy and loss than the initial model. I believe a descision tree might do better as a model since we're dealing with a lot of categorical data and we need to be able to explain to the foundation why we think an organization will succeed should Alphabet Soup fund them.