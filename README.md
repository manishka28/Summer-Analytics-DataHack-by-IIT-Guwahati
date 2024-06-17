# Summer-Analytics-DataHack-by-IIT-Guwahati
This is submission of DataHack Hack-a-thon at Summer Analytics Workshop, IIT Guwahati


I will be using scikit-learn's logistic regression implementation.

## Scaling: Transform all features to be on the same scale. This matters when using regularization, which we will discuss in the next section. I will use StandardScaler, also known as Z-score scaling. This scales and shifts features so that they have zero mean and unit variance.
## NA Imputation: Logistic regression does not handle NA values. I will use median imputation, which fills missing values with the median from the training data, implemented with SimpleImputer.

I am also going to start using Scikit-Learn's built-in composition functionality to encapsulate everything into a pipeline.

I will first chain together the preprocessing steps (scaling and imputing) into one intermediate pipeline object numeric_preprocessing_steps. Then, we use that with Scikit-Learn's ColumnTransformer, which is a convenient way to grab columns out of a pandas data frame and then apply a specified transformer.


I'll use scikit-learn's default hyperparameters for LogisticRegression of L2 (a.k.a. Ridge) regularization with C value (inverse regularization strength) of 1. Regularization is useful because it reduces overfitting.

Because we have two labels we need to predict, I'll use Scikit-Learn's MultiOutputClassifier. This is a convenient shortcut for training two of the same type of model and having them run together.
