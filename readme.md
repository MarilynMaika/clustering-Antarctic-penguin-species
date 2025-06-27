# 🐧 Penguin Clustering with K-Means

## 📌 Project Overview

This project explores how unsupervised machine learning — specifically **K-Means clustering** — can be used to group penguins in Antarctica based on their physical characteristics. Although the dataset lacks species labels, it’s known that **three penguin species** inhabit the region: Adelie, Chinstrap, and Gentoo.

The goal is to identify natural clusters in the data that may align with these species using **scikit-learn’s KMeans algorithm**.

---

## 📊 Dataset Description

The dataset used is `penguins.csv`, which contains 5 columns:

| Column              | Description                               |
|---------------------|-------------------------------------------|
| `culmen_length_mm`  | Culmen (beak) length in millimeters       |
| `culmen_depth_mm`   | Culmen (beak) depth in millimeters        |
| `flipper_length_mm` | Flipper length in millimeters             |
| `body_mass_g`       | Body mass in grams                        |
| `sex`               | Sex of the penguin (male or female)       |

> 🧭 **Data Source**:  
> The dataset was collected and made available by **Dr. Kristen Gorman** and the **Palmer Station, Antarctica LTER**, a member of the **Long Term Ecological Research Network (LTER)**.

> 🧠 **Note**:  
> This project was a supervised DataCamp learning project.

---

## 🎯 Objectives

- Perform **data cleaning and preprocessing**
- Standardize features for effective clustering
- Apply **K-Means Clustering**
- Use the **Elbow Method** to determine the optimal number of clusters
- Visualize and interpret the resulting clusters

---

## 🧪 Methodology

### ✅ Data Preparation
- Removed rows with missing values
- Encoded categorical variable `sex` using one-hot encoding
- Standardized numeric features using `StandardScaler` to ensure equal influence in clustering

### ✅ Clustering
- Tested `k` values from 1 to 9 using the **Elbow Method**
- Selected the optimal number of clusters where the inertia starts to level off
- Applied **K-Means** with the selected `k`
- Visualized clusters using 2D plots

---

## 🛠 Tools Used

- Python
- Pandas & NumPy
- Scikit-learn (`KMeans`, `StandardScaler`)
- Seaborn & Matplotlib for visualizations

---

## 📈 Results

- The Elbow plot suggested that **3 clusters** is optimal — aligning with the known number of penguin species
- Physical attributes like **flipper length** and **body mass** contributed most to cluster separation
- The clustering revealed clear groupings, showing that K-Means can reasonably approximate species without labels

---

## 📁 Project Structure

penguin-clustering/

- penguins.csv
- penguin_clustering.ipynb
- elbow_plot.png
- cluster_plot.png
