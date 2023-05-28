# fraud-detection-showcase

Showcasing fraud detection (extremely unbalanced data) technique from a hackathon.
The dataset has over 200 dimensions of various data type.
A few of the fields are also nominal which are annoying, and I used one-hot encoding for those.


## Approach

I applied classical statistics approach while my colleague applied XGBoost approach.

- I used an ensemble, partition the data set so the fraud/non-fraud are roughly 1:1 ratio (by sampling the fraud set and non-fraud set).
- Preprocessing: I first normalized the numerical dimensions with standard scaler, and append the one-hot vectors of nominal fields.
- Feature Extraction: I used PCA (also tried LDA later which gets better confusion matrix scores but I can't find the code now).
- Training: I tried logistic regression, svm, gradient boost with many hyperparameter setups.
- Validation: reserved a small test data set. Then check the confusion matrix.

## Results

**Baseline**: predicting non-fraud for all cases gives 99.6% accuracy.

I achieved an overall accuracy of 98% accuracy, with a satisfactory confusion matrix score but a lot of false positives (which I guess is better than false negatives :p).

My colleague got a better overall accuracy but a worse confusion matrix score.





