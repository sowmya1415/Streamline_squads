🛒 OmniRetail Data Platform – Databricks Lakehouse Project
📌 Project Overview

OmniRetail is a multi-channel retail business operating across physical stores, web platforms, and mobile applications.
Despite growth in sales and customers, the organization faces challenges in obtaining a unified and reliable view of its operations.

This project aims to design and implement a modern data platform using Databricks Lakehouse architecture to unify data, improve reporting, and enable data-driven decision-making.

🚨 Business Problem

OmniRetail currently struggles with:

Disconnected data sources across systems
Duplicate and inconsistent records
Delayed and manual reporting processes
Poor inventory visibility (stockouts & overstocking)
Limited understanding of customer behavior
Lack of forecasting and planning capabilities
No governed self-service analytics

These challenges result in slow, reactive decision-making and missed business opportunities.

🎯 Project Objectives

The main goals of this project are:

Provide a single source of truth for business data
Enable faster and reliable reporting
Improve inventory planning and visibility
Analyze customer behavior and retention
Support future demand forecasting
Reduce manual effort in data processing
Build a scalable analytics foundation
📊 Datasets Used
Olist E-commerce Dataset (Kaggle)
Superstore Dataset (Kaggle)
Custom datasets:
inventory.csv
stores.csv
promotions.csv
🗂️ Core Tables
Customers
Orders
Order Items
Payments
Products
Reviews
Inventory
Stores
Promotions
🏗️ Architecture Overview

The project follows the Medallion Architecture:

Source Systems → Cloud Storage → Bronze → Silver → Gold → Dashboard

Bronze Layer: Raw data ingestion (as-is storage)
Silver Layer: Cleaned, standardized, and joined data
Gold Layer: Business-level aggregated KPIs
⚙️ Data Pipeline Flow
Ingestion (Bronze Layer)
Load raw CSV/JSON files
Add metadata (file name, ingestion time, batch ID)
Store as Delta tables
Data Processing (Silver Layer)
Remove duplicates
Handle null values
Standardize formats
Validate data quality
Join multiple datasets
Business Aggregation (Gold Layer)
Generate KPIs and insights
Create analytics-ready tables
Visualization
Connect to dashboards for business reporting
📈 Key Business Outputs
Daily Revenue
Monthly Growth Trends
Top Customers
Category Performance
Regional Sales Analysis
Inventory Risk (Stockouts/Overstock)
Repeat Customer Rate
Promotion Effectiveness
🔍 Business Insights Delivered
Top revenue-generating cities
Slow-moving and high-risk inventory
Customer retention trends
Cancellation patterns
Most profitable product categories
Promotion impact analysis
Underperforming regions
🔄 Incremental Data Processing
Daily data ingestion using new files
Process only new/unseen data
Maintain historical records
Ensure efficient and scalable updates
🧪 Data Quality Checks
Unique order IDs
Non-null mandatory fields
Valid price and date values
Tracking unmatched records
Source vs target data validation
🚀 Key Features
Scalable Lakehouse architecture
Reliable data storage with ACID properties
Support for real-time and batch processing
Structured data governance
Optimized query performance
All members contributed to overall design and implementation
📦 Deliverables
Databricks Notebooks
SQL Scripts
Architecture Diagram
Dashboard Screenshots
Presentation Slides
Demo Video
GitHub Repository
❓ Key Discussion Points
Why Lakehouse over traditional warehouse?
Benefits of Medallion Architecture
Importance of incremental processing
Role of data quality in analytics
How to scale this solution in production
🏁 Conclusion

This project demonstrates how a modern data platform can transform a fragmented retail system into a unified, insight-driven ecosystem, enabling faster decisions, improved efficiency, and long-term business growth.
