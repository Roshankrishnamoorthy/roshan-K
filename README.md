**PROJECT 1**

**GROUP members**

1)Roshan Krishnamoorthy(A20592056)
2)Nisha Mayilraj(A20592055)
3)Nithishkannan Kuppal Thulasiraman(A20593857)


**Questions**

**1.What does the model you have implemented do and when should it be used?**
The model is a Linear Regression with ElasticNet Regularization. It combines L1 (Lasso) and L2 (Ridge) penalties to prevent overfitting and manage multicollinearity. It is best used when you have a dataset with many features, some of which may be highly correlated, or when you want to perform feature selection alongside regression.

**2.How did you test your model to determine if it is working reasonably correctly?**
The model was tested using cross-validation on a training dataset to evaluate its performance. Metrics such as Mean Squared Error (MSE) and R-squared were used to assess accuracy and fit. Additionally, the model was validated on a separate test set to ensure generalizability.

**3.What parameters have you exposed to users of your implementation in order to tune performance?**
Users can adjust the following parameters:
alpha: Controls the strength of the regularization.
l1_ratio: Determines the mix between L1 and L2 regularization.
max_iter: Sets the maximum number of iterations for convergence.
tol: Specifies the tolerance for stopping criteria.

**4.Are there specific inputs that your implementation has trouble with? Given more time, could you work around these or is it fundamental to the model?**
The implementation may struggle with datasets that have non-linear relationships or missing values. These issues are not fundamental to the model but require preprocessing steps like polynomial feature transformation or imputation to address effectively.


Machine learning techniques like L1 regularization, sometimes referred to as Lasso regularization, are used to stop overfitting. It functions by adjusting the loss function of the model by a penalty term that is determined by the absolute values of the model's coefficients.

**EXAMPLES:**

1.	Credit scoring: In developing a credit risk model, L1 can help identify the most crucial factors (like income, credit history, debt ratio) while eliminating less relevant ones (e.g. zip code, marital status).
2.	Medical diagnosis: When analyzing patient data to predict diseases, L1 can pinpoint the most indicative symptoms or test results, simplifying the diagnostic process.
3.	Text classification: In sentiment analysis of product reviews, L1 can select the most impactful words or phrases, ignoring less meaningful ones.

**ADVANTAGES**
1.	Can eliminate less important features by setting their coefficients to zero
2.	Sparse models: Produces simpler models with fewer active features
3.	Interpretability: Easier to identify which features have the most impact

**DISADVANTAGES:**
1.	Instability: Can be unstable when features are highly correlated
2.	Optimization challenges: Non-differentiable at zero, making optimization more difficult
3.	Limited in handling feature interactions: May struggle with complex relationships between features

**L2 REGULARIZATION**
L2 regularization, which is sometimes referred to as Ridge regularization, is a machine learning technique that stops overfitting. It functions by incorporating a penalty term into the loss function of the model, which is determined by the squared values of the model's coefficients.

**EXAMPLES**
1.	Image recognition: In a neural network for classifying animal images, L2 can help prevent any single feature (like color or texture) from dominating the model's decisions.
2.	Weather forecasting: When predicting temperature, L2 can balance the influence of various factors (humidity, wind speed, atmospheric pressure) without eliminating any.
3.	Recommendation systems: In movie recommendation algorithms, L2 can manage the impact of multiple user preferences (genre, actors, release year) without discarding any particular aspect.

**ADVANTAGES**
1.	Stability: More stable, especially when dealing with correlated features
2.	Smooth optimization: Differentiable everywhere, making it easier to optimize
3.	Handling multicollinearity: Effective at managing highly correlated features
4.	Computational efficiency: Generally faster to compute due to its mathematical properties

**DISADVANTAGES:**
1.	No feature selection: Keeps all features in the model, just reducing their impact
2.	Less interpretable: Harder to determine feature importance as all coefficients remain non-zero
3.	
**ELASTIC NET REGRESSION**

Elastic Net Regression is an advanced method in the field of linear regression that merges the strengths of two popular regularization techniques: Lasso and Ridge regression. This approach is particularly valuable when dealing with datasets where standard linear regression methods may face challenges, especially in situations involving high correlation among predictor variables. By combining the penalty terms from both Lasso and Ridge regression, Elastic Net creates a balanced approach to model regularization. This unique characteristic makes it an effective tool for addressing multicollinearity, a common issue in many real-world datasets where independent variables are closely related.

![image](https://github.com/user-attachments/assets/c525f182-a273-42c6-a1e5-5897d4c879e8)


**Elastic Net Implementation**
1.The elastic_net_gradient_descent function implements the Elastic Net algorithm using gradient descent. It takes the following parameters:
2.X: Feature matrix
3.y: Target vector
4.alpha: Regularization strength
5.l1_ratio: Ratio of L1 regularization (1 - l1_ratio is the ratio of L2 regularization)
6.num_iterations: Number of gradient descent iterations
7.learning_rate: Step size for gradient descent



