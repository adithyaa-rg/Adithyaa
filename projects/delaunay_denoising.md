---
title: "Delaunay-Based Point Cloud Denoising"
layout: default
---

## De(l)Noise: Delaunay Triangulation-Aided Point Cloud Denoising

**Advisor:** Prof. Ramanathan M, Advanced Geometric Computational Lab, IIT Madras  
**Duration:** December 2023 – October 2024  
**Published:** Computers & Graphics, 2025 &nbsp;|&nbsp; [View paper](https://www.sciencedirect.com/science/article/pii/S0097849325001517)

---

### Background

3D point clouds — captured by LiDAR, depth cameras, or photogrammetry — are fundamental to robotics, autonomous driving, and computer graphics. In practice, these scans always contain noise: sensor inaccuracies, reflections, and measurement errors add spurious points that corrupt the underlying surface geometry. Removing this noise without destroying fine geometric features is a hard problem.

---

### Algorithm

The De(l)Noise algorithm combines classical computational geometry with statistical surface fitting:

**1. Delaunay-Based Clustering**  
Rather than operating on raw nearest-neighbour neighbourhoods (which are sensitive to noise), we first compute the **3D Delaunay triangulation** of the point cloud. Delaunay connectivity captures geometric proximity more reliably, giving us stable local clusters even in noisy conditions.

**2. Moving Least Squares (MLS) Surface Fitting**  
Within each cluster, we fit a smooth surface using Moving Least Squares. This provides a local reference surface for each point, allowing us to measure how much each point deviates from the true underlying geometry.

**3. PCA-Based Feature Extraction**  
We apply PCA to each local neighbourhood to extract surface normal estimates and curvature signatures. High-curvature regions (sharp edges, corners) are detected and treated differently from flat regions to avoid over-smoothing features.

**4. Curve Fitting & Outlier Removal**  
Points with deviation scores beyond an adaptive threshold are flagged as noise or outliers and removed. The remaining points are optionally repositioned towards the fitted surface for denoising.

---

### Results

We evaluated De(l)Noise on synthetic datasets with controlled noise levels and compared against:

- Deep learning-based methods (PointNet++ variants)
- Optimisation-based methods (bilateral filtering, CLOP)
- Classical statistical outlier removal (PCL RadiusOutlier)

De(l)Noise achieved competitive denoising quality while remaining interpretable, parameter-light, and free of training data requirements — making it practically useful for deployment on novel scene types.

---

### Tools

`Python` &nbsp;·&nbsp; `CGAL` &nbsp;·&nbsp; `Open3D` &nbsp;·&nbsp; `NumPy` &nbsp;·&nbsp; `Matplotlib`
