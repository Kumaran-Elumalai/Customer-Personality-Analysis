# PersonaSense

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Clustering-orange.svg)
![Data Science](https://img.shields.io/badge/Data-Science-green.svg)

## Overview
**PersonaSense** is a machine learning–driven customer intelligence system designed to identify meaningful customer segments based on demographic, behavioral, and purchasing patterns.

The project focuses on **translating raw customer data into actionable business insights** using unsupervised learning. Instead of treating all customers uniformly, PersonaSense enables organizations to identify high-value and behaviorally distinct customer personas that can be targeted with precision marketing and personalized strategies.

---

## Problem Statement
Businesses often collect rich customer data but struggle to leverage it effectively.  
Generic marketing campaigns result in:
- Inefficient spend
- Low engagement
- Poor personalization

**Goal:**  
Design a scalable and data-driven segmentation system that groups customers into coherent personas, enabling targeted decision-making and improved campaign effectiveness.

---

## Dataset Overview
The dataset captures customer demographics, purchase behavior, and campaign interactions.

### Attribute Categories

**Customer Profile**
- Unique customer identifier
- Year of birth
- Education level
- Marital status
- Household income
- Children and teenagers in household
- Customer enrollment date
- Recency of last purchase
- Complaint history

**Product Spending**
- Wine, fruits, meat, fish, sweets, gold products

**Marketing & Promotions**
- Discount purchases
- Campaign acceptance history
- Response to latest campaign

**Purchase Channels**
- Web purchases
- Catalog purchases
- In-store purchases
- Website visit frequency

---

## Methodology & System Design

### 1. Data Exploration & Understanding
- Inspected dataset structure, data types, and missing values  
- Performed exploratory data analysis (EDA) to understand:
  - Age and income distribution
  - Spending behavior across product categories
  - Channel-wise purchasing patterns
  - Customer engagement trends  

EDA was used to **inform downstream feature engineering decisions**, not just visualization.

---

### 2. Feature Engineering & Preprocessing
- Handled missing values and treated extreme outliers  
- Encoded categorical variables using appropriate encoding strategies  
- Scaled numerical features to ensure distance-based models behaved correctly  
- Dropped non-informative and leakage-prone columns  

This step was critical to ensure **cluster stability and meaningful separation**.

---

### 3. Model Exploration
Multiple clustering approaches were evaluated:

- **K-Means**
- **Agglomerative Clustering**
- **Mean Shift**

Rather than selecting a model upfront, the focus was on **empirical evaluation and interpretability**.

---

### 4. Model Selection & Evaluation
- Used the **Elbow Method** to estimate the optimal number of clusters  
- Evaluated cluster quality using the **Silhouette Score**  
- Compared clustering algorithms based on:
  - Separation quality
  - Stability
  - Business interpretability  

**K-Means** was selected as the final model due to superior silhouette performance and clear cluster boundaries.

---

## Results & Insights
The final model identified **distinct customer personas** with significant differences in:
- Spending behavior
- Engagement levels
- Campaign responsiveness

Key insights:
- High-income customers exhibited concentrated spending in specific product categories  
- Certain clusters showed strong responsiveness to promotional campaigns  
- Low-engagement segments were clearly separable from high-value customers  

These insights enable **targeted marketing, personalization, and optimized resource allocation**.

---

## Deployment
The trained clustering pipeline was deployed using **Streamlit**, enabling an interactive interface where:
- Users can input customer attributes
- Customers are assigned to a predicted persona
- Business teams can interpret segmentation results in real time

Deployment logic is implemented in:
CustomerSegmentationwebapp.py


This demonstrates **end-to-end ownership**, from data analysis to a user-facing application.

---

## Tech Stack
- **Language:** Python  
- **Data Processing:** Pandas, NumPy  
- **Modeling:** Scikit-learn  
- **Clustering:** K-Means, Agglomerative Clustering, Mean Shift  
- **Evaluation:** Silhouette Score, Elbow Method  
- **Visualization:** Matplotlib, Seaborn, Plotly  
- **Deployment:** Streamlit  

---

## Repository Structure
```
persona-sense/
│
├── Final_Project_Customer_Personality_Analysis.ipynb # EDA & model development
├── CustomerSegmentationwebapp.py # Streamlit deployment
├── requirements.txt # Project dependencies
├── .gitignore # Ignored files
├── LICENSE # MIT License
└── README.md # Project documentation
```


---

## Key Engineering Decisions
- Chose **unsupervised learning** due to lack of labeled customer personas  
- Evaluated multiple clustering strategies before final selection  
- Prioritized **cluster interpretability and stability** over algorithmic complexity  
- Ensured feature scaling to maintain distance-based model correctness  

---

## Learnings
- Importance of preprocessing in unsupervised ML workflows  
- Evaluating clustering quality beyond visual inspection  
- Translating analytical results into business-friendly insights  
- Deploying ML solutions for real-world usability  

---

## Future Improvements
- Automated persona labeling and narrative generation  
- Integration with live customer data sources  
- Experimentation with density-based and probabilistic clustering (DBSCAN, GMM)  
- Enhanced Streamlit UI for non-technical users  

---

## License
This project is licensed under the **MIT License**.

---

## Author
**Kumaran Elumalai**  
AI / ML Engineer | Data Scientist  

🔗 GitHub: https://github.com/Kumaran-Elumalai  
🔗 LinkedIn: https://linkedin.com/in/kumaran-elumalai
