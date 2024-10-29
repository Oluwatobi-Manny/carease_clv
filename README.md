*A comprehensive analysis of the total net profit CarEase customer is expected to bring over their entire lifetime*

# Use Case: Enhancing Customer Lifetime Value (CLTV) at CarEase
---

**Problem Statement:**

CarEase, an autoinsurance company, aims to optimize its customer retention and acquisition strategies to maximize long-term profitability. By accurately predicting and increasing customer lifetime value (CLTV), CarEase can make informed decisions about customer segmentation, targeted marketing campaigns, and pricing strategies.

**Goal:**

* Develop a Python-based predictive model to estimate the CLTV of existing and potential customers.
* Identify high-value customer segments and tailor personalized offerings to retain and upsell.
* Optimize marketing and sales efforts to acquire and nurture customers with high CLTV potential.
* Make data-driven decisions to improve overall business performance.

</head>
<body>
    <h2>CarEase Customer Dataset</h2>
    <table>
        <tr>
            <th>Column Name</th>
            <th>Description</th>
        </tr>
        <tr>
            <td>Customer</td>
            <td>Unique identifier for each customer</td>
        </tr>
        <tr>
            <td>State</td>
            <td>The state where the customer resides</td>
        </tr>
        <tr>
            <td>Customer Lifetime Value</td>
            <td>Estimated total revenue a customer will generate over their lifetime</td>
        </tr>
        <tr>
            <td>Response</td>
            <td>Indicates whether the customer responded to a marketing campaign</td>
        </tr>
        <tr>
            <td>Coverage</td>
            <td>The level of coverage the customer has</td>
        </tr>
        <tr>
            <td>Education</td>
            <td>The customer's educational level</td>
        </tr>
        <tr>
            <td>Effective To Date</td>
            <td>The date the customer's policy is effective</td>
        </tr>
        <tr>
            <td>EmploymentStatus</td>
            <td>The customer's employment status</td>
        </tr>
        <tr>
            <td>Gender</td>
            <td>The customer's gender</td>
        </tr>
        <tr>
            <td>Income</td>
            <td>The customer's annual income</td>
        </tr>
        <tr>
            <td>Location Code</td>
            <td>A code representing the customer's location</td>
        </tr>
        <tr>
            <td>Marital Status</td>
            <td>The customer's marital status</td>
        </tr>
        <tr>
            <td>Monthly Premium Auto</td>
            <td>The monthly premium for the customer's auto insurance policy</td>
        </tr>
        <tr>
            <td>Months Since Last Claim</td>
            <td>The number of months since the customer's last claim</td>
        </tr>
        <tr>
            <td>Months Since Policy Inception</td>
            <td>The number of months since the customer's policy began</td>
        </tr>
        <tr>
            <td>Number of Open Complaints</td>
            <td>The number of open complaints the customer has</td>
        </tr>
        <tr>
            <td>Number of Policies</td>
            <td>The number of policies the customer has with the company</td>
        </tr>
        <tr>
            <td>Policy Type</td>
            <td>The type of policy the customer has</td>
        </tr>
        <tr>
            <td>Policy</td>
            <td>The specific policy details</td>
        </tr>
        <tr>
            <td>Renew Offer Type</td>
            <td>The type of renewal offer sent to the customer</td>
        </tr>
        <tr>
            <td>Sales Channel</td>
            <td>The channel through which the customer acquired the policy</td>
        </tr>
        <tr>
            <td>Total Claim Amount</td>
            <td>The total amount of claims the customer has filed</td>
        </tr>
        <tr>
            <td>Vehicle Class</td>
            <td>The class of the customer's vehicle</td>
        </tr>
        <tr>
            <td>Vehicle Size</td>
            <td>The size of the customer's vehicle</td>
        </tr>
    </table>


**Python Libraries:**
---

* **Data Cleaning and Manipulation:**
  * Pandas, NumPy
* **Data Visualization:**
  * Matplotlib, Seaborn
* **Machine Learning:**
  * Scikit-learn, Scipy
* **Statistical Analysis:**
  * Statsmodels, Scikit-learn

**Model Development:**

1. **EDA:**
   * Describe the data graphically.
   * Make displot, distributions of the dataset.

![Displot](<Images/Screenshot (218).png>)

![Bar Chart](<Images/Screenshot (228).png>)

2. **Data Preprocessing:**
   * Handle missing values, outliers, and inconsistencies.
   * Encode categorical variables.
   * Scale numerical features.

```
# One-Hot Encoding for categorical features
cat_dum = pd.get_dummies(cat_col, drop_first=True).astype(int)
cat_dum.head()
```
![One-Hot Encoding](<Images/Screenshot (222).png>)

3. **Feature Engineering:**
   * Consider feature interactions and non-linear relationships.
   
![Linear feature](<Images/Screenshot (220).png>)

![Non linear feature](<Images/Screenshot (224).png>)

4. **Model Selection:**
   * Explore various regression models (e.g., linear regression, polynomial regression, decision trees, random forest, gradient boosting).
   
![Model selection](<Images/Screenshot (226).png>)

5. **Model Training and Evaluation:**
   * Split the data into training and testing sets.
   * Train the selected model on the training data.
   * Evaluate the model's performance using metrics like mean squared error (MSE), root mean squared error (RMSE), and R-squared.

```
# Get the best parameters
best_params = grid.best_params_
print("Best Parameters:", best_params)
```

![Best params](<Images/Screenshot (230).png>)

**Business Applications:**
---
* **Customer Segmentation:** Identify high-value, medium-value, and low-value customer segments.
* **Targeted Marketing:** Develop personalized marketing campaigns based on customer preferences and CLTV.
* **Pricing Optimization:** Implement dynamic pricing strategies to maximize revenue and customer retention.
* **Customer Retention:** Proactively identify customers at risk of churn and offer incentives to retain them.
* **Customer Acquisition:** Focus on acquiring customers with high CLTV potential.

**VERSION**
---

numpy: 1.26.4

pandas: 2.2.2

matplotlib: 3.9.1.post1

seaborn: 0.13.2

sklearn: 1.4.2

scipy: 1.13.1