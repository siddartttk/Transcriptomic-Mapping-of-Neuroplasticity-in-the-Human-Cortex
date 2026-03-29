🧬 Transcriptomic Mapping of Neuroplasticity in the Human Cortex

📌 Overview

This project analyzes a 7.23 GB single-cell RNA sequencing (scRNA-seq) dataset from the human cerebral cortex to identify and map neural subtypes responsible for tissue repair. By isolating the expression of key recovery markers (such as BDNF and GAP43), this analysis provides a molecular foundation for understanding stroke recovery mechanisms and informing targeted neuro-rehabilitative therapies.

🧫 Biological & Clinical Context

While macroscopic therapies (such as VR-integrated motor rehabilitation) are crucial for post-stroke recovery, the underlying mechanism relies entirely on cellular neuroplasticity. This project utilizes the Siletti et al. (CytoTRACE) dataset to computationally isolate the specific cell clusters in the Middle Temporal Gyrus driving these regenerative pathways.

💻 Computational Pipeline

Handling high-dimensional transcriptomic data requires memory-efficient engineering. The pipeline was built in Python using Scanpy to process massive .h5ad matrices without overwhelming standard compute limits:

Data Ingestion: Utilized HDF5-backed AnnData objects for lazy loading and smart downsampling.

Quality Control: Filtered sparse genes and high-mitochondrial (stressed/dying) cells.

Dimensionality Reduction: Applied PCA (SVD solver) followed by UMAP to visualize the cellular latent space.

Unsupervised Clustering: Implemented the Leiden graph-clustering algorithm to define distinct neural populations.

Differential Expression: Queried specific plasticity and healing markers to annotate stroke-relevant clusters via Wilcoxon rank-sum testing.

📊 Key Visualizations

(Insert your UMAP brain map image here)
(Insert your Marker Gene Dot Plot image here)
