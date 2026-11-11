# Fake News Detection with BiLSTM

This repository contains two independent fake-news classification experiments using Bidirectional LSTM (BiLSTM) networks. Each notebook uses its own dataset and preprocessing pipeline.

## Repository structure

```text
.
├── data/
│   ├── dataset_1_fake_or_real_news/
│   │   ├── train.csv
│   │   └── test.csv
│   └── dataset_2_fake_news_detection/
│       ├── train.csv
│       └── test.csv
├── notebooks/
│   ├── 01_fake_or_real_news_bilstm.ipynb
│   └── 02_fake_news_detection_bilstm.ipynb
├── .gitignore
├── requirements.txt
└── README.md
```

## Datasets

The dataset folders were matched against the schemas and data-loading logic in the original notebooks.

| Experiment | Dataset folder | Records reported in original notebook | Columns |
|---|---|---:|---|
| 1 | `data/dataset_1_fake_or_real_news/` | 6,335 | `text`, `label` |
| 2 | `data/dataset_2_fake_news_detection/` | 4,138 (3,340 train + 798 test) | `text`, `label` |

Each dataset is stored in its original `train.csv` and `test.csv` files. The updated notebooks keep these files separate: validation data is split from the training file, and the provided test file is reserved for final evaluation. Dataset 1 removes its original index-like `Unnamed` column if present. Both experiments remove rows missing required text or label values.

## Verified test results

The following metrics were obtained by running the updated notebooks in Google Colab. Each experiment uses its supplied test file for final evaluation; validation data is split from the training file only.

| Experiment | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Dataset 1 — Fake or Real News | 0.9127 | 0.8924 | 0.9402 | 0.9156 |
| Dataset 2 — Fake News Detection | 0.9649 | 0.9706 | 0.9483 | 0.9593 |

Results can vary slightly between runs because neural-network training is stochastic. These values are the reported results from the Colab runs.

## Setup

Use Python 3.10 or 3.11.

1. Clone the repository:
   ```bash
   git clone https://github.com/Ali-Rzp/-fake-news-detection-using-bilstm.git
   cd -fake-news-detection-using-bilstm
   ```

2. Create a virtual environment:
   ```bash
   python -m venv .venv
   ```

   Activate it on Windows:
   ```powershell
   .venv\Scripts\Activate.ps1
   ```

   Or on macOS/Linux:
   ```bash
   source .venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   python -m pip install --upgrade pip
   pip install -r requirements.txt
   ```

4. Launch Jupyter:
   ```bash
   jupyter notebook
   ```

5. Open either notebook under `notebooks/` and run its cells from top to bottom.

The notebooks locate the dataset folders whether Jupyter is started from the repository root or from the `notebooks/` directory. Required NLTK resources are downloaded by the notebooks when needed. Training may take a while on CPU.

## Notes

- The two experiments are independent and should be evaluated separately.
- The notebooks do not require Google Drive or Colab-specific file paths.
- Saved cell outputs have been cleared to keep the notebooks lightweight and easier to render on GitHub.
- Dataset folders not referenced by either original notebook were removed from this project repository.

## Author

**Ali Rezapour** · [GitHub](https://github.com/Ali-Rzp) · [Portfolio](https://ali-rezapour.vercel.app/)
