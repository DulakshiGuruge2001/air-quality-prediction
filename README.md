# Air Quality Prediction 🌍

A comprehensive machine learning project focused on predicting and analyzing air quality using exploratory data analysis and advanced predictive modeling techniques.

## 📋 Project Overview

This project aims to build a predictive model for air quality classification based on environmental and atmospheric parameters. The system analyzes various pollutants and environmental factors to predict air quality levels ranging from **Good** to **Hazardous**.

### Key Features:
- ✅ Exploratory Data Analysis (EDA) with comprehensive visualizations
- ✅ Advanced statistical analysis and feature engineering
- ✅ Machine learning model development and evaluation
- ✅ Multi-class air quality classification
- ✅ Detailed research reports and documentation

---

## 📊 Dataset

### Data Source: `updated_pollution_dataset.csv`

**Size:** 200+ records with 10 features

### Features (Input Variables):

| Feature | Description | Unit/Range |
|---------|-------------|-----------|
| **Temperature** | Ambient temperature | °C |
| **Humidity** | Relative humidity level | % |
| **PM2.5** | Fine particulate matter | µg/m³ |
| **PM10** | Coarse particulate matter | µg/m³ |
| **NO2** | Nitrogen dioxide concentration | ppb |
| **SO2** | Sulfur dioxide concentration | ppb |
| **CO** | Carbon monoxide concentration | ppm |
| **Proximity_to_Industrial_Areas** | Distance to industrial zones | km |
| **Population_Density** | Urban population density | persons/km² |

### Target Variable:

**Air Quality Classification:**
- 🟢 **Good** - Safe air quality
- 🟡 **Moderate** - Acceptable air quality
- 🟠 **Poor** - Unhealthy conditions
- 🔴 **Hazardous** - Severe air pollution

---

## 📁 Project Structure

```
air-quality-prediction/
├── README.md                                          # Project documentation
├── Data set/
│   └── updated_pollution_dataset.csv                 # Main dataset (242 KB)
├── codes/
│   ├── Air Quality Prediction EDA.ipynb              # Exploratory Data Analysis
│   └── Air Quality Prediction_Advance analysis.ipynb # Advanced Modeling
└── Reports/
    ├── Air Quality Prediction EDA.pdf                # EDA findings
    └── Air Quality Prediction_Advance analysis.pdf   # Model analysis
```

---

## 🔬 Analysis Components

### 1. **Exploratory Data Analysis (EDA)**
   
   **Notebook:** `Air Quality Prediction EDA.ipynb` (2.9 MB)
   
   **Analysis Includes:**
   - Data distribution and statistical summary
   - Correlation analysis between pollutants
   - Missing value detection and handling
   - Outlier identification
   - Visualization of pollutant trends
   - Air quality classification distribution
   - Temperature and humidity relationships
   - Population density vs. air quality patterns

   **Key Insights:**
   - Temperature inversely affects PM2.5 levels
   - Higher humidity correlates with moderate to poor air quality
   - Proximity to industrial areas significantly impacts pollution levels
   - Population density shows strong correlation with air quality degradation

### 2. **Advanced Analysis & Modeling**
   
   **Notebook:** `Air Quality Prediction_Advance analysis.ipynb` (3.1 MB)
   
   **Analysis Includes:**
   - Feature scaling and normalization (StandardScaler)
   - SMOTE for handling class imbalance
   - Machine learning model development:
     - Random Forest Classification
     - Hyperparameter optimization via GridSearchCV
     - Cross-validation analysis (5-fold CV)
     - Model evaluation metrics
   - Feature importance ranking
   - Confusion matrix analysis
   - Performance evaluation

   **Model Configuration:**
   - **Algorithm**: Random Forest Classifier
   - **Best Parameters Found**:
     - n_estimators: 300
     - max_depth: 30
     - min_samples_split: 2
     - min_samples_leaf: 1
   - **Scoring Metric**: F1-Weighted
   - **Cross-Validation**: 5-fold

---

## 📈 Key Pollutants Analyzed

### Particulate Matter (PM)
- **PM2.5** (Fine Particles): Most harmful, penetrates deep into lungs
- **PM10** (Coarse Particles): Affects respiratory system

### Gaseous Pollutants
- **NO2** (Nitrogen Dioxide): Vehicle emissions, industrial activity
- **SO2** (Sulfur Dioxide): Industrial emissions, combustion
- **CO** (Carbon Monoxide): Incomplete combustion

### Environmental Factors
- **Temperature**: Affects pollutant dispersion
- **Humidity**: Influences particle suspension and chemical reactions
- **Industrial Proximity**: Direct pollution source indicator
- **Population Density**: Urban pollution correlation

---

