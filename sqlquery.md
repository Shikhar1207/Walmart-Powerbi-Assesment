## Top 10 Customers by Total Purchase

This SQL query retrieves the top 10 customers (by `User_ID`) based on the total amount they have spent.

User_ID: Unique identifier for each customer.

SUM(Purchase): Aggregates total purchase amount per user.

GROUP BY: Groups transactions by user to compute totals.

ORDER BY ... DESC: Sorts users from highest to lowest total purchases.

LIMIT 10: Returns only the top 10 spenders.

### 📄 SQL Query

```sql
SELECT User_ID,
       SUM(Purchase) AS total_purchases
FROM walmartdb.walmart
GROUP BY User_ID
ORDER BY total_purchases DESC
LIMIT 10;
 
