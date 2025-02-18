# Builders-Bootcamp-HW2
Building an ETL Pipeline for Anomaly Detection
Copyright (C) 2025 Shaji R. Nathan/IP INFUSION INC.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License along with this program. If not, see https://www.gnu.org/licenses/.

Description: A comprehensive machine learning framework for anomaly detection in network data. This module implements a complete ML pipeline including:

- Data preprocessing and feature scaling
- Handling imbalanced datasets using SMOTE and other techniques
- Multiple classification algorithms (LogReg, SVM, Random Forest, Gradient Boosting)
- Model evaluation with various metrics (ROC-AUC, Precision-Recall, F1)
- Detailed visualization of results and model performance
- Feature importance analysis and interpretation
- Similar sample analysis for prediction explanation
- Model persistence and result export capabilities

The framework is designed to be easily extensible and configurable through
a flexible configuration system that allows customization of preprocessing
steps, model parameters, and evaluation metrics.

Author: Shaji R. Nathan CTO IP Infusion Inc. Email: snathanfax@gmail.com

Created: 2025-02-17 - Initial implementation of anomaly detection framework

Modified: 2025-02-17 - Added comprehensive visualization and analysis capabilities Added model persistence and export functionality Enhanced documentation and code organization
Version:

1.0.0 - First stable release with complete functionality
- Major (1): Initial release with complete feature set
- Minor (0): No feature additions after initial release
- Patch (0): No bug fixes yet

Dependencies: Core ML Libraries:

- scikit-learn>=1.0.0 : Main ML functionality
- imbalanced-learn>=0.8.0 : Handling imbalanced datasets

Data Processing:
- pandas>=1.3.0 : Data manipulation and analysis
- numpy>=1.20.0 : Numerical computations

Visualization:
- matplotlib>=3.4.0 : Basic plotting capabilities
- seaborn>=0.11.0 : Enhanced statistical visualizations

Utilities:
- joblib>=1.0.0 : Model persistence and parallel processing

Notes:

- The framework currently assumes input data is in CSV format with the last column
  containing binary labels (0 for normal, 1 for anomaly)
- All models are optimized for binary classification tasks
- Feature scaling is automatically applied based on model requirements
- Cross-validation is performed with stratified k-fold splitting
- Model selection is based on ROC-AUC score by default

Example Usage:

# Initialize detector
detector = AnomalyDetector()

# Load and prepare data
detector.load_data('network_data.csv')
detector.preprocess_data()

# Train and evaluate models
detector.train_models()
detector.evaluate_models()

# Select best model and make predictions
best_model = detector.select_best_model()
predictions = detector.predict(new_data)

For additional documentation and updates, please visit: https://github.com/snathanfax/anomaly-detection

Bug Reports and Feature Requests: Please submit issues and pull requests through the GitHub repository or contact the author directly at snathanfax@gmail.com
