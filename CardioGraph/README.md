# CardioGraph

Cardiac AI models for the CardioGraph assistant: 12-lead ECG interpretation and echocardiogram ejection fraction.

Data sources for every notebook: [`data_sources.csv`](data_sources.csv)

| # | Notebook | Task | Model | Output | Result |
|---|---|---|---|---|---|
| 01 | [`01_ecg_12lead_multilabel_classification_ptbxl_tf_efficientnet_b0.ipynb`](notebooks/01_ecg_12lead_multilabel_classification_ptbxl_tf_efficientnet_b0.ipynb) | Multi-label classification (52 SCP-ECG statements) | timm tf_efficientnet_b0 (ImageNet), ECG signal -> 224x224 image | 52 label probabilities | Production checkpoint: val macro AUC **0.893** |
| 02 | [`02_echo_ejection_fraction_regression_echonet_dynamic_r2plus1d_18.ipynb`](notebooks/02_echo_ejection_fraction_regression_echonet_dynamic_r2plus1d_18.ipynb) | Video regression (ejection fraction %) | torchvision R(2+1)D-18 (Kinetics-400), 32 frames / period 2 | EF % + category | Run on Kaggle GPU |

## Notes

- **ECG:** labels, preprocessing and checkpoint keys match the `ECG_Model` FastAPI service (`inference.py`).
  Copy the trained `timm_efficientnet_b0_imagenet_ecg_multilabel_hr_500hz_best.pth` into `ECG_Model/model/` to deploy.
- **Echo:** predicts LV ejection fraction from an apical-4-chamber cine loop. Categories: reduced <= 40 %, mildly reduced 41-49 %, normal >= 50 %.
- Both notebooks find their dataset under `/kaggle/input` automatically. Set `SMOKE_TEST=1` for a quick CPU check of the pipeline.
- These pipelines were rebuilt because the original Kaggle notebooks were not kept.
