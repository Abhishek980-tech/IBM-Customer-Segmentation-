# IBM Investment Customer Segmentation

## Overview
This project performs customer segmentation for investment customers using unsupervised machine learning techniques (KMeans, GMM, DBSCAN) with PCA dimensionality reduction. It analyzes investment data to identify clusters, generates visualizations, and provides business insights.

Key features:
- Data preprocessing and scaling
- Multiple clustering models
- Model comparison and optimal cluster selection
- Cluster profiles and risk/ROI analysis
- Streamlit app for interactive exploration (`app.py`)

## Dataset
- `data/investment_customers.csv`: Main dataset with investment customer features.

## Preprocessing & Models
- Features scaled using `StandardScaler` (`models/scaler.pkl`)
- PCA model: `models/pca_model.pkl`
- Clustering models:
  - KMeans: `models/kmeans_model.pkl`
  - GMM: `models/gmm_model.pkl`
  - DBSCAN: `models/dbscan_model.pkl`
- Preprocessor: `models/preprocessor.pkl`
- Metadata: `models/model_metadata.json`, `models/feature_names.txt`, `models/label_encoders.pkl`

## Outputs
- `outputs/clustered_dataset.csv`: Dataset with cluster labels
- Visualizations:
  - `dataset_analysis.png`, `feature_distributions.png`
  - `optimal_clusters_analysis.png`, `pca_clusters.png`
  - `cluster_comparison.png`, `basic_cluster_distribution.png`
  - `risk_roi_analysis.png`
- Insights: `outputs/business_insights.json`, `outputs/cluster_profiles.json`, `outputs/cluster_summaries.json`

## Setup
1. Clone the repo:
   ```
   git clone https://github.com/Abhishek980-tech/IBM-Customer-Segmentation-.git
   cd IBM-Customer-Segmentation-
   ```

2. Create virtual environment:
   ```
   python -m venv venv
   venv\\Scripts\\activate  # Windows
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

## Usage
### Run Streamlit App
```
streamlit run app.py
```
Open http://localhost:8501 for interactive cluster analysis.

### Training Scripts (if needed)
- `data/train_models.py`: Train and save models
- `data/visuals.py`: Generate plots

## Results
- Cluster profiles and summaries saved in `outputs/`
- Business insights in `outputs/business_insights.json`

## Dependencies
See `requirements.txt` for full list (Streamlit, scikit-learn, pandas, plotly, etc.).

## License
MIT License
