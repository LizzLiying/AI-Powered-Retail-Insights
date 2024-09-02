# Beyond Traditional Methods: AI-Powered Retail Insights

## Capstone project on creating an advanced AI-driven data analystics system using Python

### Problem Statement
Traditional data analysis methods such as spreadsheets and basic statistical analysis are often inadequate for modern retail data due to:
- Data volume and complexity
- Data quality issues
- Limited insights
- Limited on predictive analytics tools
- Scalability.

Advanced techniques like data mining, machine learning, and AI are better suited to handle thses challenges and extract valuable insights.

### Dataset used for the capstone project
[Link to dataset](https://www.kaggle.com/datasets/ihelon/coffee-sales/data)

Description of dataset:
This dataset contains detailed records of coffee sales from a vending machine. The dataset spans from March 2024 to present time, capturing daily transaction data. It is intended for analysis of purchasing patterns, sales trends, and customer preferences related to coffee products.

### Using machine learning models to extract valuable insights

<details>
<summary><b>Using kMEANs to identify customer segmentation</b></summary>

<img width="456" alt="image" src="https://github.com/user-attachments/assets/fef1d277-e73b-48df-8d26-7456fbf5c988">

Screenshot of elbow plot

Based on the elbow plot, decided on k value equal to 3 because it is where the SSE begins to flatten out and see an inflection point. 

<img width="488" alt="image" src="https://github.com/user-attachments/assets/0d053ae4-1231-4611-865d-b95bb992b9b2">

Screenshot of kMeans scatterplot


**Scatterplot Observation**

The scatter plot illustrates the relationship between average spending and purchase frequency for a group of customer. Each dot represents a customer, with its position on the graph determined by their average spending and purchase frequency. 

**Left cluster:**
This cluster likely to represents customers who make infrequent but high-value purchases. They might be looking for premium coffee and are willing to pay a premium price. However, there is also some distinct customers on the bottom of this cluster buying low-value purchase in the group.

**Middle cluster:**
This cluster likely to represents customer who are regular buyers and are willing to spend a moderate amount on the coffee. They might be looking for value and convenience.

**Right cluster:**
This cluster likely to represents a mix of customers who are either high-value buyers or regular buyers seeking value. They are both highly engaged and frequent customers. 

**Overall conclusion:**
The clusters might also represent different stages of customer lifecycle. For example, the left cluster could represent new customers or customers who happened to passby the vending machine, while middle and right clusters could represent loyal and repeat customer. 

**Why choose kMeans Model?**

It is a popular choice for customer segmentation due to it simplicity, efficiency and scalability. It automatically group customer based on their similarity in terms of the calculated metrics. 

</details>

<details>
<summary><b>Using RNNs (LSTM) Model to forecast daily sales volume</b></summary>

<img width="442" alt="image" src="https://github.com/user-attachments/assets/954028d4-187c-4482-9860-83fbefd3aba7">

Screenshot of LSTM Model

Model's RMSE score: 112.41933002358847


**LSTM Chart Observation**

The chart shows the actual vs. predicted values of the sales amount for each day. 

**Overall performance:**
The model shows a moderate level of accuracy in predicting the value. There is a clear trend that the model follows but there are also noticeable deviations between the actual and predicted values. The RMSE value of 112.42 indicates that the model's predictions are, on average, off by about $112.42 from the actual value. 

**Specific observation:**
The model tends to underpredict the peaks and overpredict the troughs. There are a few instances where the model's prediction deviate significantly from the actual values. The model seems to struggle with capturing the sharp fluctuations in the data. 

**Conclusion:**
The model demonsrates moderate accuracy in predicting values. However, there are areas where the model could be improved, such as capturing sharp fluctations and reducing the overall prediction error. 

**Why choose LSTM model?**

LSTM is specialized RNN well-suited for time series forecasting due to its ability to handle long-term dependencies. It uses "gates" to control information flow and avoids the vanishing gradient problem, making it ideal for capturing trends, seasonality and complex pattern. 

</details>

<details>
<summary><b>Using Random Forest Classifier Model to forecast product demand</b></summary>

<img width="415" alt="image" src="https://github.com/user-attachments/assets/9e49730c-4ca6-4b2b-a652-4595a7fbd896">

Screenshot of RFC Model Prediction

![image](https://github.com/user-attachments/assets/dbfef955-fe05-4ee4-a92a-dc1ede840dcd)

Screenshot of RFC Model Classification Report


**Obervation on the Random Forecast Classification Model**

**Overall performance:**
The model achieves and overall accuracy of 73%, indicating that it correctly predicts the coffee order in approximately 73% of the cases. The macro average of precision, recall, and F1-score is 0.60, 0.61, and 0.60 respectively, suggesting that the model's performance is relatively balanced across different classes. 

**Class-wise performance:**
Class 0 has the highest precision and recall, indicating that the model is accurate in predicting this class. Class 3 has a precision and recall of 0, suggesting that the model is unable to correctly predict any instances of this class. Other classes exhibit varying levels of precision and recall, with some performing better than others. 

**Conclusion:**
The RFC model demonstrates moderate accuracy in predicting coffee orders. While the model performs well for some classes, it struggles with other, particularly class 3.

**Why choose RFC model?**

RFC has the ability to handle non-linear relationships, providing feature importance, and reduce overfitting. It's suitable for complex data, handles missing values well, and can be applied to large datasets.

</details>

### Conclusion
Machine Learning is transforming retail by extracting insights from data and helping retailers enhance customer satisfaction, increase sales, reduce costs, and gain a competitive edge.

[Link to your LinkedIn](https://www.linkedin.com/in/lizz-tan-li-ying-59639910b/)
