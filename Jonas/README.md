# Jonas

LLM (Qwen3-14B) and OCR pipeline for the Jonas finance / AP-invoice agent.

Data sources for every notebook: [`data_sources.csv`](data_sources.csv)

| # | Notebook | Task | Model | Classes | Result |
|---|---|---|---|---|---|
| 01 | [`01_qwen3_14b_4bit_finance_ap_invoice_agent.ipynb`](notebooks/01_qwen3_14b_4bit_finance_ap_invoice_agent.ipynb) | LLM loading + prompt test | Qwen3-14B, 4-bit NF4 (bitsandbytes), Unsloth setup | - | - |
| 02 | [`02_qwen3_14b_inference_quickstart.ipynb`](notebooks/02_qwen3_14b_inference_quickstart.ipynb) | LLM inference test | Qwen3-14B (transformers) | - | - |
| 03 | [`03_invoice_ocr_high_accuracy_paddleocr_v6_gpu.ipynb`](notebooks/03_invoice_ocr_high_accuracy_paddleocr_v6_gpu.ipynb) | OCR (document text extraction) | PaddleOCR PP-OCRv6 medium det+rec, GPU | - | - |
| 04 | [`04_document_ocr_text_extraction_paddleocr_cpu.ipynb`](notebooks/04_document_ocr_text_extraction_paddleocr_cpu.ipynb) | OCR (document text extraction) | PaddleOCR (CPU) | - | - |
