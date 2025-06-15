# Detection-of-Depression-Using-Late-Fusion-of-Sequential-Actigraphy-Features
Analyzed time-series data (Depressjon) to detect depression from patient activity recorded via clinical actigraphy watches. Utilized features such as time domain, statistical metrics, and LSTM-extracted attributes.

Done under the supervision of Dr. Anshika Arora & Ankur Maurya (Assistant Professors at Bennett University)

## Dataset :
https://datasets.simula.no/depresjon/

## Paper Pubished :
https://doi.org/10.1016/B978-0-443-32862-6.00009-2

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Feature Extraction & Classification Pipeline</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 40px;
      max-width: 900px;
    }
    h1, h2, h3 {
      color: #333;
    }
    code, pre {
      background-color: #f4f4f4;
      padding: 10px;
      display: block;
      white-space: pre-wrap;
      word-wrap: break-word;
    }
    ul {
      margin-top: 0;
    }
  </style>
</head>
<body>

  <h1>🧠 Feature Extraction & Classification Pipeline</h1>

  <p>This project presents a complete workflow for extracting meaningful features from time-series data and using machine learning models to classify them. It includes both statistical/time-domain and LSTM-derived features, feature fusion, and model evaluation.</p>

  <hr>

  <h2>📌 Features Extracted</h2>

  <h3>1. Day-wise Statistical & Time-Domain Features</h3>
  <ul>
    <li>Extracts core time-based features for each day (mean, std, skewness, etc.)</li>
  </ul>

  <h3>2. LSTM-based Features</h3>
  <ul>
    <li>Sequence modeling using LSTM to generate high-level deep features</li>
  </ul>

  <h3>3. Late Feature Fusion</h3>
  <ul>
    <li>Combines traditional statistical features and LSTM features at a later stage</li>
  </ul>

  <h3>4. Single-Day Features</h3>
  <ul>
    <li>Experiments with features derived from only one day’s data for baseline comparison</li>
  </ul>

  <hr>

  <h2>🧪 Final Task: Model Training & Evaluation</h2>

  <p>The extracted features are used to train and compare the following classifiers:</p>

  <ul>
    <li><strong>On Statistical + Time-Domain Features (TDF):</strong>
      <ul>
        <li>Random Forest</li>
        <li>AdaBoost</li>
        <li>SVM</li>
      </ul>
    </li>
    <li><strong>On LSTM Features:</strong>
      <ul>
        <li>Random Forest</li>
        <li>AdaBoost</li>
      </ul>
    </li>
    <li><strong>Late Fusion Model:</strong>
      <ul>
        <li>Combines predictions or features from both above sets</li>
      </ul>
    </li>
  </ul>

  <p>All models are evaluated and compared for accuracy, robustness, and consistency.</p>

  <hr>

  <h2>🔁 Workflow Overview</h2>

  <pre>
Data Preprocessing
      ↓
Normalization (reduce bias)
      ↓
Feature Extraction (Statistical + LSTM)
      ↓
Feature Normalization
      ↓
Feature Fusion
      ↓
Dimensionality Reduction
      ↓
Feature Selection
      ↓
Classification (RF, AdaBoost, SVM)
  </pre>

  <ul>
    <li><strong>Cross-validation:</strong> Stratified K-Fold</li>
    <li><strong>Hyperparameter Tuning:</strong> Grid Search</li>
  </ul>

  <hr>

  <h2>📂 Project Structure</h2>

  <pre>
├── data/                # Input data
├── src/                 # Source code
│   ├── visualization/   # Data and result visualizations
│   ├── features/        # Feature extraction scripts
│   ├── models/          # Model training and evaluation
│   └── utils/           # Helper functions
├── results/             # Accuracy curves and evaluation outputs
├── README.md            # Project documentation
  </pre>

  <hr>

  <h2>📄 Code Modules (Documentation)</h2>

  <ol>
    <li><strong>Visualization</strong> – Raw data, feature distributions, model performance</li>
    <li><strong>Feature Extraction</strong> – Statistical and LSTM feature generation</li>
    <li><strong>Model Creation</strong> – Training, validation, tuning scripts</li>
    <li><strong>Accuracy Curves</strong> – Plots showing model performance</li>
  </ol>

  <hr>

  <h2>📊 Model Comparison</h2>

  <p>This project includes a thorough comparison of:</p>
  <ul>
    <li>Individual feature sets</li>
    <li>Combined feature sets</li>
    <li>Different classification models</li>
  </ul>

  <p>Helps assess how different features and fusion strategies impact performance.</p>

  <hr>

  <h2>🚀 Future Improvements</h2>

  <ul>
    <li>Add attention mechanism to LSTM for temporal focus</li>
    <li>Explore other fusion techniques (e.g., early fusion, attention-based)</li>
    <li>Use feature importance from models for feature selection</li>
  </ul>

</body>
</html>


