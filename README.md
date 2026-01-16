# Market Basket Analysis Using Apriori Algorithm

## Project Overview
- Performed **Market Basket Analysis (MBA)** on a grocery dataset  
- Objective: identify frequent itemsets and association rules to understand customer buying behavior  
- Used Apriori algorithm to generate rules for cross-selling and promotions

## Dataset
- **Groceries_dataset.csv**  
- Contains transactions with:
  - Member_number  
  - Date  
  - itemDescription  

## Data Preprocessing & Feature Engineering
- Converted `Date` to datetime and extracted Year, Month, Day  
- Removed duplicate or irrelevant columns for analysis  
- Created **transactional format** suitable for Apriori:
  - One-hot encoding of items per transaction  
  - Aggregated items per customer per date  
- Converted data into a list of item lists for the Apriori algorithm

## Exploratory Data Analysis
- Identified **top-selling and least-selling items**  
- Analyzed **most active customers**  
- Examined sales distribution by:
  - Year  
  - Month  
  - Day of the month  
- Visualized trends using bar charts for top items and active customers

## Association Rule Mining
- Applied **Apriori algorithm** using `apyori` library  
- Parameters used:
  - Minimum support: 0.0002  
  - Minimum confidence: 1  
  - Minimum lift: 3  
  - Maximum rule length: 3  
- Generated frequent itemsets and association rules  
- Sorted rules by **lift** to identify strongest associations

## Key Insights
- Top-selling items frequently appear together in transactions  
- Certain item combinations have high confidence and lift, useful for promotions  
- Insights can help with **cross-selling, bundle offers, and inventory planning**

## How to Run the Repository
1. Clone the repository
   
        git clone https://github.com/Gem793/Market_Basket_Analysis
        cd market_basket_analysis
2. Install required dependencies
     
        pip install pandas numpy matplotlib seaborn apyori
3. Ensure `Groceries_dataset.csv` is in the project directory  
4. Launch Jupyter Notebook
    
        jupyter notebook
5. Run all cells to reproduce EDA, preprocessing, and Apriori analysis

## Technologies Used
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Apyori (Apriori algorithm implementation)

## Conclusion
- Market Basket Analysis helps uncover **hidden patterns in customer purchases**  
- Frequent itemsets and association rules provide actionable insights for **promotions and cross-selling**  
- Apriori algorithm is effective for discovering **high-confidence item associations** in transactional datasets
