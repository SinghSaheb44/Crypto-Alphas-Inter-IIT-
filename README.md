
This innovative strategy leverages the advanced predictive capabilities of one of the most widely acclaimed boosted tree ensemble models, the XGBoost Classifier. By utilizing a diverse range of oscillator-based technical indicators that capture trend, momentum, and volatility characteristics, the model delivers precise predictions for optimal trade decisions. Oscillator-based indicators are specifically chosen due to their minimal autocorrelation with price and volume, effectively mitigating the risk of overfitting.
XGBoost is an ideal choice for this machine learning framework due to its numerous advantages:
Optimized Performance: XGBoost is designed for speed and efficiency, offering highly optimized implementations for tree construction and gradient boosting.
Regularization: Incorporates L1 (Lasso) and L2 (Ridge) regularization techniques, reducing overfitting and enhancing generalization.
Scalability: Efficiently handles large-scale datasets through distributed and parallel processing capabilities.
Missing Data Handling: Automatically manages missing values by learning the optimal pathways during training.
Feature Importance: Provides detailed insights into feature importance, facilitating effective feature selection and model interpretability.
Cross-validation: Includes built-in support for K-fold cross-validation, enabling robust model evaluation and hyperparameter tuning.
The trade signals predicted by the XGBoost model are further refined by integrating a Moving Average crossover signal for entry points, while the exit strategy employs an ATR (Average True Range)-based trailing stop-loss mechanism. This combination ensures a systematic and balanced approach to trade execution, aligning predictive accuracy with risk management.
Signal Generation :

Long Signal :
If the model’s predicted trade call is long and MA_Short > MA_Long  i.e the moving average crossover complements the trade signal thus eliminating the possibility of any arbitrarily noisy decision , a long entry signal is generated.
Length of MA_Short = 9 periods , Length of MA_Long = 26 periods.


Short Signal:
Similarly if the model’s predicted trade call is short and MA_Short < MA_Long , it generates a short entry signal.


Long Exit:
An ATR-based trailing stop-loss mechanism governs exit decisions for long trades::
Stop-loss = current_price - ATR_Multiplier * ATR_value, when the price moves favourably.
Remains unchanged if the price moves unfavourably i.e downwards.
When the trailing stop-loss is attained , it generates a long exit signal.
Length of ATR= 14 periods , ATR_Multiplier =14


Short Exit:
For short trades, the trailing stop-loss is defined as::
Stop-loss = current_price + ATR_Multiplier * ATR_value, when the price moves favourably.
Remains unchanged if the price moves unfavourably i.e upwards.
When the trailing stop-loss is attained , it generates a short exit signal.

Avoiding Overfitting and Look-Ahead Bias:
Given the machine learning-based nature of this strategy, addressing overfitting and look-ahead bias is paramount. The following measures are implemented to ensure robustness:
K-fold cross-validation: The model employs K-fold cross-validation to curb overfitting by ensuring the model was trained and validated on diverse subsets of data, enhancing its generalization capability.


Evaluating train-test errors: Errors on the train and test sets are evaluated to detect signs of overfitting. The win ratios indicate minimal or no overfitting:
Win ratio on train set : 0.54 
Win ratio on test set : 0.53


Hyperparameter optimization: RandomizedSearchCV, combined with validation set evaluation, was used for hyperparameter optimization. This approach efficiently explores a wide range of parameter configurations and identifies the optimal setup, reducing overfitting


Moving Average Crossover Confirmation: The strategy avoids relying solely on the XGBoost model for trade signal generation, as this could result in arbitrarily noisy and potentially loss-inducing signals. Instead, the trade signal is validated through a moving average crossover, ensuring greater accuracy and reliability.

