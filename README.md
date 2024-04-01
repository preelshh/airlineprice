# airlineprice
**Short Description**
This project utilizes Indian airline price data to predict fares using a Random Forest Tree classifier. Data was preprocessed for readability and dimensionality reduction. Feature encoding and outlier handling were performed. Model optimization was achieved via hyperparameter tuning for enhanced accuracy.



**Process**

The data science project commenced by importing essential libraries such as Pandas, Seaborn, and Matplotlib. The first step involved identifying the business problem, which aimed to predict airline fare prices based on various independent factors including destination, source, date of journey, time of journey, arrival time, number of stops, trip length, and airline carrier.

Addressing missing values was the subsequent task, with only one row containing a missing value, leading to the decision to remove the entire row for data integrity. Following this, transformations were applied to date, arrival time, and time columns to make them more readable for machine learning models, converting them from strings to integer values.

An initial exploratory data analysis was conducted to uncover correlations within the data. Scatterplots were utilized to visually inspect correlations between factors such as trip duration and price, as well as the number of stops and duration versus price. Regression lines were incorporated into the visualizations to accentuate these correlations.

Feature encoding was then implemented, beginning with one-hot encoding for the source column due to its manageable number of unique locations. Target-guided encoding was chosen for the airline column to handle the larger variety of airlines and mitigate the curse of dimensionality. Label encoding was applied to other relevant columns.

Outliers in the data were addressed next by visualizing their distribution and employing the Interquartile Range (IQR) method to identify and replace outlier values with the median price.

Feature selection was conducted to determine the most influential variables on the price using mutual information regression from the sklearn.feature_selection package. The top three features identified were destination, airline, and total stops.

The ML model was implemented using the RandomForestRegressor from the scikit-learn library. An automated machine learning pipeline was developed to streamline model iteration and display essential results such as training scores, predictions, R2 score, MSE, MAE, RMSE, MAPE, and error distribution.

Finally, hyperparameter tuning was performed to optimize the model's accuracy. This involved experimenting with multiple algorithms, hyperparameter optimization, cross-validation, and various evaluation metrics based on domain expertise to select the best-performing model configuration.





