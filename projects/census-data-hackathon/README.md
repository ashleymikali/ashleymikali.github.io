# Census Income Prediction Hackathon

Predictive modeling using U.S. Census data to classify individuals by income threshold (>$50k vs ≤$50k annual income).

🏆 **3rd Place Finish** | 86.6% Classification Accuracy

📊 **[View Full Analysis](https://ashleymikali.com/projects/census-data-hackathon/ar_hackathon.html)**

## Project Overview

This project analyzes demographic and employment data from the U.S. Census to build classification models that predict whether an individual earns more than $50,000 annually. The analysis explores which demographic and socioeconomic factors are most strongly associated with higher income levels.

### Dataset
- **Size:** ~30,000+ records
- **Source:** U.S. Census data
- **Features:** Age, education, occupation, work class, marital status, race, sex, hours worked, and more
- **Target:** Binary classification (income >$50k or ≤$50k)

## Methodology

### Data Preparation
- Handled missing values and inconsistent categorical encodings
- Feature engineering and encoding for categorical variables
- Validation of data quality and completeness
- Train/test split for model evaluation

### Modeling Approaches
1. **Logistic Regression** - Baseline interpretable model
2. **XGBoost (Gradient Boosted Trees)** - Final competition model

### Model Development
- Cross-validation for hyperparameter tuning
- Feature selection to reduce overfitting
- Performance evaluation using accuracy, precision, and recall
- Model interpretability analysis

## Results

**Final Model Performance:**
- **Accuracy:** 86.6%
- **Competition Ranking:** 3rd place overall
- **Key Predictive Features:** Education level, occupation, age, hours worked per week

The analysis revealed that education and occupation type were the strongest predictors of income level, followed by age and weekly work hours.

## Technical Stack

- **Language:** R
- **Frameworks:** tidymodels, XGBoost
- **Visualization:** ggplot2
- **Documentation:** Quarto

## Repository Structure

```
census-data-hackathon/
├── ar_hackathon.qmd          # Main analysis document (Quarto)
├── ar_hackathon.html          # Rendered analysis
├── census_train.csv           # Training dataset
├── census_test.csv            # Test dataset
├── my_predictions.csv         # Final model predictions
└── README.md                  # This file
```

## Key Takeaways

- **Education matters:** Individuals with higher education levels showed significantly higher probability of earning >$50k
- **Occupation clusters:** Certain occupational categories (professional, managerial) strongly predicted higher income
- **Model tradeoffs:** XGBoost provided better predictive accuracy than logistic regression while maintaining reasonable interpretability
- **Data quality:** Careful handling of missing values and categorical encodings was essential for model performance

## Running the Analysis

To reproduce this analysis:

1. Install required R packages:
```r
install.packages(c("tidyverse", "tidymodels", "xgboost"))
```

2. Open the R project:
```r
# Open hack-a-thon.Rproj in RStudio
```

3. Render the analysis:
```bash
quarto render ar_hackathon.qmd
```

## Future Improvements

- Explore additional feature engineering (interaction terms, polynomial features)
- Implement ensemble methods combining multiple model types
- Conduct deeper analysis of model fairness across demographic groups
- Add SHAP values for improved feature importance interpretation

## Contact

- Email: ashkalirussell@gmail.com
- Portfolio: [ashleymikali.com](https://ashleymikali.com)
- GitHub: [@ashleymikali](https://github.com/ashleymikali)

## License

This project is open source for educational and portfolio purposes.
