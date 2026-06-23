# Part 9 - Model Fit, Evaluation, Inferencing, and ML Project Lifecycle

[← 08](08-ai-and-machine-learning-overview.md) | [↑ Index](../README.md) | [10 →](10-aws-managed-ai-services.md)

### Model fit
When model performance is poor, one of the first things to check is model fit.

Three common cases:
- `Overfitting`: performs well on training data but poorly on evaluation or unseen data
- `Underfitting`: performs poorly even on training data
- `Balanced fit`: neither overfitting nor underfitting

### Bias
Bias is the error caused by an overly simplistic or inappropriate modeling choice.

High bias usually means:
- the model does not match the training data well
- the model is too simple
- the model is underfitting

Ways to reduce bias:
- use a more complex model
- increase the number of useful features

### Variance
Variance measures how much model performance changes when trained on a different but similar dataset.

High variance usually means:
- the model is too sensitive to the training data
- the model performs well on training data but poorly on unseen data
- the model is overfitting

Ways to reduce variance:
- keep fewer but more relevant features
- repeat train/test splits and validate more carefully

### Bias-variance relationship
Useful intuition:
- high bias -> underfitting
- high variance -> overfitting
- low bias and low variance -> better balance

### Binary classification evaluation
For classification problems, one of the key tools is the `confusion matrix`.

It tracks:
- `True Positive (TP)`
- `False Positive (FP)`
- `True Negative (TN)`
- `False Negative (FN)`

### Main classification metrics
`Precision`
- `TP / (TP + FP)`
- important when false positives are costly

`Recall`
- `TP / (TP + FN)`
- important when false negatives are costly

`Accuracy`
- `(TP + TN) / (TP + TN + FP + FN)`
- more useful when classes are balanced

`F1 score`
- harmonic mean of precision and recall
- useful when you want a balance between the two, especially with imbalanced datasets

### Multiclass confusion matrices
Confusion matrices can also be used for multi-class classification, not only binary classification.

### AUC-ROC
`AUC-ROC` means `Area Under the Receiver Operating Characteristic curve`.

Main ideas:
- value ranges from `0` to `1`
- a higher value is better
- compares true positive rate against false positive rate across multiple thresholds

Why it matters:
- helps choose the threshold that best fits the business tradeoff

### Regression metrics
For regression tasks, key metrics include:
- `MAE` = Mean Absolute Error
- `MAPE` = Mean Absolute Percentage Error
- `RMSE` = Root Mean Squared Error
- `R²` = R-squared

How to interpret them:
- `MAE`, `MAPE`, and `RMSE` measure prediction error
- `R²` measures how much variance in the target is explained by the model

Quick intuition:
- lower `MAE`, `MAPE`, and `RMSE` are better
- `R²` closer to `1` is better

### Inferencing
Inferencing is when a trained model makes predictions on new data.

### Real-time vs batch inferencing
`Real-time inferencing`
- used when decisions must be made quickly
- latency matters more than perfect accuracy
- example: chatbots

`Batch inferencing`
- used on large datasets processed all at once
- often used for analysis workloads
- speed is less important than accuracy or throughput

### Inferencing at the edge
Edge inferencing runs close to where data is generated.

Typical edge-device characteristics:
- limited compute power
- very low latency
- local or offline capability

Common pattern:
- smaller models on edge devices
- larger models on remote servers

Tradeoff:
- local models are faster and more private
- remote models are usually more powerful

### Phases of an ML project
An ML project typically moves through these phases:
- business problem definition
- ML problem framing
- data collection and preparation
- feature engineering
- model training and parameter tuning
- model evaluation
- testing and deployment
- monitoring and debugging
- iteration and retraining

### Business problem and ML framing
Before building a model:
- define business goals
- define budget and success criteria
- define KPIs
- confirm that ML is actually appropriate

This step usually involves collaboration across:
- stakeholders
- data scientists
- data engineers
- ML architects
- subject-matter experts

### Data processing
Data processing includes:
- data collection
- data integration
- data preprocessing
- data visualization
- converting data into a usable format

### Exploratory Data Analysis
`EDA` helps understand the dataset before training.

Common activities:
- graphing and visualization
- checking correlations between variables
- identifying which features may matter most

### Iterative model development
Model development is iterative.

It often includes:
- additional feature engineering
- retraining
- hyperparameter tuning
- re-evaluation
- monitoring after deployment

### Deployment and monitoring
Once results are good enough, the model is deployed for inference.

Possible deployment styles mentioned:
- real-time
- serverless
- asynchronous
- batch
- on-premises

After deployment, monitoring is needed to:
- detect performance drops early
- debug issues
- understand model behavior in production

### Hyperparameters
Hyperparameters are settings defined before training begins.

Examples:
- learning rate
- batch size
- number of epochs
- regularization

Hyperparameter tuning means searching for the values that improve performance and generalization.

Common search methods:
- grid search
- random search

Managed help:
- `SageMaker Automatic Model Tuning (AMT)`

### Important hyperparameters
`Learning rate`
- controls the size of weight updates
- too high can overshoot the optimum
- too low can make training slow

`Batch size`
- number of training examples used in one update step
- smaller batches can be more stable but slower
- larger batches are faster but can be less stable

`Number of epochs`
- how many full passes the model makes over the training dataset
- too few can cause underfitting
- too many can cause overfitting

`Regularization`
- helps control model complexity
- increasing regularization can reduce overfitting

### How to reduce overfitting
Common approaches:
- increase training data size
- use early stopping
- apply data augmentation
- tune hyperparameters
- use ensembling

Main causes of overfitting:
- training data is too small or not representative
- training runs too long on the same data
- model complexity is too high and starts learning noise

### When ML is not appropriate
Machine learning is not always the right solution.

If a problem is deterministic and can be computed exactly, it is often better to write explicit code.

Example:
- if a deck has 5 red cards, 3 blue cards, and 2 yellow cards, the probability of drawing a blue card is exactly `3/10`

Key principle:
- use ML for pattern learning and uncertainty
- use regular programming when the correct answer can be computed directly and reliably

[← 08](08-ai-and-machine-learning-overview.md) | [↑ Index](../README.md) | [10 →](10-aws-managed-ai-services.md)
