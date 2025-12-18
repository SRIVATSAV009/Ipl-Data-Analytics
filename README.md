
# **Apple Products Price Analysis**
End-to-end data analysis pipeline for Apple iPhone pricing and customer sentiment on Flipkart marketplace.
Problem Statement
Analyze pricing strategies, discount patterns, and customer satisfaction metrics across iPhone product lines to identify market opportunities and consumer preferences.
Tech Stack
Python 3.9
Pandas 1.4.4
Jupyter Notebook
Dataset Overview
62 iPhone products scraped from Flipkart with complete data (no missing values).
Key Metrics:

Price range: ₹39,900 - ₹149,900
11 features including pricing, ratings, reviews, and specifications
4.5-4.7 star average ratings
100K+ customer reviews across products

Analysis Pipeline
1. Data Exploration
pythondf = pd.read_csv("apple_products.csv")
df.count()  # Validate completeness
df['Mrp'].max()  # 149900
df['Mrp'].min()  # 39900
2. Feature Engineering
Extracted model names from product titles using string slicing:
pythondf['Model Name'] = df['Product Name'].str[6:15]
3. Price Segmentation

Premium (≥₹100K): 22 products - iPhone 11 Pro Max, iPhone 12 Pro series
Mid-range (₹50-100K): 31 products - iPhone 11, iPhone 12 variants
Budget (<₹50K): 9 products - iPhone SE, iPhone 8 series

4. Customer Insights

iPhone 11 Pro Max: Highest ratings (4.7★)
iPhone SE: Most reviewed (95K+ ratings)
Zero discount on new Pro Max models
Up to 29% discount on older Pro models

Key Findings

Premium positioning: Pro Max models command ₹117K-149K with minimal discounting
Volume drivers: SE models dominate review counts despite lower pricing
Rating consistency: Tight 4.5-4.7 range across all price segments
Discount strategy: Aggressive discounts (14-29%) on previous-gen Pro models

Business Applications

Pricing optimization: Identify sweet spots in each segment
Inventory planning: High-review products indicate strong demand
Marketing strategy: Leverage high-rated models for promotions
Competitive analysis: Benchmark against market positioning

Quick Start
bashgit clone <repo-url>
pip install pandas numpy
jupyter notebook
Open Apple_Products_Analysis.ipynb and run all cells.
Files
├── apple_products.csv           # Raw data
├── Apple_Products_Analysis.ipynb # Analysis notebook
└── README.md
Next Steps

Time-series pricing analysis
Review text sentiment mining
Predictive pricing models
Competitor brand comparison
