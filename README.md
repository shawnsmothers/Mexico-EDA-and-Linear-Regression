# Mexico-EDA-and-Linear-Regression


## Project Overview
This project analyzes housing prices across various states in Mexico. The primary goal is to explore the relationship between house size (in square meters) and price, and to investigate how these variables differ across different states. Additionally, we aim to predict house prices using a regression model based on this data.

## Data Cleaning and Preparation
The raw data required extensive cleaning and preparation. The steps taken include:

1. **Cleaning Price Data**: 
   - Removed characters from the `price` column (e.g., currency symbols or other text).
   - Converted the `price` column from an object data type to a float for numerical analysis.
   
2. **Extracting State Information**:
   - Extracted the state names from a column where states were mixed with other characters, creating a new, clean column for the state.

3. **Handling Location Data**:
   - Split the combined `lanlon` column into two separate columns for latitude (`lat`) and longitude (`lon`).

4. **Combining Data**:
   - Merged three separate tables using `concat`/`append` methods to unify the data for further analysis.
   
5. **Handling Missing Data**:
   - Dropped rows with null values to ensure a clean dataset for exploration and modeling.

## Data Exploration
Several exploratory analyses were conducted to understand the housing market in Mexico:

1. **State-by-State Price Analysis**:
   - Examined the average price per state to see which regions had the highest and lowest property prices.

2. **State-by-State Price per Square Meter**:
   - Analyzed the price per square meter across different states to identify how house prices scale with size.

3. **Individual State Analysis**:
   - Looked at a few individual states and found that some states have a stronger correlation between house size (in square meters) and price than others.

## Key Findings
1. **Correlation Between Area and Price**:
   - In some states, there is a strong correlation between house size and price, while in others, the relationship is weaker.
   
2. **Urban vs Rural Pricing**:
   - It was observed that as the area (in square meters) decreases, the price per square meter tends to increase. This suggests that smaller homes, likely located in urban areas, are priced higher per square meter, whereas larger homes, likely in rural areas, are priced lower per square meter.

## Predictive Modeling
A regression model was built to predict house prices based on features such as area and location:

- **Model Performance**:
  - The regression model achieved an R² score of **88.87%**, meaning the model explains a significant portion of the variance in house prices. 
  - The model suggests that house size and location are important predictors for house prices in Mexico.

## Conclusion
This project provides insights into the housing market in Mexico, showing that house prices are influenced not only by size but also by location. The predictive model, while performing well, could be further improved by tuning or adding more features. Overall, this analysis demonstrates that larger homes tend to be located in rural areas and are priced lower per square meter compared to smaller homes in urban areas.

## Future Work
- Improve the model by incorporating additional features such as the number of bedrooms, age of the property, or proximity to amenities.
- Perform deeper analysis on the influence of economic factors like state GDP on house prices.

## Skills used
- Libraries: `pandas`, `numpy`, `matplotlib`, `scikit-learn`



