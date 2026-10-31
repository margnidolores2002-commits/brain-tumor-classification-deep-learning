
# Brain Tumor Classification with Transfer Learning

This project explores a **multi-class brain tumor MRI classification problem** using deep learning and transfer learning techniques.

The objective is to compare different convolutional neural network architectures, identify the best-performing model, and evaluate how well the selected models generalize to a separate external dataset.

This project was developed collaboratively as part of a university group assignment.

## Project Overview

The project uses brain MRI images belonging to multiple diagnostic categories, including tumor classes and normal cases.

The workflow includes:

- Dataset exploration and class analysis
- Data preprocessing and augmentation
- Train, validation, and test splitting
- Transfer learning using pre-trained CNN architectures
- Comparison of multiple deep learning models
- Hyperparameter tuning
- Performance evaluation using classification metrics and confusion matrices
- External validation on a second MRI dataset

## Models

The following architectures were evaluated:

- EfficientNetB0
- EfficientNetB0 with additional regularization
- EfficientNetB5
- DenseNet121

A custom CNN architecture was also explored during the project.

Among the compared transfer-learning models, **EfficientNetB5 achieved the best performance on the internal test set, with approximately 93.3% accuracy**.

## External Validation

To further evaluate model generalization, the trained models were tested on a second brain MRI dataset.

This additional evaluation highlighted the effect of **domain shift**, showing that performance may decrease when models are applied to images with different characteristics, acquisition settings, or orientations from those used during training.

This step was included to assess model robustness beyond the original dataset.

## Technologies

- Python
- TensorFlow / Keras
- scikit-learn
- NumPy
- pandas
- Matplotlib
- Seaborn
- Plotly
- KaggleHub
- Keras Tuner
- Pillow

## Dataset

The primary dataset is downloaded automatically through KaggleHub:

**Brain Tumor MRI Images — 44 Classes**

The notebook downloads the dataset directly when executed, so the image dataset itself is not included in this repository.

## Repository Structure

```text
brain-tumor-classification-deep-learning/
│
├── notebooks/
│   └── brain_tumor_classification.ipynb
│
├── presentation/
│   └── deep_learning_project_presentation.pdf
│
├── models/
│   └── generated locally and excluded from GitHub
│
├── README.md
├── requirements.txt
└── .gitignore
```

## Installation

Clone the repository and move into the project folder:

```bash
git clone <repository-url>
cd brain-tumor-classification-deep-learning
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

Then open:

```text
notebooks/brain_tumor_classification.ipynb
```

in Jupyter Notebook or Visual Studio Code.

The dataset will be downloaded automatically when the corresponding notebook cell is executed.

## Model Files

Trained `.keras` model files are saved locally inside the `models/` directory.

Because trained deep learning models can be large, this directory is excluded from the GitHub repository through `.gitignore`.

Running the training sections of the notebook will recreate the models locally.

## Results

The project compares model performance using metrics such as:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrices

EfficientNetB5 produced the strongest overall performance on the original test set, reaching approximately **93.3% test accuracy**.

The external validation stage demonstrated that strong performance on an internal test set does not necessarily guarantee equivalent performance on data from a different source.

## Presentation

The `presentation/` directory contains the final project presentation summarizing the methodology, experiments, model comparison, and conclusions.

## Notes

Training all deep learning models and running hyperparameter tuning can require significant computational resources and execution time.
