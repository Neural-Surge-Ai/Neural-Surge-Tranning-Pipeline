# MediGraph

Medical-imaging models (ultrasound, CT, MRI, X-ray) for the MediGraph diagnostic assistant.

Data sources for every notebook: [`data_sources.csv`](data_sources.csv)

| # | Notebook | Task | Model | Classes | Result |
|---|---|---|---|---|---|
| 01 | [`01_abdominal_organ_detection_kidney_liver_spleen_yolo26s.ipynb`](notebooks/01_abdominal_organ_detection_kidney_liver_spleen_yolo26s.ipynb) | Object detection (ROI cropping) | YOLO26s (Ultralytics) | Kidney, Liver, Spleen | mAP50 0.993 / mAP50-95 0.974 |
| 02 | [`02_kidney_ultrasound_stone_vs_normal_efficientnet.ipynb`](notebooks/02_kidney_ultrasound_stone_vs_normal_efficientnet.ipynb) | Binary classification | EfficientNet-B0 / B3 (torchvision) | Normal, Stone | Unseen-test acc 0.58 / F1 0.71 (12 imgs) |
| 03 | [`03_kidney_ultrasound_normal_vs_abnormal_vit_b16_effnet_b3_ensemble.ipynb`](notebooks/03_kidney_ultrasound_normal_vs_abnormal_vit_b16_effnet_b3_ensemble.ipynb) | Binary classification | ViT-B/16 + EfficientNet-B3 ensemble, Focal loss | Normal, Abnormal (cyst/stone/tumor) | Unseen-test acc 0.55 / F1 0.49 |
| 04 | [`04_kidney_ultrasound_normal_vs_abnormal_resnet50_cbam_custom_cnn.ipynb`](notebooks/04_kidney_ultrasound_normal_vs_abnormal_resnet50_cbam_custom_cnn.ipynb) | Binary classification | Custom ResNet50 + CBAM attention | Normal, Abnormal | Val acc ~91% / unseen-test acc 55.6% |
| 05 | [`05_liver_cancer_lesion_detection_yolo26s.ipynb`](notebooks/05_liver_cancer_lesion_detection_yolo26s.ipynb) | Object detection | YOLO26s (Ultralytics) | 3 lesion classes (0,1,2) | mAP50 0.728 / mAP50-95 0.43 |
| 06 | [`06_brain_mri_tumor_classification_efficientnet_b3.ipynb`](notebooks/06_brain_mri_tumor_classification_efficientnet_b3.ipynb) | 4-class classification | EfficientNet-B3 (torchvision) | Glioma, Meningioma, No tumor, Pituitary | Test acc 0.945 / F1 0.944 |
| 07 | [`07_brain_mri_tumor_detection_yolo11s.ipynb`](notebooks/07_brain_mri_tumor_detection_yolo11s.ipynb) | Object detection | YOLO11s (Ultralytics) | Tumor | mAP50 0.959 / mAP50-95 0.751 |
| 08 | [`08_ct_scan_cancer_vs_normal_classification_efficientnet_b0.ipynb`](notebooks/08_ct_scan_cancer_vs_normal_classification_efficientnet_b0.ipynb) | Binary classification | EfficientNet-B0 (torchvision) | Cancer, Normal | Val acc 0.993 / F1 0.993 |
| 09 | [`09_bone_xray_fracture_classification_efficientnet_b3.ipynb`](notebooks/09_bone_xray_fracture_classification_efficientnet_b3.ipynb) | Binary classification | EfficientNet-B3 (torchvision) | Fractured, Not fractured | Val acc 0.69 / F1 0.77 (2 epochs) |
| 10 | [`10_spine_xray_scoliosis_spondylolisthesis_classification_efficientnet_b3.ipynb`](notebooks/10_spine_xray_scoliosis_spondylolisthesis_classification_efficientnet_b3.ipynb) | 3-class classification | EfficientNet-B3 (torchvision) | Normal, Scoliosis, Spondylolisthesis | Test acc 0.96 / F1 0.95 |
| 11 | [`11_chest_xray_input_validator_efficientnet_b3_embeddings.ipynb`](notebooks/11_chest_xray_input_validator_efficientnet_b3_embeddings.ipynb) | Input gate (embedding similarity) | EfficientNet-B3 feature extractor | Chest X-ray vs other image | Threshold 0.75 cosine sim |
| 12 | [`12_spine_xray_vindr_spinexr_dataset_download.ipynb`](notebooks/12_spine_xray_vindr_spinexr_dataset_download.ipynb) | Data download | - | - | - |

> `12_spine_xray_vindr_spinexr_dataset_download.ipynb` reads PhysioNet credentials from the `PHYSIONET_USER` / `PHYSIONET_PASSWORD` environment variables.
