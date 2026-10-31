# Shoplifting_Detection — Multi-Model Shoplifting Detection Benchmark

## Overview
- **Project 1 (3D CNNs)**: `R(2+1)D` baseline vs. `DMD-A-Net` (Frame-Differential Motion Gate + Temporal Concealment Cross-Attention)
- **Project 2 (Video Transformers)**: `TimeSformer` baseline vs. `TCA-ViT` (Motion-Salience Patch Gate + Occlusion Gradient Head)
- **Project 3 (Skeleton GCNs, YOLOv26n-pose)**: `ST-GCN` vs. `CTR-GCN` vs. `VDA-GCN` (Velocity-Gated Temporal Conv + Directed Concealment Adjacency)

## Cross-Dataset Evaluation Plan (`NaveenKumarGottipalli/Shoplifting_DataCollection`)
- **Training & validation corpus**: `S3` + `Shop DataSet` + `UCF-Crime`
- **Unseen real-world test set**: `DCSASS Dataset` (`DCSASS Dataset/Labels/Shoplifting.csv`)

## Repository structure
- `dataset_splits/` — verified sample manifests (`train.json`, `val.json`, `test.json`, `verified_all.json`, `quarantined.json`), `viability_report.csv`, dataset charts and input→output sample figures
- `Project_1_R2Plus1D_DMD_ANet/` — `results/` (JSON metrics), `figures/` (accuracy / loss / ROC / confusion matrix / input-vs-output), `figures/limitations/` (17 limitation figures), `models/` (trained weights)
- `Project_2_TimeSformer_TCA_ViT/` — same layout, 15 limitation figures
- `Project_3_Skeleton_GCNs/` — same layout, 8 limitation figures, plus the YOLO pose model in `models/`
- `All_Projects_Comparison/` — cross-project summary table (`all_models_summary.csv`) and combined ROC / F1 / AUC chart
- `MANIFEST.csv` — every file with its size and SHA-256

Model weights above GitHub's 100 MB limit are hosted on Hugging Face (`NaveenKumarGottipalli/Shoplifting_Detection`), Kaggle and Google Drive instead.
