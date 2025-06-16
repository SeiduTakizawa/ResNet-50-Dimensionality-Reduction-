# Dimensionality Reduction and Clustering Techniques

## 📌 Project Summary

This project explores multiple techniques for dimensionality reduction and unsupervised clustering on high-dimensional datasets. Conducted as part of the **Machine Learning (MYE002)** course at the University of Ioannina in **May 2025**, the project compares PCA, LLE, and Autoencoders and their impact on clustering quality.

**Team Members:**

* Vasileios Papadimitriou 

  **Instructor:** K. Blekas

---

## 🎯 Objectives

* Apply and compare three dimensionality reduction techniques:

  * PCA (Principal Component Analysis)
  * LLE (Locally Linear Embedding)
  * Deep Autoencoders
* Evaluate clustering performance post-reduction using:

  * KMeans (Euclidean & Cosine distance)
  * Agglomerative Clustering
* Metrics used: Silhouette Score, Purity, F-Measure

---

## 🧪 Methods & Experiments

### 🔷 PCA (Principal Component Analysis)

* Reduced dimensions to 2, 3, 5, 10, 20 components
* Visualized clusters in 2D & 3D plots
* Captured variance:

  * 5D: 82.14%
  * 10D: 89.25%
  * 20D: 94.36%

#### Clustering After PCA

* Best Silhouette Score: **0.5881** (KMeans, Euclidean, M=2, k=2)
* Purity and F-Measure followed similar trends

### 🔷 LLE (Locally Linear Embedding)

* Non-linear technique, preserving local geometry
* Reduced dimensions: 2, 3, 5, 10, 20 with `n_neighbors=10`
* Captured more complex structures vs PCA

#### Clustering After LLE

* Best Silhouette Score: **0.8148** (KMeans, Euclidean, M=2, k=3)
* Cosine distance further improved results when normalized

### 🔷 Autoencoders

* Deep Neural Network with 2 hidden layers: 256 and 128 neurons
* Latent code dimensionality: 2, 3, 5, 10, 20
* Visualized 2D/3D latent space representations

#### Clustering After Autoencoders

* Best Silhouette Score: **0.5483** (M=2, KMeans Euclidean)
* Slightly lower performance compared to LLE, but strong structure preservation

---

## 📈 Evaluation Metrics

* **Silhouette Score**: Measures cohesion & separation
* **Purity**: Agreement with ground truth labels
* **F-Measure**: Balance between precision and recall

---


## 🧠 Insights

* LLE consistently outperformed PCA and Autoencoders in clustering quality (Silhouette score)
* Autoencoders preserved structural info but required careful tuning
* PCA remains useful for variance retention and initial exploration

---

## 📚 References

* Scikit-learn documentation
* Hinton & Salakhutdinov (2006), "Reducing the Dimensionality of Data with Neural Networks"
* Tenenbaum et al. (2000), "A Global Geometric Framework for Nonlinear Dimensionality Reduction"

---

## 🎓 Acknowledgments

University of Ioannina — Machine Learning Course (MYE002)

Instructor: **K. Blekas**

Team: **Vasileios Papadimitriou **
