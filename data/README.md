# Dataset files

- `dataset_1_fake_or_real_news/` is the 6,335-record dataset used by notebook 01. Its source notebook schema is `title`, `text`, `label`.
- `dataset_2_fake_news_detection/` is the 4,009-record dataset used by notebook 02. Its source notebook schema is `URLs`, `Headline`, `Body`, `Label`.

Each dataset is represented by the existing `train.csv` and `test.csv` files. The notebooks concatenate those files before preprocessing.
