# Clay Classification Machine Learning Script

This repository contains a clean functional Python script converted from the original notebook-style clay classification workflow.

## Goal

Classify different clay types using experimental physicochemical properties such as particle size distribution, water absorption, oxide composition, impurities, and heat-release-related variables.

## Main models

- Decision Tree
- Random Forest
- Support Vector Machine, SVM

## Validation

The script uses Leave-One-Out Cross-Validation, LOOCV, which is suitable for very small datasets.

## Folder structure

```text
clay_ml_script_project/
├── data/
│   └── Clay classification.csv        # place your dataset here
├── output/
│   ├── figures/                       # generated plots
│   └── results/                       # generated text results
├── src/
│   └── clay_classification.py         # main functional Python script
├── README.md
└── requirements.txt
```

## How to run

Place your CSV file inside the `data/` folder and run:

```bash
python src/clay_classification.py --data "data/Clay classification.csv" --target Output
```

If your target column has a different name, change `Output`:

```bash
python src/clay_classification.py --data "data/your_file.csv" --target clay_type
```

## Outputs generated

### Results folder

```text
output/results/
├── dataset_summary.txt
├── model_evaluation_report.txt
├── feature_importance.txt
├── robustness_results.txt
└── new_sample_prediction.txt
```

### Figures folder

```text
output/figures/
├── class_distribution.png
├── correlation_heatmap.png
├── pca_plot.png
├── confusion_matrix_decision_tree.png
├── confusion_matrix_random_forest.png
├── confusion_matrix_svm.png
├── accuracy_comparison.png
├── actual_vs_predicted.png
├── feature_importance_decision_tree.png
├── feature_importance_random_forest.png
└── robustness_accuracy.png
```

## Notes

- The code is written using a functional programming style, meaning the workflow is separated into functions such as `load_data()`, `clean_data()`, `define_models()`, `evaluate_models_loocv()`, and `run_pipeline()`.
- Random seeds are fixed for reproducibility.
- SHAP was removed from the main script to keep the submission simple and easy to run. If required, SHAP can be added later as an optional interpretation module.
- The new-sample prediction will only run if the example feature names match the dataset column names.
