# Innomatics-Research-Labs-Hackathon--Technical-Evaluation

🍽️ Food Delivery Data Integration & Analysis
Hackathon Project – Jupyter Notebook Based

📌 Project Overview

This project focuses on integrating food delivery data coming from multiple real-world data sources and transforming it into a single, analysis-ready dataset.

The goal is to simulate how data teams in companies like Swiggy or Zomato combine transactional and master data to answer meaningful business questions related to revenue, user behavior, and restaurant performance.

All work has been done strictly in a Jupyter Notebook, as per the hackathon instructions.

📂 Datasets Used

The project uses three different file formats, each representing a different system:

orders.csv

Transactional data

One row per order

Contains order amount, order date, user ID, and restaurant ID

users.json

User master data

Contains user details such as city and membership type (Gold / Regular)

restaurants.sql

Restaurant master data stored in SQL format

Contains cuisine type and restaurant ratings

These datasets were intentionally provided in different formats to simulate real-world data integration challenges.

🔧 Tools & Technologies

Google Colab / Jupyter Notebook

Python

Pandas (data manipulation)

SQLite (to load and query SQL data)

No external BI tools or scripts were used.

🔄 Data Integration Process

The integration process followed a clear and structured approach:

Loaded CSV and JSON files using Pandas

Loaded SQL data using SQLite inside the notebook

Performed LEFT JOINs to ensure no order data was lost

orders.user_id → users.user_id

orders.restaurant_id → restaurants.restaurant_id

Created a single merged dataset where:

Each row represents one order

User and restaurant details are repeated for multiple orders when applicable

The final dataset is saved as:

final_food_delivery_dataset.csv


This dataset acts as the single source of truth for all analysis.

📊 Analysis Performed

Using the final dataset, the notebook answers both conceptual and numerical questions, including:

Revenue contribution by Gold vs Regular members

City-wise and cuisine-wise performance

Average order values

Rating-based revenue analysis

User behavior patterns

Time-based (quarterly) revenue trends

All answers were derived directly from the merged dataset, without hardcoding or assumptions.

📁 Project Structure
├── Food_Delivery_Data_Integration.ipynb
├── orders.csv
├── users.json
├── restaurants.sql
├── final_food_delivery_dataset.csv
└── README.md

✅ Key Highlights

Fully reproducible Jupyter Notebook

Clear step-by-step explanations

No loss of transactional data (LEFT JOIN strategy)

Clean, analysis-ready final dataset

Designed with real-world data engineering practices in mind

🏁 Conclusion

This project demonstrates how data from different sources and formats can be combined into a unified dataset for meaningful business analysis.

The notebook not only answers the hackathon questions but also reflects how real analytics and data engineering workflows operate in production environments.

