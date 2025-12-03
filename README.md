# Credit-Scoring-Project-

## Business Context
This project develops a credit-scoring model to identify companies at risk of bankruptcy using historical financial statement data. The goal is to support lending decisions, underwriting, and portfolio risk monitoring by providing an early indication of financial distress. By modeling structured financial ratios and indicators, the system helps distinguish stable firms from those with elevated default risk, improving decision-making and reducing exposure to failing companies.

## Techniques Used
- Worked with the `bankruptcy.RData` dataset containing financial attributes and a binary `Bankrupt?` target  
- Inspected, cleaned, and transformed numerical predictors  
- Applied dummy-encoding where needed using `fastDummies`  
- Ensured proper split between training and testing sets  
- Converted predictors to matrix format for LightGBM  

- Implemented a LightGBM gradient-boosted decision tree model  
  - Controlled learning rate  
  - Tuned tree depth and number of leaves  
  - Set a high number of boosting iterations  
  - Monitored training with evaluation frequency  

- Conducted structured hyperparameter search across `num_leaves` and `learning_rate` using functional mapping (`pmap`)  
- Generated predictions on unseen test data with clean separation from training
