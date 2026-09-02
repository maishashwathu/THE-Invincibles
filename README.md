# Polymer Property Prediction: An Invariance-First Multi-Property Model

This repository contains the codebase for a robust machine learning pipeline designed to predict seven key physical and electronic properties of polymers using their repeat-unit SMILES representations. The approach emphasizes structural invariance, advanced graph representation learning, and physical explainability.

## Key Highlights

* **Representation Invariance:** Implements a rigorous CRU mapping strategy as a foundational preprocessing step, ensuring that arbitrary string variations of the same physical polymer systematically resolve to identical model inputs.
* **Graph Representation Learning:** Utilizes an MPNN architecture, heavily boosted by self-supervised pretraining on large, unlabelled corpora to generate rich and stable molecular embeddings. 
* **Hybrid Feature Engineering:** Combines standard cheminformatics descriptors and fingerprints with custom, physics-directed feature operators to capture the underlying macroscopic properties of the chains.
* **Multi-Property Dynamics:** Exploits cross-task learning to maximize predictive power in low-data regimes, utilizing relationships between different physical and electronic properties.
* **Heterogeneous Ensembling:** Stacks a diverse roster of models—including Gradient Boosted Trees (LightGBM, XGBoost, CatBoost), Kernel methods, and Neural Networks—using a custom meta-learning protocol to ensure robust out-of-fold generalization.
* **Explainability:** Features a comprehensive attribution layer to audit model logic and map feature importances directly back to intelligible chemical domains.
