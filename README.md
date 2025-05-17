# Hyphotesis-Energy-Consumption
This project analyzed the Energy Consumption Dataset using statistical tests to evaluate variable distributions and relationships, as well as differences based on household features such as occupancy, building area, average temperature, and electronic appliances.

# 📊 Hypothesis Testing of Energy Consumption Dataset

This project aims to explore and analyze the energy consumption dataset using descriptive, comparative, and associative statistical methods. The analysis is conducted to understand distribution patterns, relationships between variables, and statistical significance based on parameters such as temperature, building size, number of occupants, and number of electronic devices.

# 📦  Dataset

The dataset used for this project was downloaded from Kaggle: 

**Dataset:** govindaramsriram/energy-consumption-dataset-linear-regression

**Main file:** train_energy_data.csv

# 🛠️ Libraries Used

- **pandas, numpy:** For data manipulation
- **matplotlib, seaborn:** For data visualization
- **scipy.stats, statsmodels:** For statistical tests
- **sklearn:** For preprocessing and models (optional)
- **Kaggle CLI:** For downloading live datasets

# 📈 Initial Exploration
## Histogram Visualization

We display the distribution of variables such as:

- **Square Footage:** Multimodal distribution
- **Number of Occupants:** Multimodal distribution
- **Appliances Used:** Bimodal distribution
- **Average Temperature:** Almost uniform distribution
- **Energy Consumption:** Right-skewed distribution

## Normality Test (Kolmogorov-Smirnov Test)

Most variables are not normally distributed; therefore, non-parametric tests like the Wilcoxon and Mann-Whitney tests are utilized.

# 🔍 Hypothesis Testing

1. **Descriptive: Wilcoxon Test**
   - **Null Hypothesis (H0):** Average Energy Consumption = 1.0
   - **Result:** P-value ≈ 0.000 → Reject H0 → Energy consumption is not equal to 1.0.

2. **Comparative: Mann-Whitney U Test**
   - **Independent Variable Significance Test Result (α = 0.05):**
     - Average Temperature: P-value = 0.8749 → Failed to Reject H0 ❌ (Not significant)
     - Square Footage: P-value = 0.0000 → Reject H0 ✅ (Significant)
     - Number of Occupants: P-value = 0.0000 → Reject H0 ✅ (Significant)
     - Appliances Used: P-value = 0.0000 → Reject H0 ✅ (Significant)

   The variables Square Footage, Number of Occupants, and Appliances Used have a significant effect on energy consumption.

3. **Associative: Spearman Correlation**
   - **Null Hypothesis (H0):** There is no correlation between Average Temperature and Energy Consumption.
   - **Result:** (e.g.) Spearman ρ ≈ 0.05, P-value > 0.05 → Failure to Reject H0 → Weak or insignificant correlation.

# 📊 Additional Visualizations

- **Histogram + KDE Curve:** To visualize the shape of the distribution.
- **Probability Plot (Q-Q Plot):** To check whether the distribution conforms to normality.
- **Boxplot & Grouped Analysis:** To compare distributions between different groups.

# 📌 Conclusion

Energy consumption is not normally distributed, necessitating the use of non-parametric methods. The variables Square Footage, Number of Occupants, and Appliances Used show a significant influence on energy consumption, while Average Temperature does not significantly affect energy consumption in this context.

This project emphasizes the importance of validating assumptions before selecting a statistical analysis method.

# 🧠 Additional Notes

This analysis is suitable for exploratory data analysis and training in inferential statistics. It can be extended to multivariate regression modeling or advanced feature engineering.

# 🧪 How to Run

To download the datasets and run the analysis in a Jupyter Notebook or Python script, use the following commands:

```bash
# Download datasets
!kaggle datasets download -d govindaramsriram/energy-consumption-dataset-linear-regression
!unzip energy-consumption-dataset-linear-regression.zip
```
