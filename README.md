Limitations:
The DecisionTreeClassifier may lead to overfitting, particularly when the tree is deep, and there is noise in the training data. The algorithm exhibits high variance, resulting in different splits and trees for small variations in the input data.

Improvements:
To address overfitting, limitations were imposed on the classifier, such as setting max_depth=10, min_samples_split=5, and min_samples_leaf=5. These constraints prevent overfitting and reduce execution time by 13% (from 8.1 seconds to 7 seconds).

As a second improvement, the variance of each dimension in the dataset was plotted. It was observed that most data from dimension 15 to the end (33) was negligible. Restricting the model training to dimensions 1 to 14 resulted in a 57% reduction in execution time and helped prevent overfitting.

Additionally, to test the model's robustness to noisy data, noise was added to 5000 data points, creating a synthetic noisy dataset. Despite the known challenges of handling noisy data, the model achieved an accuracy of 80%, demonstrating its resilience.
