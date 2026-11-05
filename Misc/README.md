# Misc

Notebooks not tied to a product: assessment task and third-party model inference.

Data sources for every notebook: [`data_sources.csv`](data_sources.csv)

| # | Notebook | Task | Model | Classes | Result |
|---|---|---|---|---|---|
| 01 | [`01_openearthmap_landcover_segmentation_segformer_mit_b3_partial_labels.ipynb`](notebooks/01_openearthmap_landcover_segmentation_segformer_mit_b3_partial_labels.ipynb) | Semantic segmentation (9 classes, point labels) | SegFormer-style UNet, MiT-B3 encoder (segmentation-models-pytorch) | 9 land-cover classes | - |
| 02 | [`02_petrol_station_detection_onnx_inference.ipynb`](notebooks/02_petrol_station_detection_onnx_inference.ipynb) | Object detection inference | Pre-trained ONNX (HF coolroman/petrol-station-detect) | - | - |
