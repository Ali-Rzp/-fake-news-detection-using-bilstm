# Fake News Detection Using Bidirectional LSTM

This project explores fake-news classification using Bidirectional Long Short-Term Memory (Bi-LSTM) neural networks. Separate notebooks are provided for two datasets.

## Project Structure

| File / Folder | Description |
|---|---|
| [fake_news_detection_using_bi_lstm_dataset_1.ipynb](./fake_news_detection_using_bi_lstm_dataset_1.ipynb) | Model development and evaluation on dataset 1 |
| [fake_news_detection_using_bilstm_dataset_2.ipynb](./fake_news_detection_using_bilstm_dataset_2.ipynb) | Model development and evaluation on dataset 2 |
| [Fake News Dataset](./Fake%20News%20Dataset/) | Dataset 1 files |
| [News _dataset](./News%20_dataset/) | Dataset 2 files |

## Model

The notebooks implement a text-classification workflow using a Bidirectional LSTM architecture. Each dataset is handled in its own notebook so the experiments and evaluation can be reviewed separately.

## Results

For the first dataset, the reported evaluation metrics are:

| Metric | Score |
|---|---:|
| Accuracy | 0.9749 |
| Precision | 0.9679 |
| Recall | 0.9784 |

These figures refer to the first dataset only. Results for the second dataset should be taken from its notebook.

## Running the Notebooks

1. Open the relevant notebook in Jupyter Notebook, JupyterLab, or Google Colab.
2. Make sure the dataset files are available at the paths expected by that notebook.
3. Install the Python packages imported in the notebook if they are not already installed.
4. Run the cells in order, including preprocessing, training, and evaluation.

> **Reproducibility note:** Dependency versions and dataset setup instructions should be documented after verifying the imports and file paths in both notebooks.

## Author

**Ali Rezapour** — [GitHub](https://github.com/Ali-Rzp) · [Portfolio](https://ali-rezapour.vercel.app/)
