# Mall Customer Segmentation using K-Means Clustering

This project applies **K-Means Clustering** on the **Mall Customer
dataset** to segment customers into groups based on their demographic
and spending patterns. The analysis includes preprocessing, determining
the optimal number of clusters, clustering, visualization, and
evaluation.

------------------------------------------------------------------------

## 📂 Dataset

The dataset used is **Mall_Customers.csv**, which contains customer
details:

-   `CustomerID`\
-   `Gender`\
-   `Age`\
-   `Annual Income (k$)`\
-   `Spending Score (1–100)`

👉 Place the dataset in the correct path before running the code.

``` python
file_path = r"C:\Users\Dimple.S\Downloads\Mall_Customers.csv"
df = pd.read_csv(file_path)
```

------------------------------------------------------------------------

## ⚙️ Steps in the Code

### 1. **Load Dataset**

Reads the CSV file and displays the first few rows.

### 2. **Preprocessing**

-   Selects only numeric columns (`Age`, `Annual Income`,
    `Spending Score`).\
-   Standardizes features using **StandardScaler**.

### 3. **Elbow Method**

-   Runs KMeans for values of `k = 2 to 10`.\
-   Plots inertia values to identify the "elbow point" for optimal
    clusters.

### 4. **KMeans Clustering**

-   Applies KMeans with the chosen number of clusters (default = 5).\
-   Assigns cluster labels to the dataset.

### 5. **Visualization (PCA)**

-   Uses **PCA (2D)** to reduce dimensions for visualization.\
-   Plots clusters with different colors using **Seaborn**.

### 6. **Silhouette Score**

-   Calculates the **silhouette score** to measure clustering quality.

------------------------------------------------------------------------

## 📊 Example Output

### Elbow Method Graph

Shows inertia decreasing with cluster count.

### Cluster Visualization (PCA 2D)

Scatter plot of customers grouped into clusters.

### Silhouette Score

Example:

    Silhouette Score: 0.554

------------------------------------------------------------------------

## 📦 Requirements

Install dependencies using:

``` bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

------------------------------------------------------------------------

## ▶️ How to Run

1.  Download the dataset **Mall_Customers.csv**.\
2.  Update the `file_path` in the code with your dataset path.\
3.  Run the script.\
4.  Check outputs:
    -   Elbow method graph\
    -   Cluster visualization\
    -   Silhouette score

------------------------------------------------------------------------

## 🎯 Applications

-   Customer segmentation for targeted marketing.\
-   Identifying high-value customers.\
-   Designing personalized promotions.
