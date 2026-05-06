# Calligraphy Identifier

Calligraphy Identifier is a research project for identifying Chinese calligraphy single-character images by script style and calligrapher.

## Task

The project focuses on classifying cropped Chinese calligraphy character images. The target tasks are:

- Script style classification, such as regular script, seal script, cursive script, running script, and clerical script.
- Calligrapher identification from single-character calligraphy images.

## Methods

The planned modeling approaches include:

- Direct calligrapher classification: train one model to predict the calligrapher directly from the preprocessed character image.
- Two-stage classification: first classify the script style, then use a style-aware classifier or per-style classifier to predict the calligrapher.

## Data

Current data sources are:

- Self-crawled Shufazidian dataset.
- MCCD dataset.

Datasets are not included in this repository due to size and copyright considerations. Raw images, processed images, downloaded datasets, model weights, checkpoints, and cache files should remain local and are ignored by git.

## Preprocessing

The preprocessing notebook outputs fixed-size `96 x 96` grayscale images. The preprocessing is designed to preserve calligraphy stroke details, including brush texture, dry-brush effects, and stroke endings, instead of converting the result to a binary image.

Main notebook:

- `preprocess_calligraphy_96.ipynb`

By default, the notebook uses `RUN_FULL = False` and only processes a small sample for validation. Set `RUN_FULL = True` inside the notebook to process the full local dataset.

## Repository Contents

This repository should contain source code, notebooks, small configuration files, scripts, and environment files only. It should not contain datasets, generated images, model checkpoints, API keys, or local cache files.
