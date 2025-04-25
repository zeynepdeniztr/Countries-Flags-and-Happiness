# Countries' Flags and Happiness: Exploring the Connection Between National Symbols and Well-being  

> Sabancı University **DSA210** Introduction to Data Science Course Spring 2024-2025 Term Project.  
> Combining data science with social sciences to uncover insights hidden in national symbols.  



## Introduction  

This project explores whether national flags — through their colors, symbols, and patterns — may reflect deeper elements of a country, such as its **happiness, economy, and social support**.  

As someone interested in **social sciences and cultural studies**, I have always been fascinated by how symbols represent societies. Flags are important national symbols, but do they tell us something meaningful about a country's well-being? Through this project, I aim to investigate the **relationship between flag designs and real-world indicators like happiness scores and GDP**.  

---

## Contents  
- [Motivation](#motivation)  
- [Data Sources](#data-sources)  
- [Data Merging Plan](#data-merging-plan)  
- [Possible Challenges](#possible-challenges)  
- [Future Work](#future-work)  

---

## Motivation   

National flags are more than just beautiful pieces of cloth — they represent a country's identity, history, culture, and beliefs. As a person who has always been curious about **how culture connects to society's well-being**, I wanted to address this topic from a **data science perspective**.  

Some questions I am curious to explore:  
- Are countries with **blue flags** happier on average?  
- Do **religious symbols** in flags reflect differences in GDP or happiness?  
- Are there visible patterns in flag designs based on **geographic regions or economic status**?  

Flags often feature powerful symbols such as ✝️ (cross), ☪️ (crescent), ⭐ (star), ⚒️ (hammer & sickle), which might reflect a country's identity and possibly correlate with happiness and well-being.  

Although there are studies about the cultural and political meaning of flags, **there is little to no data-driven research** into how flag aspects link to social variables such as happiness. That makes this a **creative and original** project combining data science with social science.  
 

---

## Data Sources  

1. **World Flags Dataset**  
   - **Source**: [Kaggle - World Flags](https://www.kaggle.com/datasets/edoardoba/world-flags)  
   - **Description**: Contains features of flags from 193 countries, including:  
     - Colors (red, blue, green, etc.)  
     - Symbols: ✝️ (Cross), ☪️ (Crescent), ⭐ (Star), ⚒️ (Hammer & Sickle), 🔆 (Sun-like), 🦅 (Eagle), 🐉 (Dragon) ...
     - Geographic information (landmass, zone)  
     - Population, language, religion  

2. **World Happiness Report 2019**  
   - **Source**: [Kaggle - World Happiness Report](https://www.kaggle.com/unsdsn/world-happiness)  
   - **Description**: Contains happiness scores and detailed well-being indicators for 156 countries, such as:  
     - Happiness score  
     - GDP per capita  
     - Social support  
     - Healthy life expectancy  
     - Freedom to make life choices  
     - Generosity  
     - Perceptions of corruption  

---

## Data Merging Plan  

- Since the two datasets have different country lists (193 vs. 156), I will focus on **the common countries that appear in both datasets**.  
-Since the country names do not match exactly between datasets (e.g., 'UK' vs. 'United Kingdom'), I plan to handle this issue using manual mapping and fuzzy matching techniques to ensure proper alignment for analysis.

Steps:  
1. **Standardize country names** to match them correctly.  
2. **Merge the datasets** on country names.  
3. Handle missing data if necessary.  

---

## Data Analysis  

### 1. **Data Cleaning**  
- Fix country name mismatches between datasets.  
- Select relevant features (flag colors, symbols, happiness score, GDP, etc.).  
- Handle missing values and merge datasets into one.  

### 2. **Exploratory Data Analysis (EDA)**  
- Explore distributions of flag features — colors, symbols, patterns.  
- Analyze how often symbols like ✝️, ☪️, ⭐, ⚒️ appear and how they relate to happiness and GDP.  
- Compare flag designs across continents, regions, and income levels.  

### 3. **Correlation Analysis**  
- Investigate if certain flag elements (colors, symbols) are linked to higher happiness or GDP.  
- Examine connections between geographic features (landmass, zone) and happiness.  

### 4. **Visualization**  
- Create visualizations to show key patterns and relationships.  
- Use bar charts, heatmaps, scatter plots.  
- Example visuals:  
  - Happiness scores by flag colors.  
  - GDP comparisons for flags with vs. without religious symbols.  

---

## Possible Challenges  

| Challenge                                  | Solution                                                      |
|--------------------------------------------|---------------------------------------------------------------|
| **Country name mismatches**                 | Manual adjustments and fuzzy matching if needed.              |
| **Missing data in happiness scores**       | Imputation (filling gaps) or excluding some countries.         |
| **Encoding flag features for analysis**    | Using binary or one-hot encoding for categorical flag data.   |
| **Finding meaningful correlations**        | Focus on both data-driven results and social science context. |

---

## Future Work  

- **Add more datasets**: Including data like the Democracy Index or Human Development Index could give a broader perspective on how national symbols relate to well-being.  
- **Focus on specific regions**: Narrowing down the research to specific groups of countries (e.g., post-colonial states or Nordic countries) may reveal deeper cultural patterns.  
- **Analyze historical flag changes**: Looking at how flag designs have evolved over time could show connections between national identity shifts and happiness.  
- **Support findings with academic research**: Bringing in studies from political science and cultural studies would help interpret the meaning of flag elements in relation to social indicators.   

---

Hypothesis Testing:
I tested whether the level of Freedom significantly affects the Happiness Score.

Hypotheses:
H₀: Freedom and Happiness Score are independent.

H₁: There is a significant positive correlation between Freedom and Happiness Score.

Method
Test Used: Pearson Correlation Test

Variables: Freedom, Happiness Score

Tool: scipy.stats.pearsonr

Result: 
Correlation coefficient (r): 0.6429

P-value: < 0.0001
So..
The result is statistically SIGNIFICANT (p < 0.05)

Conclusion:

We reject the null hypothesis.
Countries with higher freedom tend to have higher happiness scores.

