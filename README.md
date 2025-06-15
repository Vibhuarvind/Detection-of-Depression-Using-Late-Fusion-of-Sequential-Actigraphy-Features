<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Detection of Depression Using Late Fusion of Sequential Actigraphy Features</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 40px;
      max-width: 900px;
      color: #333;
    }
    h1, h2, h3 {
      color: #2c3e50;
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
    a {
      color: #2980b9;
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>

  <h1>🧠 Detection of Depression Using Late Fusion of Sequential Actigraphy Features</h1>

  <p>This project analyzes time-series data from the <strong>Depresjon dataset</strong> to detect signs of depression based on patients' physical activity recorded via clinical actigraphy watches.</p>

  <p>We employ a combination of traditional time-domain and statistical features with deep learning-based LSTM features, using late fusion strategies to improve classification accuracy.</p>

  <p><strong>Supervised by:</strong> Dr. Anshika Arora & Mr. Ankur Maurya (Assistant Professors, Bennett University)</p>

  <h2>📁 Dataset</h2>
  <p>Publicly available at: 
    <a href="https://datasets.simula.no/depresjon/" target="_blank">https://datasets.simula.no/depresjon/</a>
  </p>

  <h2>📄 Published Paper</h2>
  <p>Read the publication at: 
    <a href="https://doi.org/10.1016/B978-0-443-32862-6.00009-2" target="_blank">
      https://doi.org/10.1016/B978-0-443-32862-6.00009-2
    </a>
  </p>

  <hr>

  <h2>📌 Features Extracted</h2>

  <h3>1. Day-wise Statistical & Time-Domain Features</h3>
  <ul>
    <li>Mean, standard deviation, min/max values, skewness, etc.</li>
  </ul>

  <h3>2. LSTM-based Sequential Features</h3>
  <ul>
    <li>Learned representations using LSTM layers to capture temporal dependencies</li>
  </ul>

  <h3>3. Late Feature Fusion</h3>
  <ul>
    <li>Combines statistical and LSTM-based features during or after model training</li>
  </ul>

  <h3>4. Single-Day Feature Baseline</h3>
  <ul>
    <li>Baseline analysis using features from a single day of activity</li>
  </ul>

  <hr>

  <h2>🧪 Final Task: Classification & Evaluation</h2>

  <p>Various classifiers were trained and evaluated:</p>

  <ul>
    <li><strong>Using Time-Domain + Statistical Features:</strong>
      <ul>
        <li>Random Forest</li>
        <li>AdaBoost</li>
        <li>Support Vector Machine (SVM)</li>
      </ul>
    </li>
    <li><strong>Using LSTM Features:</strong>
      <ul>
        <li>Random Forest</li>
        <li>AdaBoost</li>
      </ul>
    </li>
    <li><strong>Late Fusion Model:</strong>
      <ul>
        <li>Combined classification using both feature sets</li>
      </ul>
    </li>
  </ul>

  <p>Performance is compared across models to assess effectiveness of different feature types and fusion strategies.</p>

  <hr>

  <h2>🔁 Workflow Pipeline</h2>

  <pre>
1. Data Preprocessing
2. Normalization (to reduce bias)
3. Feature Extraction (Statistical + LSTM)
4. Feature Normalization
5. Feature Fusion (late-stage)
6. Dimensionality Reduction
7. Feature Selection
8. Classification (RF, AdaBoost, SVM)
  </pre>

  <ul>
    <li><strong>Cross-Validation:</strong> Stratified K-Fold</li>
    <li><strong>Hyperparameter Tuning:</strong> Grid Search for robust model parameters</li>
  </ul>

  <hr>

  <h2>📂 Project Structure</h2>

  <pre>
├── data/                # Raw and processed data
├── src/                 # Source code
│   ├── visualization/   # Data and result visualizations
│   ├── features/        # Feature extraction scripts
│   ├── models/          # Model training and evaluation
│   └── utils/           # Helper functions
├── results/             # Accuracy curves and evaluation metrics
├── README.md            # Project documentation
  </pre>

  <hr>

  <h2>📄 Code Modules</h2>

  <ol>
    <li><strong>Visualization</strong> – Activity data plots and model accuracy curves</li>
    <li><strong>Feature Extraction</strong> – Scripts for extracting time-domain and LSTM-based features</li>
    <li><strong>Model Creation</strong> – ML models with tuning and training logic</li>
    <li><strong>Accuracy Curves</strong> – Performance comparison graphs</li>
  </ol>

  <hr>

  <h2>📊 Model Comparison</h2>

  <p>Extensive comparison across:</p>
  <ul>
    <li>Traditional vs LSTM features</li>
    <li>Late-fused models vs individual models</li>
    <li>Impact of single-day vs full-window features</li>
  </ul>

  <p>The goal is to determine the most robust approach to detecting depressive symptoms via wearable data.</p>

  <hr>

  <h2>🚀 Future Enhancements</h2>

  <ul>
    <li>Incorporate attention mechanism in LSTM</li>
    <li>Test early or hybrid fusion approaches</li>
    <li>Explore ensemble models with weighted fusion strategies</li>
    <li>Integrate feature importance rankings for selection</li>
  </ul>

</body>
</html>