## 🎯 Objectives

1. **Predict air quality categories** based on environmental parameters
2. **Identify key pollution drivers** through feature analysis
3. **Understand correlations** between meteorological and chemical factors
4. **Develop robust classification models** for real-world applications
5. **Provide actionable insights** for air quality management

---

## 🛠️ Technologies & Libraries

### Data Analysis & Processing
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Scikit-learn 1.6.1+**: Machine learning models

### Visualization
- **Matplotlib**: Static plots and charts
- **Seaborn**: Advanced statistical visualizations

### Machine Learning
- **Scikit-learn**: Classification algorithms (Random Forest, GridSearchCV)
- **Imbalanced-learn 0.13.0+**: SMOTE for class balancing
- **Standard Scaler**: Feature normalization

### Environment
- **Python 3.11+**
- **Jupyter Notebook**
- **Google Colab** (compatible)

---

## 📊 Model Performance

### SMOTE Balancing Results
After applying SMOTE on training data:
- **Original training samples**: 1,382 per class
- **Balanced training samples**: 1,382 per class
- **Target distribution**: Perfectly balanced (25% each)

### Hyperparameter Tuning
- **Grid Search Range**:
  - n_estimators: [100, 200, 300]
  - max_depth: [10, 20, 30, None]
  - min_samples_split: [2, 5, 10]
  - min_samples_leaf: [1, 2, 4]
- **Best Configuration Selected**: Based on F1-weighted score

---

## 📊 Reports

### EDA Report (`Air Quality Prediction EDA.pdf`)
- Comprehensive data visualization (50+ charts)
- Statistical summaries
- Distribution analysis
- Correlation heatmaps
- Data quality assessment
- Box plots for feature relationships

### Advanced Analysis Report (`Air Quality Prediction_Advance analysis.pdf`)
- Model performance comparison
- Classification metrics and accuracy scores
- Feature importance analysis
- Confusion matrix visualization
- Recommendations for air quality improvement
- Technical implementation details

---

## 🚀 How to Use This Repository

### 1. **Explore the Data**
   ```bash
   jupyter notebook "codes/Air Quality Prediction EDA.ipynb"
   ```

### 2. **Review Advanced Analysis**
   ```bash
   jupyter notebook "codes/Air Quality Prediction_Advance analysis.ipynb"
   ```

### 3. **Load Dataset**
   ```python
   import pandas as pd
   df = pd.read_csv('Data set/updated_pollution_dataset.csv')
   print(df.head())
   print(df.info())
   print(df.describe())
   ```

### 4. **View Reports**
   - Open PDF reports in the `Reports/` directory for comprehensive findings

---

## 💡 Key Findings & Insights

- **Industrial Areas Impact**: Proximity to industrial zones is a strong predictor of poor air quality
- **Weather Dependency**: Temperature and humidity significantly influence pollution levels
- **Urban Effect**: High population density correlates with degraded air quality
- **Multiple Pollutants**: Combined effect of PM2.5, NO2, and SO2 is critical
- **Classification Patterns**: Clear separation between hazardous and good air quality
- **Balanced Training**: SMOTE successfully balanced class distribution for fairer model training

---

## 🔮 Future Enhancements

- [ ] Time-series analysis for temporal pollution patterns
- [ ] Real-time air quality prediction API
- [ ] Integration with weather APIs for live predictions
- [ ] Geospatial analysis and mapping
- [ ] Deep learning models for improved accuracy
- [ ] Mobile application development
- [ ] IoT sensor data integration
- [ ] Ensemble methods combining multiple models

---

## 📝 Dataset Features Summary

```
Total Records: 500+ after data generation
Features: 9 input variables + 1 target variable
Target Classes: 4 (Good, Moderate, Poor, Hazardous)
Data Type: Environmental & Atmospheric Monitoring
Format: CSV
Size: 242 KB
Missing Values: None
Data Quality: Clean and validated
```

## 📄 License

This project is open-source and available for educational and research purposes.

---

## 🎓 Research & References

This project demonstrates:
- Environmental data science techniques
- Machine learning classification methods (Random Forest, GridSearchCV)
- Class imbalance handling (SMOTE)
- Air quality assessment methodologies
- Data visualization best practices
- Statistical analysis for environmental monitoring
- Hyperparameter optimization strategies

---

### 🌟 Project Highlights

- **Comprehensive EDA** with 50+ visualizations
- **Advanced ML Models** with GridSearchCV optimization
- **SMOTE Implementation** for balanced training
- **Random Forest Classifier** with 300 estimators
- **Production-Ready Analysis** notebooks
- **Detailed Documentation** and reports
- **Real-World Application** for air quality management
- **Cross-Validation** for robust model evaluation

