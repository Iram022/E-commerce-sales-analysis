# E-commerce-sales-analysis

Amazon E-commerce Sales Analysis – Python EDA Project

This project performs exploratory data analysis (EDA) on an Amazon product dataset scraped from Amazon.in.
The goal is to extract insights about pricing, ratings, discounts, categories, and product performance using Python.

📁 Dataset Overview

The dataset contains product information such as:

product_id

product_name

category (hierarchical)

discounted_price

actual_price

discount_percentage

rating

rating_count

about_product

review_content

img_link, product_link

Total entries: varies per CSV.

🟦 Problem

The category column contains hierarchical data, e.g.:

Computers&Accessories|Accessories&Peripherals|Cables|USB Cables


Prices include symbols like ₹ and commas.
Ratings have missing values.
Rating_count has commas.

All of this requires cleaning before analysis.

🛠️ Tech Stack

Python

Pandas

NumPy

Matplotlib

Seaborn

Jupyter Notebook

🧹 Data Cleaning Steps

✔ Removed currency symbols (₹) and commas from price columns
✔ Converted discounted_price, actual_price, rating_count to numeric
✔ Converted discount_percentage to numeric
✔ Extracted the main_category (first level only) using string split
✔ Removed missing ratings
✔ Reset index, removed duplicates

Analysis Performed
1️⃣ Category Analysis

Count of products by category

Most common product categories

Extracted main_category for clear visualization

2️⃣ Price Analysis

Price distribution

Category-wise average price

Top 10 expensive categories/products

3️⃣ Ratings Analysis

Distribution of ratings

Average ratings by category

Relationship between rating & rating_count

4️⃣ Discount Analysis

Discount percentages by category

Correlation between discount & actual price

5️⃣ Correlation Analysis

Heatmap of numerical features

Relationships between price, rating, counts, discount

📊 Visualizations Used

Countplots (category, main_category)

Bar charts

Histogram (price, ratings)

Scatterplot (discount vs rating)

Heatmap (correlation)

Top 10 category charts

All visualizations generated using Matplotlib and Seaborn.

💡 Key Insights

1. Electronics dominates the catalog, indicating high demand and competition in this category.
2. The price distribution is heavily right-skewed, meaning the majority of Amazon products are budget or mid-range items.
3. Amazon products generally maintain high customer satisfaction, with most ratings clustered around 4.0–4.5.
4. Discounts do not significantly influence ratings — product quality drives customer satisfaction more than price cuts.
5. Actual and discounted prices are almost perfectly correlated, meaning most products receive proportional discounts
6. Popularity (rating_count) is independent of price or discount. Some cheap products can be very popular, while expensive ones may have fewer reviews.
7. 


