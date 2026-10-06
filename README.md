# Predicting Customer Ratings for Amazon Beauty Products

Welcome to the **Predicting Customer Ratings for Amazon Beauty Products** project! This repository contains a Google Colab Notebook that walks through building a mathematical recommendation system to predict customer ratings and suggest similar items using collaborative filtering techniques.

---

## Project Overview
This project processes a massive e-commerce dataset to build an item-based recommendation system. By converting raw user interactions into a structured utility matrix, applying **Linear Algebra (Truncated SVD)** for dimensionality reduction, and calculating statistical correlations, the system successfully uncovers hidden relationships between products to make accurate recommendations.

---

## Dataset
The system utilizes an Amazon Beauty Products dataset containing **over 2 million customer reviews and ratings** with the following features:
* `UserId`: Unique identifier for each customer.
* `ProductId`: Unique identifier for each beauty product.
* `Rating`: Explicit rating given by the user to the product (1–5 star scale).
* `Timestamp`: The recorded time of the rating.

---

## Table of Contents
1. [Tech Stack](#%EF%B8%8F-tech-stack)
2. [Project Steps & Architecture](#%EF%B8%8F-project-steps--architecture)
3. [Results & Examples](#-results--examples)
4. [How to Run](#-how-to-run)

---

## Tech Stack
* **Language:** Python
* **Environment:** Google Colab / Jupyter Notebooks
* **Libraries:** Pandas, NumPy, Scikit-Learn (`TruncatedSVD`), Matplotlib, Seaborn

---

## Project Steps & Architecture

* **Step 1: Download the Dataset** – Acquired the large-scale customer dataset from Kaggle.
* **Step 2: Import Required Libraries** – Loaded the necessary tools for matrix manipulation, decomposition, and plotting.
* **Step 3: Load the Dataset** – Ingested the raw review files into a Pandas DataFrame.
* **Step 4: Drop Irrelevant Columns** – Cleansed the data by removing metrics (like timestamps) not required for filtering.
* **Step 5: Data Visualization** – Executed EDA to analyze the global distribution of ratings across the platform.
* **Step 6: Building the Utility Matrix** – Constructed a sparse User-Item matrix mapping specific ratings from users to individual products.
* **Step 7: Transposing the Matrix** – Swapped rows and columns to re-orient the framework for product-centric similarity testing.
* **Step 8: Decomposing the Matrix** – Executed **Truncated Singular Value Decomposition (SVD)** to compress the sparse matrix into key latent features.
* **Step 9: Generating the Correlation Matrix** – Calculated a **Pearson Correlation Matrix** across the decomposed product space.
* **Step 10: Recommending Top Correlated Products** – Programmed the final inference logic to surface the top 5 highly correlated items for any item target.

---

## Results & Examples
The mathematical framework successfully identifies highly relevant product cross-recommendations. For example, when querying the target product **`B00004TMFE`**, the system outputs the following top 5 mathematically correlated items:

1. `B000052WYD`
2. `B00012NI7E`
3. `B00013TQRE`
4. `B0001TQ9WI`
5. `B00027DMLK`

---

## How to Run
1. **Clone this repository** to your local machine:
   ```bash
   git clone https://github.com
   ```
2. Open the notebook file in **Google Colab** or setup a local Jupyter workspace.
3. Install the required data science packages:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
4. Run the code cells sequentially to process the matrices and compute the similarity correlations!
