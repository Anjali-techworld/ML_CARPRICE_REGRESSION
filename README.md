# ML_CARPRICE_REGRESSION

A Chinese automobile company aspires to enter the US market by setting up their manufacturing unit there and producing cars locally to give competition to their US and European counterparts. They have contracted an automobile consulting company to understand the factors on which the pricing of cars depends. Specifically, they want to understand the factors affecting the pricing of cars in the American market, since those may be very different from the Chinese market. Essentially, the company wants to know:
These steps are followed here:
Loading and Preprocessing Data:
Data Cleaning: Removing or imputing missing values is essential for ensuring model reliability. Dropping rows can lead to information loss, so imputing with mean/median (for numerical) or mode (for categorical) may be better for large datasets. Categorical Encoding: Encoding is necessary to convert non-numeric data into a format that can be understood by machine learning models. Label encoding is simple but may introduce ordinal relationships; One-Hot encoding could be more suitable if no ordinal relation exists.

Feature Scaling: Helps models like Support Vector Regressor (SVR) and Gradient Boosting by ensuring numerical features have similar ranges. Standardization (mean=0, std=1) is a preferred method. Train-Test Split: Ensures the model generalizes well by testing it on unseen data. Using random_state ensures reproducibility.

Model Implementation :
Using diverse models captures a range of assumptions about the data: Linear Regression assumes a linear relationship between predictors and the target. Decision Tree Regressor captures non-linear relationships but can overfit. Random Forest Regressor mitigates overfitting by averaging predictions from multiple trees. Gradient Boosting Regressor builds sequentially to correct errors, often outperforming Random Forest. Support Vector Regressor works well with smaller datasets and captures complex relationships through kernels.

Model Evaluation :
R² (Coefficient of Determination): Measures the proportion of variance explained by the model. Closer to 1 indicates better performance. MSE (Mean Squared Error): Penalizes large errors heavily, making it sensitive to outliers. MAE (Mean Absolute Error): Offers a more intuitive measure of average prediction error, less sensitive to outliers compared to MSE. The comparison table allows identifying the best-performing model for the given data.

Feature Importance Analysis Insights
Significant Features: Tree-based models (like Random Forest) rank features by their importance in reducing error. A feature with high importance is strongly correlated with the target variable. This analysis helps prioritize design and marketing decisions for the automobile company. Interpretation: Features like engine size, horsepower, or luxury-level indicators may emerge as significant. If categorical features like "brand" or "type" dominate, it shows brand perception significantly influences price.

Hyperparameter Tuning Insights
Purpose: Optimizing hyperparameters can improve the model's predictive power. For example: Increasing n_estimators in Random Forest improves model stability. Adjusting C or kernel in SVR helps handle non-linear relationships better. Results: Typically, tuned models outperform default configurations. However, improvements may be marginal if the baseline model is already well-suited.

General Insights
Best Model Selection: The model with the highest R² and lowest MSE/MAE on the test set should be chosen. It balances predictive power and robustness. Actionable Insights for the Company: Identify features that drive prices, such as "brand," "engine power," or "fuel efficiency." Adjust design and production strategies to align with key drivers of price in the American market. Utilize the best-performing model to predict prices of new models before launch.

Based on the analysis of the Chinese automobile company dataset, Rando, Forset emerged as the best-performing model for predicting the target variable, price. Its superior performance, compared to other models, highlights its ability to capture the intricate relationships between features and the target variable within the dataset. This finding underscores the effectiveness of Gradient Boosting in handling complex data structures and delivering accurate predictions. 
