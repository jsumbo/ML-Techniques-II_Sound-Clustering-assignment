# Sound Dataset Clustering

This repository contains a Jupyter notebook for performing clustering on an unlabeled dataset of 3,000 sound recordings. The project involves extracting audio features, applying dimensionality reduction techniques, implementing clustering algorithms, and evaluating their performance.

## Project Overview

The goal of this project is to identify potential clusters within a dataset of unlabeled sound recordings. The process includes:

1.  **Data Loading and Feature Extraction:** Loading `.wav` audio files and extracting Mel Spectrogram features.
2.  **Dimensionality Reduction:** Applying PCA and t-SNE to reduce the dimensionality of the feature data for visualization and improved clustering.
3.  **Clustering:** Implementing and applying K-Means and DBSCAN clustering algorithms.
4.  **Evaluation:** Evaluating the performance of the clustering algorithms using metrics such as Silhouette Score and Davies-Bouldin Index.

## Dataset

The dataset consists of 3,000 unlabeled sound recordings in `.wav` format. The data is expected to be located in a directory accessible from the notebook environment, specifically within a Google Drive path.

**Note:** The notebook assumes the data is located at `/content/drive/My Drive/sound data/unlabelled_sounds`. You may need to adjust this path in the notebook to match your setup.

## Setup and Running the Notebook

The project is implemented as a Jupyter notebook, designed to be run in a Google Colab environment for easy access to Google Drive and necessary libraries.

1.  **Open the Notebook:** Upload and open the `[Notebook Name].ipynb` file in Google Colab.
2.  **Mount Google Drive:** Run the cell that mounts Google Drive to access the dataset. You will be prompted to authorize Colab to access your Google Drive files.
3.  **Install Libraries:** Run the cell that installs the `librosa` library and imports all necessary Python packages.
4.  **Run Cells Sequentially:** Execute the notebook cells in sequential order. The notebook is structured to guide you through the data loading, feature extraction, dimensionality reduction, clustering, and evaluation steps.

The notebook includes explanations and visualizations at each stage of the process.

## Results Summary

The analysis explored clustering the sound data using K-Means and DBSCAN on both PCA and t-SNE reduced feature data.

*   **Dimensionality Reduction:** t-SNE was found to provide better visual separation of potential clusters compared to PCA, suggesting the data has a non-linear structure.
*   **Clustering Performance:** K-Means generally performed more robustly and provided more interpretable clusterings than DBSCAN in this context. K-Means applied to the t-SNE reduced data with 10 clusters yielded a Silhouette Score of 0.37 and a Davies-Bouldin Index of 0.90, indicating a reasonable balance of cluster cohesion and separation.

The notebook provides detailed evaluation metrics and visualizations to support these findings.

## Dependencies

The main libraries used in this project are:

*   `numpy`
*   `librosa`
*   `os`
*   `google.colab.drive`
*   `pandas`
*   `seaborn`
*   `matplotlib`
*   `sklearn`

These dependencies are installed or available in the Google Colab environment. The `librosa` library is explicitly installed within the notebook.
