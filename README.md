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

The dataset folders were matched against the saved notebook outputs and the schemas used in the original experiments.

| Experiment | Dataset folder | Records reported by original notebook | Columns |
|---|---|---:|---|
| 1 | `data/dataset_1_fake_or_real_news/` | 6,335 | `title`, `text`, `label` |
| 2 | `data/dataset_2_fake_news_detection/` | 4,009 | `URLs`, `Headline`, `Body`, `Label` |

Each dataset is stored as `train.csv` and `test.csv`. The notebooks combine those two files to recreate the full dataset used in the experiments. Dataset 1 removes its original index-like `Unnamed` column during preprocessing; Dataset 2 removes rows with missing values as in the original workflow.

## Experiments and reported results

The following values are taken from the evaluation outputs saved in the original notebooks. They are historical experiment results; a fresh run with different library versions may produce slightly different values.

| Experiment | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Dataset 1 — Fake or Real News | 0.9061 | 0.9030 | 0.9101 | 0.9065 |
| Dataset 2 — Fake News Detection | 0.9749 | 0.9679 | 0.9784 | 0.9731 |

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

The notebooks locate the dataset folders whether Jupyter is started from the repository root or from the `notebooks/` directory. NLTK resources are downloaded by the notebooks when needed. Training may take a while on CPU.

## Notes

- The two experiments are independent and should be evaluated separately.
- The notebooks no longer require Google Drive or a Colab-specific file path.
- Saved cell outputs have been cleared to keep the notebooks lightweight and easier to render on GitHub.
- Other dataset folders previously present in this repository were not referenced by either notebook and have been removed from this project repository.

## Author

**Ali Rezapour** · [GitHub](https://github.com/Ali-Rzp) · [Portfolio](https://ali-rezapour.vercel.app/)
