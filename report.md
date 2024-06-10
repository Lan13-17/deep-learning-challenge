# Module 21 Report Template

## Overview of the analysis: Explain the purpose of this analysis.

This analysis serves to review the model's target's and features, as well as analyse its optimization and performance.


## Data Preprocessing:

The model is looking to correctly identify whether a company will effectively use their money should they be funded. In the model we take a look at application type, affiliation, government classification, income, organization type/status, requested amount of funding, what they'll use it for, and any special considerations.


## Compiling, Training, and Evaluating the Model:

- Kept the top 8 application types and put the rest as others
- Put all classification types whose value_count = 1 as others
- Added an additional hidden layer
- Changed number of neurons to 40, 20, 10, 1
- Changed layers to leaky relu, leaky relu, leaky relu, sigmoid
- Increased epochs to 150

Reached 0.7293 accuracy with a loss of 0.5547.

Target model performance was 0.75, so we are short by 0.0207.


## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

Overall this model falls short of the target performance by 0.0207, still this model is slightly better in terms of accuracy and loss than the initial model.