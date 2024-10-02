# Insurance Risk Analysis Project

## Overview
This project implements a machine learning model for predicting insurance risk categories using both Python and R. It demonstrates the application of data science techniques in the insurance industry, specifically for risk assessment and classification.

## Features
- Data preprocessing and feature engineering
- Machine learning model implementation using Random Forest
- Comprehensive visualizations using R
- Risk prediction functionality for new cases
- Model performance evaluation

## Technologies Used
- Python 3.x
  - pandas
  - numpy
  - scikit-learn
- R
  - tidyverse
  - ggplot2
  - gridExtra

## Dataset
The analysis uses the Medical Cost Personal Insurance dataset from Kaggle, which includes the following features:
- Age
- Sex
- BMI
- Number of children
- Smoking status
- Residential region
- Insurance charges

## Model Performance
- Accuracy: 93%
- Precision: 94% (High Risk category)
- Recall: 77% (High Risk category)

## Key Findings
1. Smoking status is the most significant predictor of insurance risk
2. Age and BMI show strong correlations with risk levels
3. The model successfully identifies high-risk cases with high precision

## Project Structure
```
insurance-risk-analysis/
├── data/
│   └── insurance.csv
├── python/
│   └── insurance_model.py
├── R/
│   └── visualizations.R
├── output/
│   ├── risk_distribution.png
│   ├── feature_importance.png
│   ├── risk_factors.png
│   └── bmi_age_risk.png
└── README.md
```

## How to Run
1. Clone the repository:
```bash
git clone https://github.com/yourusername/insurance-risk-analysis.git
```

2. Install required Python packages:
```bash
pip install pandas numpy scikit-learn
```

3. Install required R packages:
```R
install.packages(c("tidyverse", "ggplot2", "scales", "gridExtra"))
```

4. Run the Python script:
```bash
python insurance_model.py
```

5. Run the R script:
```R
Rscript visualizations.R
```

## Example Usage
```python
from insurance_model import predict_risk

risk_prediction, risk_probability = predict_risk(
    age=35, sex='male', bmi=28.5, 
    children=2, smoker='yes', region='southwest'
)

print(f"Risk Category: {'High' if risk_prediction else 'Low'}")
print(f"Probability of High Risk: {risk_probability:.2f}")
```

## Visualizations
The project generates several visualizations:
1. Distribution of insurance charges by risk category
2. Feature importance ranking
3. Risk distribution by age group and smoking status
4. BMI vs Age plot with risk categorization

## Future Improvements
- Implement cross-validation for more robust model evaluation
- Explore other machine learning algorithms
- Add more feature engineering techniques
- Develop a web interface for risk prediction

## Contributing
Feel free to fork the project and submit pull requests. For major changes, please open an issue first to discuss the proposed change.

## Author
Parvej Akhter
- GitHub: [parvej8461](https://github.com/parvej8461)

## Acknowledgments
- Dataset source: [Medical Cost Personal Insurance Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- Inspired by real-world applications in the insurance industry
