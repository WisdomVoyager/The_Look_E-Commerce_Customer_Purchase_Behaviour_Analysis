# The_Look_E-Commerce_Customer_Purchase_Behaviour_Analysis

The link to Looker Studio BI Report - https://lookerstudio.google.com/reporting/0ad1ada1-f46f-4e7f-9cd8-2c2193b01fd5

The provided BIGQUERY SQL code creates two data models that analyze customer details and purchase behavior based on an e-commerce database. The data models are constructed using a combination of the "user_details" and "PURCHASE BEHAVIOR" queries, which join user information and order data to derive meaningful insights. Here's a description of the key components of these data models:

1. **User Details Data Model ("user_details"):**
   This data model combines information from the "users" and "order_items" tables to create a comprehensive profile for each user. The following attributes are extracted and processed:
   
   - `user_id`: A unique identifier assigned to each user, serving as a primary key in the users table.
   - `email`: The user's email address, a critical contact information piece.
   - `age`: The age of the user, providing demographic information.
   - `gender`: The gender of the user, reflecting their identity.
   - `country`: The user's country of residence, offering geographical insights.
   - `traffic_source`: The source from which the user was directed to the e-commerce platform (e.g., search engines, social media, email marketing).
   - `account_created`: The date the user's account was created on the e-commerce platform.
   - `order_id`: The unique identifier for each order placed by the user.
   - `product_id`: The identifier for the product associated with an order.
   - `order_date`: The date when an order was placed.
   - `sale_price`: The price paid for a product in a particular order.

2. **Purchase Behavior Data Model:**
   The second data model builds upon the "user_details" model to derive insights about user behavior and purchasing patterns. It includes the following attributes:

   - `user_id`, `email`, `age`, `gender`, `country`, `traffic_source`: User information carried over from the "user_details" model.
   - `cohort_date`: The date of the user's first order, used for cohort analysis.
   - `latest_shopping_date`: The date of the user's most recent order, indicating recent activity.
   - `lifespan_months`: The duration in months between the user's first and most recent orders, offering insights into user retention and lifecycle.
   - `LTV` (Lifetime Value): The total sales value associated with a user, calculated by summing up the sale prices of all orders placed by the user.
   - `purchase_frequency`: The total number of distinct orders made by the user, indicating their engagement level.
   - `avg_order_value` (Average Order Value): The average monetary value of each order placed by the user, calculated by dividing the total sales value by the number of distinct orders. This reflects the user's spending habits.

In summary, the provided SQL code generates two interconnected data models that enable comprehensive analysis of user details and purchase behavior within an e-commerce context. These models provide valuable insights into customer demographics, user engagement, retention, and purchasing patterns, facilitating data-driven decision-making for the e-commerce platform.
