# SQL and Snowflake Fundamentals

## Exercise Requirements

### 1. Problem Statement
You are tasked with analyzing pizza sales data for a food delivery service app that caters to sports fans, particularly Chelsea F.C. The management wants to understand how sales fluctuate over time, especially during key soccer matches. Your goal is to develop aggregation queries that summarize pizza sales data over time, taking into account the matches played by Chelsea F.C.

You will need to utilize SQL joins to combine the pizza sales data with match data to gain insights into how match outcomes affect pizza sales. 

**Tables involved:**
- **Pizza_Sales**: Contains columns `sale_id`, `sale_date`, `amount`, and `pizza_type`.
- **Matches**: Contains columns `match_id`, `match_date`, `team`, `opponent`, and `result`.

**Your task is to write SQL queries that:**
1. Aggregate total pizza sales by date.
2. Join the pizza sales data with match data to analyze sales on match days versus non-match days.

### 2. Fill-in-the-Blank Starter Code
```sql
-- Starter code for summarizing pizza sales data
SELECT 
    Pizza_Sales.sale_date AS sale_date,
    SUM(Pizza_Sales.amount) AS total_sales
FROM 
    Pizza_Sales
WHERE 
    Pizza_Sales.sale_date = _______ -- Fill in with the appropriate date condition
GROUP BY 
    Pizza_Sales.sale_date
ORDER BY 
    sale_date;

-- Joining Pizza Sales with Matches
SELECT 
    Matches.match_date,
    COUNT(Pizza_Sales.sale_id) AS total_pizza_sales,
    Matches.result
FROM 
    Matches
LEFT JOIN 
    Pizza_Sales ON Matches.match_date = Pizza_Sales.sale_date
WHERE 
    Matches.team = 'Chelsea F.C.'
GROUP BY 
    Matches.match_date, Matches.result
ORDER BY 
    Matches.match_date;
```

### 3. Hints
- **Hint 1**: When filling in the blank for the first query, consider how you might filter sales that occurred on a specific match date.
- **Hint 2**: For the second query, remember that a LEFT JOIN will allow you to see all matches played by Chelsea F.C., even if no pizzas were sold on those days.
- **Hint 3**: Think about how you can use aggregation functions like `SUM()` and `COUNT()` to get the total sales and the number of sales made.

### 4. Expected Outcome
By completing this exercise, you should be able to:
- Write SQL queries that aggregate data effectively using joins.
- Analyze how specific events (like soccer matches) influence sales patterns.
- Demonstrate your understanding of SQL concepts covered in the lecture, such as INNER, OUTER, LEFT, and RIGHT joins.

The final SQL queries should be well-structured, include appropriate comments explaining each step, and adhere to best practices in SQL coding. Ensure that your queries are tested for correctness and handle any potential errors gracefully.

---

This exercise is designed to challenge your understanding of SQL joins and aggregation while aligning with your interests in sports analytics and real-world applications in data processing. Happy querying!