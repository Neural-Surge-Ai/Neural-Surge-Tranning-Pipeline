# Neural Surge - Training Pipelines

Kaggle training notebooks for Neural Surge projects, grouped by project.

| Folder | Project | Contents |
|---|---|---|
| [`MediGraph/`](MediGraph) | MediGraph | Medical-imaging classifiers and detectors (kidney, liver, brain, CT, bone, spine, chest X-ray) |
| [`Jonas/`](Jonas) | Jonas | Qwen3-14B LLM + PaddleOCR document pipeline for finance / AP invoices |
| [`data_sources/`](data_sources) | - | `all_data_sources.csv` (every dataset / pretrained model used) and `notebook_inventory.csv` (notebook -> task, model, result, original filename) |

Each project folder has:

```
<Project>/
├── README.md          # notebook table: task, model, classes, result
├── data_sources.csv   # datasets / pretrained models used by this project
└── notebooks/         # .ipynb files, named <nn>_<data>_<task>_<model>.ipynb
```

All notebooks were written for Kaggle (`/kaggle/input/...` paths). Datasets owned by `ahmedshayan1` may be private.
