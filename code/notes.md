# Intro
This file lists the main reflections about modelling tasks and statistics that I incurred in the project. These are organized into the following sections:
- Scaling
- Packages for classification analysis
- Post-hoc analysis

## Notes about scaling
You do not always need to transform or scale the data in advance when using logistic regression on a training dataset. However, there are some cases where it may be helpful to do so.

One reason to transform or scale the data is if the features have different scales. For example, if one feature is measured in meters and another feature is measured in kilograms, then the logistic regression model may not be able to learn the relationship between the features as effectively. Transforming the data to a common scale can help to address this issue.

Another reason to transform or scale the data is if the features are not normally distributed. Logistic regression assumes that the features are normally distributed, so transforming the data to a normal distribution can help to improve the performance of the model.

Finally, transforming or scaling the data can help to improve the interpretability of the logistic regression model. When the features are on different scales, it can be difficult to understand the impact of each feature on the predicted probability. Transforming the data to a common scale can make it easier to understand the relative importance of each feature.

Ultimately, the decision of whether or not to transform or scale the data is a case-by-case decision. There is no one-size-fits-all answer. However, if you are unsure, it is always best to err on the side of caution and transform or scale the data.

Here are some of the common transformations and scaling techniques used in logistic regression:

- Standardization: This is the most common transformation technique. It involves subtracting the mean from each feature and then dividing by the standard deviation.
- Normalization: This technique involves transforming the data so that all of the features have a mean of 0 and a standard deviation of 1.
- Min-max scaling: This technique involves transforming the data so that all of the features are between 0 and 1.
- The best transformation or scaling technique to use will depend on the specific dataset and the goals of the analysis.

**Scaling multiple features**: 
You can scale the dataset once and then include the features that you need in the model. This is because the scaling process does not depend on the specific model that you are using. However, it is important to note that if you scale the data once and then include different subsets of features in different models, the results of the models may not be comparable. This is because the different models will be trained on different scales of the data.

If you want to make sure that the results of the models are comparable, you can scale the data for each bundle of features. This will ensure that all of the models are trained on the same scale of the data.

Here are some of the things to consider when deciding whether to scale the data once or for each bundle of features:

The number of models: If you are only running a few models, then it may be easier to scale the data once. However, if you are running a large number of models, then it may be more efficient to scale the data for each bundle of features.
The size of the dataset: If the dataset is large, then it may be more computationally expensive to scale the data for each bundle of features.
The importance of comparability: If you need to make sure that the results of the models are comparable, then you should scale the data for each bundle of features.
Ultimately, the decision of whether to scale the data once or for each bundle of features is a trade-off between convenience and accuracy.

## Notes about packages for classification analysis
- Statsmodels: Wide selection of statistical models, including logit and probit and multivariate analysis. It has This is a good option for LDA and QDA analysis because it has a module for both of these methods. The documentation for the LDA and QDA modules is also very good.
- Scikit-learn: Easy to use and with wide documentation. It includes also random forest. This is also a good option for LDA and QDA analysis. It does not have a dedicated module for LDA and QDA, but it does have a module for discriminant analysis. The discriminant analysis module can be used to perform both LDA and QDA.
- PyTorch: This is a Python library for machine learning. This is not a good option for LDA and QDA analysis. It does not have a dedicated module for LDA and QDA, and the discriminant analysis module is not as well-developed as the modules for other machine learning methods.
- TensorFlow: This is a Python library for machine learning. It includes a module for logistic regression. This is not a good option for LDA and QDA analysis. It does not have a dedicated module for LDA and QDA, and the discriminant analysis module is not as well-developed as the modules for other machine learning methods.
- XGBoost: This is a Python library for machine learning. It is known for its speed and accuracy. It includes a module for logistic regression. This is not a good option for LDA and QDA analysis. It does not have a dedicated module for LDA and QDA, and the discriminant analysis module is not as well-developed as the modules for other machine learning methods.

## Notes about post-hoc analysis
- Statsmodels: Statsmodels has a module for post-hoc analyses of logistic regression models. This module includes functions for performing Wald tests, likelihood ratio tests, and other common post-hoc tests.
- Scikit-learn: Scikit-learn does not have a dedicated module for post-hoc analyses of logistic regression models. However, it does have a module for model evaluation, which includes functions for calculating the odds ratios and confidence intervals for the coefficients of the model.
- PyTest: PyTest is a unit testing framework that can be used to perform post-hoc analyses of logistic regression models. This can be done by writing custom unit tests that test the statistical significance of the coefficients of the model.
- R: R is a statistical programming language that has a number of packages for post-hoc analyses of logistic regression models. Some of the popular packages include car, lmtest, and multcomp.
