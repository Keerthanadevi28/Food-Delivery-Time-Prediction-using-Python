# Food-Delivery-Time-Prediction-using-Python

To predict food delivery times accurately, it's crucial to factor in the distance between the food preparation site and the delivery destination. This involves understanding the historical patterns of delivery times for various distances traveled by delivery partners. To achieve this, we require a dataset containing comprehensive information on delivery times based on distance covered.

I've identified an optimal dataset that encompasses all the necessary features for this task. You can access and download this dataset from the provided link.
https://statso.io/wp-content/uploads/2023/01/Delivery-time.zip

To initiate the food delivery time prediction task, I began by importing essential Python libraries and loading the provided dataset. The dataset encompasses various attributes including details about delivery personnel, location coordinates, order type, vehicle type, and delivery duration.

Subsequently, I conducted exploratory data analysis to glean insights from the dataset. With a total of 45593 entries, the dataset exhibited no missing values. I then computed the distance between the restaurant and delivery destinations employing the haversine formula based on latitude and longitude coordinates.

Following the addition of the distance feature to the dataset, I delved into exploring relationships between different attributes and delivery time. These relationships were visualized through scatter plots and box plots. Noteworthy observations included a consistent correlation between delivery time and distance, an inverse linear association between delivery time and delivery partner ratings, and the impact of delivery partner age on delivery time.

For constructing the food delivery time prediction model, I employed an LSTM neural network. The data was partitioned into training and testing sets, and the model architecture was defined and trained using the training dataset. Post-training, I evaluated the model's performance and tested its predictive capabilities by inputting features such as delivery partner age, ratings, and distance to anticipate the food delivery time.

In summary, the outlined procedures for predicting food delivery time encompass:

Data preprocessing: Importing libraries, loading the dataset, handling missing values, and computing the distance between restaurant and delivery locations.
Exploratory data analysis: Investigating relationships between attributes and delivery time using visualizations.
Model training: Partitioning the data, defining an LSTM neural network model, compiling the model, and training it on the training dataset.
Model evaluation: Assessing the trained model's performance and utilizing it to predict food delivery time based on input features.

Model Evaluation
After training and testing the food delivery time prediction model, the following evaluation metrics were obtained:

Mean Absolute Error (MAE): The average absolute difference between predicted and actual delivery times is approximately 6.35 minutes. This indicates that, on average, the model's predictions deviate by about 6.35 minutes from the actual delivery times.

Mean Squared Error (MSE): The average squared difference between predicted and actual delivery times is approximately 62.82 minutes squared. This metric penalizes larger errors more heavily than MAE.

Root Mean Squared Error (RMSE): The square root of MSE is approximately 7.93 minutes. RMSE provides a measure of the spread of errors in the predictions, with lower values indicating better performance.
