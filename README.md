# Customer-segmentation-using-K-means-Clustering-1

## Overview
This project focuses on performing **customer segmentation** for a retail business (simulated via mall customer data) using the unsupervised machine learning algorithm **K-Means Clustering**. The primary goal is to identify distinct groups of customers based on their **Annual Income** and **Spending Score** to enable the marketing team to design targeted and effective strategies for each segment.

## Dataset
The project utilizes the **Mall Customers** dataset, which contains information about mall visitors.

| Column Name | Description |
| :--- | :--- |
| `CustomerID` | Unique identifier for each customer. |
| `Gender` | Gender of the customer. |
| `Age` | Age of the customer. |
| `Annual Income (k$)` | Annual income of the customer (in thousands of dollars). |
| `Spending Score (1-100)` | Score assigned by the mall based on customer behavior and spending habits, with 100 being the highest. |

**Source:** The data is loaded from a local CSV file named `Mall_Customers.csv`.

## Methodology

### 1. Data Preprocessing and Exploration
* The dataset contains 200 entries and 5 columns.
* Checked for and confirmed the absence of any **missing values** (`null` values) in the dataset.
* The clustering features were selected as **Annual Income (k$)** (column index 3) and **Spending Score (1-100)** (column index 4).

### 2. Determining Optimal Clusters (K)
* The **Elbow Method** was used to determine the optimal number of clusters (`K`) for the K-Means algorithm.
* This method plots the **Within Clusters Sum of Squares (WCSS)** against the number of clusters (1 to 10).
* The "elbow point" (where the rate of decrease in WCSS significantly slows down) typically indicates the optimal number of clusters.

### 3. K-Means Clustering
* The `KMeans` model from `sklearn.cluster` was initialized and trained on the selected features.
* The analysis proceeds by fitting the model with the chosen optimal number of clusters (`K=5` is the common result for this dataset, although the final notebook output is needed to confirm the exact value used in the scatter plot).

### 4. Visualization and Interpretation
* A scatter plot is generated to visualize the final clusters, showing customer groups based on their Annual Income and Spending Score.
* Each cluster represents a distinct customer segment, allowing for interpretation (e.g., "High Income, High Spending," "Low Income, Low Spending," etc.).

## Requirements
To run this notebook, you will need the following Python libraries:
* `numpy`
* `pandas`
* `matplotlib`
* `seaborn`
* `scikit-learn` (`sklearn`)

## How to Run

1.  **Clone the repository** (if applicable).
2.  Ensure the `Mall_Customers.csv` file is in the same directory as the Jupyter Notebook or update the file path in the notebook.
3.  Open the notebook: `Project_13_Customer_Segmentation_using_K_Means_Clustering.ipynb` in a Jupyter environment (Jupyter Lab, Google Colab, etc.).
4.  Run the cells sequentially.
