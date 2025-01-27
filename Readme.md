# Data Science Assignment: E-Commerce Transactions Dataset

## Overview
This project involves analyzing e-commerce transaction data, building a customer lookalike model, and performing customer segmentation. The goal is to extract actionable insights, recommend similar customers, and cluster customers based on their profiles and transaction histories. The assignment demonstrates proficiency in data cleaning, exploratory data analysis (EDA), clustering, and predictive modeling.

---

## Dataset Description

The dataset consists of three files:

1. **Customers.csv**:
   - `CustomerID`: Unique identifier for each customer.
   - `CustomerName`: Name of the customer.
   - `Region`: Continent where the customer resides.
   - `SignupDate`: Date when the customer signed up.

2. **Products.csv**:
   - `ProductID`: Unique identifier for each product.
   - `ProductName`: Name of the product.
   - `Category`: Product category.
   - `Price`: Product price in USD.

3. **Transactions.csv**:
   - `TransactionID`: Unique identifier for each transaction.
   - `CustomerID`: ID of the customer who made the transaction.
   - `ProductID`: ID of the product sold.
   - `TransactionDate`: Date of the transaction.
   - `Quantity`: Quantity of the product purchased.
   - `TotalValue`: Total value of the transaction.

---

## Tasks

### **Task 1: Exploratory Data Analysis (EDA) and Business Insights**

#### Objectives:
1. Perform EDA on the dataset to understand trends and patterns.
2. Derive 5 business insights from the analysis.

#### Deliverables:
1. **Code**: `Rounak_Kumar_EDA.ipynb`
2. **Report**: `Rounak_Kumar_EDA.pdf` with key insights.

#### Steps:
- Load the data and clean missing or duplicate values.
- Analyze total sales, product popularity, and customer distribution.
- Visualize key trends (e.g., sales over time, regional performance).

#### Example Insights:
1. **Peak Sales Period**: Sales are highest during December, suggesting a strong holiday season effect.
2. **Top-Performing Region**: Customers from Asia contribute the most to sales.
3. **Popular Categories**: Electronics is the most purchased category, accounting for 40% of total sales.

---

### **Task 2: Lookalike Model**

#### Objectives:
- Build a model that recommends 3 similar customers for a given customer based on their profile and transaction history.
- Assign similarity scores to the recommendations.

#### Deliverables:
1. **Code**: `Rounak_Kumar_Lookalike.ipynb`
2. **Output**: `Rounak_Kumar_Lookalike.csv` with top-3 recommendations for Customer IDs `C0001` to `C0020`.

#### Steps:
1. **Prepare Data**:
   - Merge `Customers.csv`, `Products.csv`, and `Transactions.csv`.
   - Calculate total spending, category preferences, and region data for each customer.
2. **Calculate Similarity**:
   - Normalize the data using Min-Max scaling.
   - Use cosine similarity to compare customers.
3. **Interactive Input**:
   - Allow user to input a `CustomerID` and output the top 3 similar customers.

#### Example Output:
For `CustomerID: C0001`, the output might be:
```
Top 3 similar customers:
1. CustomerID: C0005, Similarity Score: 0.95
2. CustomerID: C0010, Similarity Score: 0.92
3. CustomerID: C0008, Similarity Score: 0.89
```

---

### **Task 3: Customer Segmentation (Clustering)**

#### Objectives:
- Perform customer segmentation using clustering techniques.
- Identify patterns in customer behavior based on transaction data and profiles.

#### Deliverables:
1. **Code**: `Rounak_Kumar_Clustering.ipynb`
2. **Report**: `Rounak_Kumar_Clustering.pdf` with visualizations and metrics.

#### Steps:
1. **Normalize Data**:
   - Scale the customer profiles using Min-Max scaling.
2. **Apply Clustering**:
   - Use K-Means clustering with `k` (number of clusters) ranging from 2 to 10.
   - Evaluate the clusters using the Davies-Bouldin Index.
3. **Visualize Clusters**:
   - Use PCA to reduce data to 2 dimensions for plotting.
   - Display distinct clusters in a scatterplot.

#### Example Output:
- Number of clusters: 4
- Davies-Bouldin Index: 1.69
- Key Characteristics:
  - Cluster 0: High spenders primarily buying electronics.
  - Cluster 1: Budget-conscious buyers focused on apparel.

---

## Tools and Libraries
1. **Programming Language**: Python
2. **Libraries**:
   - `pandas` for data manipulation.
   - `matplotlib` and `seaborn` for visualization.
   - `scikit-learn` for machine learning models and clustering.

---

## How to Run
1. Clone the repository or download the files.
2. Ensure you have Python and Jupyter Notebook installed.
3. Install required libraries using:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
4. Open the `.ipynb` files in Jupyter Notebook and run the cells step-by-step.
