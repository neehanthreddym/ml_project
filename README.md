# Student Performance Prediction

## Overview
This project is an end-to-end Machine Learning application designed to predict student performance (specifically math scores) based on various demographic and socio-economic factors. The solution implements a robust pipeline for data ingestion, transformation, and model training, served via a Flask web application and ready for deployment on AWS Elastic Beanstalk.

## 🌟 Features
*   **End-to-End Pipeline**: Modularized components for data ingestion, transformation, and model training.
*   **Web Interface**: User-friendly web application built with Flask for making real-time predictions.
*   **Model Performance**: Utilizes advanced ensemble methods (CatBoost, XGBoost, etc.) to achieve high accuracy.
*   **Reproducibility**: Modular code structure ensuring easy replication of results.
*   **Deployment Ready**: Configured for deployment on AWS Elastic Beanstalk.

## 🛠️ Tech Stack
*   **Language**: Python 3.8+
*   **Framework**: Flask
*   **Libraries**: Pandas, NumPy, Scikit-learn, CatBoost, Dill
*   **Deployment**: AWS Elastic Beanstalk

## 📂 Project Structure
The project is organized as follows:
```
ml_project/
├── .ebextensions/       # AWS Elastic Beanstalk configuration
├── artifacts/           # Stores generated datasets and models
├── notebooks/           # Jupyter notebooks for EDA and experimentation
├── src/
│   ├── components/      # Core ML components
│   │   ├── data_ingestion.py      # Handles data reading and splitting
│   │   ├── data_transformation.py # Handles preprocessing and feature engineering
│   │   └── model_trainer.py       # Handles model training and evaluation
│   ├── pipeline/        # Pipeline orchestrators
│   │   └── predict_pipeline.py    # Pipeline for making predictions
│   ├── utils.py         # Utility functions
│   ├── logger.py        # Logging configuration
│   └── exception.py     # Custom exception handling
├── application.py       # Flask application entry point
├── requirements.txt     # Python dependencies
└── setup.py             # Package setup
```

## 🚀 Installation

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/neehanthreddym/ml_project.git
    cd ml_project
    ```

2.  **Create a virtual environment** (recommended):
    ```bash
    python -m venv .venv
    source .venv/bin/activate  # On Windows: .venv\Scripts\activate
    ```

3.  **Install dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

## 💻 Usage

### Running the Web Application
To start the Flask application and use the web interface:
```bash
python application.py
```
Open your browser and navigate to `http://127.0.0.1:5000`.

### Training the Model
To run the complete data ingestion, transformation, and training pipeline:
```bash
python src/components/data_ingestion.py
```
This will:
1.  Ingest data from `notebooks/data/`.
2.  Preprocess the data and save artifacts.
3.  Train the model and save the best performing model to `artifacts/model.pkl`.

## 📊 Dataset
The dataset includes the following features:
*   Gender
*   Race/Ethnicity
*   Parental Level of Education
*   Lunch Type
*   Test Preparation Course
*   Math, Reading, and Writing Scores

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License
This project is open source and available under the [MIT License](LICENSE).
