# Code-Smell-Prediction
# AI Code Smell Detection System

> An intelligent machine learning project for detecting software code smells from engineering metrics through a modern Streamlit dashboard.

## Project Overview

The **AI Code Smell Detection System** is a machine learning-based application that predicts the type of software code smell using software quality metrics. It combines a trained ML model with an interactive **Streamlit** frontend, allowing users to enter code-related measurements and instantly receive predictions about potential maintainability and quality issues.

This project is designed as a practical AI-powered software engineering tool and is suitable for academic work, portfolio presentation, and code quality experimentation.

## Features

- Predicts **code smell type** using a trained machine learning model
- Interactive **Streamlit** web interface
- Futuristic **dark-themed dashboard UI**
- Accepts user input for important software metrics
- Displays prediction outcomes in real time
- Clean and structured Python implementation
- Suitable for demonstration, portfolio, and research use

## System Architecture

```text
+---------------------------+
| User Inputs Code Metrics  |
+------------+--------------+
             |
             v
+---------------------------+
| Streamlit Frontend (UI)   |
| - Sliders / Inputs        |
| - Dashboard Visualization |
+------------+--------------+
             |
             v
+---------------------------+
| Data Preparation Layer    |
| - Convert inputs to DataFrame
| - Format feature values   |
+------------+--------------+
             |
             v
+---------------------------+
| Trained ML Model          |
| - Extra Trees / RF based  |
| - Predict code smell type |
+------------+--------------+
             |
             v
+---------------------------+
| Prediction Result Display |
+---------------------------+
```

## Machine Learning Model

The system uses a trained machine learning model saved as a `.joblib` file:

```text
code_smell_model.joblib
```

The model is built for **classification**, where the target output is the predicted **code smell type** based on the following software metrics:

- `lines_of_code`
- `cyclomatic_complexity`
- `num_methods`
- `num_classes`
- `maintainability_index`
- `bug_prone_score`
- `technical_debt_minutes`
- `developer_experience_years`

Modeling approaches referenced in this project include:

- **Extra Trees**
- **Random Forest**

These ensemble methods are well-suited for structured tabular data and help capture complex relationships between software quality indicators and code smell categories.

## Dataset Information

**Dataset Name:** Code Smells and Refactoring Dataset  
**Dataset Size:** 120K samples

This dataset contains software metric records and associated code smell labels, enabling supervised machine learning for code quality prediction. It supports training models to identify patterns linked to common maintainability issues in software systems.

## Installation Instructions

### 1. Clone the repository

```bash
git clone https://github.com/your-username/ai-code-smell-detection-system.git
cd ai-code-smell-detection-system
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install streamlit pandas numpy scikit-learn joblib
```

## How to Run the Application

Make sure the trained model file is available in the project root:

```text
code_smell_model.joblib
```

Then start the Streamlit application:

```bash
streamlit run app.py
```

After launching, open the local URL shown in the terminal, usually:

```text
http://localhost:8501
```

## Project Structure

```text
AI Code Smell Detection System/
│
├── app.py
├── code_smell_model.joblib
├── README.md
├── .venv/
└── __pycache__/
```

### File Descriptions

- `app.py` - Streamlit application with the dashboard UI and prediction logic
- `code_smell_model.joblib` - Trained machine learning model used for inference
- `README.md` - Project documentation

## Example Usage

1. Run the Streamlit app.
2. Enter software metrics such as lines of code, complexity, and maintainability score.
3. Click **Predict Code Smell**.
4. View the predicted code smell type and quality feedback in the dashboard.

Example input:

```text
lines_of_code = 350
cyclomatic_complexity = 18
num_methods = 10
num_classes = 4
maintainability_index = 58.2
bug_prone_score = 0.47
technical_debt_minutes = 120
developer_experience_years = 3.5
```

Example outcome:

```text
Predicted code smell type: Long Method
```

## Future Improvements

- Add support for batch prediction using CSV uploads
- Visualize metric importance and model confidence
- Improve model explainability with SHAP or feature importance charts
- Add authentication and project history tracking
- Deploy the application to Streamlit Community Cloud or Azure
- Integrate static code analysis tools for automated metric extraction

## Author

**Dinol Siriwardena**  
AI / Machine Learning Project Developer

---

## Tech Stack Summary

`Python` `Streamlit` `Scikit-learn` `Pandas` `NumPy` `Joblib` `Machine Learning` `VS Code`

---

## Portfolio Note

This project demonstrates:

- Applied machine learning for software engineering
- Interactive dashboard development with Streamlit
- End-to-end model integration in a user-facing application
- Practical use of software quality metrics for intelligent prediction

If you are using this project for a portfolio, research showcase, or academic submission, this README is structured to present both the technical implementation and the user-facing value clearly.
