🧬 Yeast Gene Expression Visualization
Overview

This project explores the Yeast gene expression dataset using dimensionality reduction techniques to visualize multi-label data.

Goals:

Load and preprocess the data ✅

Identify top single-label and multi-label categories 🏷️

Scale features for distance-based methods 📏

Visualize using t-SNE and Isomap 📊

Detect outliers and noisy labels ⚠️

Dataset

Files: yeast.arff (data), yeast.xml (labels)

Features: Numerical gene expression values

Labels: Multi-label functional categories

Preprocessing

Decode bytes → strings 📝

Separate features (X_df) and labels (Y_df)

Assign label names from XML

Scale features with StandardScaler

Dimensionality Reduction
t-SNE 🎯

Focuses on local structure

Produces tight clusters

Perplexity: 30 for best balance

Isomap 🌐

#Focuses on global structure

Reveals continuous curved manifold

n_neighbors: 10

Color scheme:

🔴 Dark red → TopSingle_1

🟢 Dark green → TopSingle_2

⚪ Gray → Most frequent multi-label

💛 Light yellow → Other

Outliers & Noisy Labels

Outliers detected using Z-score

Noisy labels detected via nearest neighbors

Highlighted with distinct colors for clarity 🔎

Mixed-Label Regions

Points with overlapping classes are hard to classify

Simple linear models fail here ❌

Non-linear models are recommended ✅

Comparison Plots

t-SNE: Shows local clusters

Isomap: Shows global manifold

Side-by-side plots for comparison 🖼️
