# Countries' Flags and Happiness: Exploring the Connection Between National Symbols and Well-being

> Sabancı University **DSA210** Introduction to Data Science Course Spring 2024-2025 Term Project.  
> Combining data science with social sciences to uncover insights hidden in national symbols.  

---

## Introduction  

This project explores whether national flags — through their colors, symbols, and patterns — may reflect deeper elements of a country, such as its **happiness, economy, and social support**.  

As someone interested in **social sciences and cultural studies**, I have always been fascinated by how symbols represent societies. Flags are important national symbols, but do they tell us something meaningful about a country's well-being? Through this project, I aim to investigate the **relationship between flag designs and real-world indicators like happiness scores and GDP**.  

In the updated version, I applied **machine learning models** to see whether flag features can predict happiness scores and selected specific test cases to evaluate prediction quality.

---

## Contents  
- [Motivation](#motivation)  
- [Data Sources](#data-sources)  
- [Data Merging Plan](#data-merging-plan)  
- [Data Analysis](#data-analysis)  
- [Machine Learning Model](#machine-learning-model)  
- [Challenges](#possible-challenges)  
- [Future Work](#future-work)  

---

## Motivation   

National flags are more than just beautiful pieces of cloth — they represent a country's identity, history, culture, and beliefs. As a person who has always been curious about **how culture connects to society's well-being**, I wanted to address this topic from a **data science perspective**.  

Some questions I am curious to explore:  
- Are countries with **blue flags** happier on average?  
- Do **religious symbols** in flags reflect differences in GDP or happiness?  
- Are there visible patterns in flag designs based on **geographic regions or economic status**?  

Although there are studies about the cultural and political meaning of flags, **there is little to no data-driven research** into how flag aspects link to social variables such as happiness. That makes this a **creative and original** project combining data science with social science.  

---

## Data Sources  

1. **World Flags Dataset**  
   - **Source**: [Kaggle - World Flags](https://www.kaggle.com/datasets/edoardoba/world-flags)  
   - **Description**: Contains features of flags from 193 countries, including:  
     - Colors (red, blue, green, etc.)  
     - Symbols: ✝️ (Cross), ☪ (Crescent), ⭐ (Star), ⚒️ (Hammer & Sickle), 🌆 (Sun-like), 🦅 (Eagle), 🐉 (Dragon)
     - Geographic info: landmass, zone, population, language, religion  

2. **World Happiness Report (2015)**  
   - **Source**: [Kaggle - World Happiness Report](https://www.kaggle.com/unsdsn/world-happiness)  
   - **Description**: Provides happiness scores and well-being metrics for 158 countries:  
     - Happiness score  
     - GDP per capita  
     - Social support  
     - Healthy life expectancy  
     - Freedom to make life choices  
     - Generosity, Corruption perception

---

## Data Merging Plan  

Steps:  
1. **Standardized country names** by stripping whitespaces and lowering case.  
2. **Merged datasets** based on country names.  
3. Selected countries with happiness score and valid flag feature data.  
4. Handled `;`-delimited flags.csv and cleaned column names for consistency.

---

## Data Analysis

### 1. Data Cleaning  
- Fixed mismatches between country names (e.g., "USA" vs "United States").
- Selected relevant features such as flag color/symbol counts and happiness score.
- Ensured proper encoding and handling of numeric/categorical features.

### 2. Exploratory Data Analysis (EDA)
- **Histogram of Happiness Scores**: Displayed normal-like distribution.
- **Top 15 Happiest Countries**: Visualized with horizontal bar chart.
- **Boxplot by Region**: Showed regional happiness variations.
- **Correlation Heatmap**: Explored inter-variable relations.
- **Freedom vs Happiness Scatterplot**: Showed clear positive correlation.

### Histogram of Happiness Scores
![Happiness Histogram](happiness_histogram.png)

### Top 15 Happiest Countries
![Top 15 Happiest Countries](top15_happiness.png)

### Correlation Heatmap
![Correlation Heatmap](correlation_heatmap.png)

### 3. Hypothesis Testing: Freedom vs Happiness
- **Null Hypothesis**: Freedom and Happiness are not correlated.
- **Alternative Hypothesis**: There is a positive correlation.
- **Test**: Pearson Correlation Coefficient
  - r = 0.6429
  - p < 0.0001
- **Conclusion**: Reject null. Freedom positively correlates with Happiness.

---

## Machine Learning Model

### Objective
To predict a country's happiness score based on flag features (colors and symbols).

### Hypothesis
> **"A country's flag design may contain patterns (colors/symbols) that relate to its happiness level."**

### Model Used
- **Random Forest Regressor** from scikit-learn
- 80/20 Train-Test Split
- Features used: red, green, blue, gold, white, black, orange, crosses, crescents, sunstars, icon presence, etc.

### Results
- **R² Score**: 0.076 (Low predictive power)
- **MSE**: 1.46
- This suggests that **flag designs alone are not strong predictors** of happiness.

### Sample Predictions
| Country   | Actual Happiness | Predicted | Error |
|-----------|------------------|-----------|-------|
| Greece    | 4.86             | 7.38      | 2.52  |
| Brazil    | 6.98             | 4.92      | 2.06  |
| Singapore | 6.80             | 5.01      | 1.79  |

---

## Possible Challenges  

| Challenge                              | Solution                                  |
|----------------------------------------|-------------------------------------------|
| Country name mismatches                | Normalization and manual corrections      |
| Dataset size differences               | Focused on common countries               |
| Flags contain categorical/symbol data  | Binary encoding used                      |
| Low correlation between flags and happiness | Highlighted in results and future work |

---

## Future Work  

- Add **Human Development Index** and **Democracy Index** to improve predictions
- Investigate deeper meaning of **flag color psychology**
- Analyze **flag changes over time** and link to historical happiness shifts
- Explore **regional case studies** with cultural/political backgrounds
- Use **textual/visual analysis** of flag images for more nuanced features

---

Thanks for reading this interdisciplinary exploration!  
A creative blend of data science, symbolism, and social indicators ✨
