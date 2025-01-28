
# Sales Performance Dashboard

Explore our **Sales Performance Dashboard** to gain valuable insights into sales, profit, and performance metrics.  

**[View the Live Looker Dashboard](https://your-looker-dashboard-link.com)**  

![Dashboard Overview](https://raw.githubusercontent.com/RitzyKingS/Worldwide-COVID-19-Analysis/main/images/google-site-screenshot.png)

---

## Key Features

### 1. Monthly Sales and Profit Trends
- **Sales Over Time:** Visualizes monthly sales trends from January 2019 to October 2020.
- **Profit Trends:** Displays profit performance across the same time frame.

### 2. Payment Mode Analysis
- **Sales by Payment Mode:** COD, Online, and Cards with respective sales figures.

### 3. Regional Performance
- **Sales by Region:** West, South, Central, and East performance comparison.

### 4. Segment and Category Analysis
- Sales by customer segments and product categories.

### 5. Shipping Insights
- Visual breakdown of sales by shipping mode.

### 6. Sub-Category Performance
- Detailed sub-category analysis for granular insights.

---

## Code Example

Here’s an example of how we used SQL to extract monthly sales data:

```sql
SELECT 
    DATE_TRUNC('month', ship_date) AS sales_month,
    SUM(sales) AS total_sales,
    SUM(profit) AS total_profit
FROM 
    sales_data
GROUP BY 
    sales_month
ORDER BY 
    sales_month;
```

For advanced visualizations, LookML code like the following was used:

```yaml
view: sales {
  dimension: ship_date {
    sql: ${TABLE}.ship_date ;;
  }
  measure: total_sales {
    type: sum
    sql: ${TABLE}.sales ;;
  }
  measure: total_profit {
    type: sum
    sql: ${TABLE}.profit ;;
  }
}
```

---

## How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/sales-performance-dashboard.git
   ```
2. Access the live dashboard:
   [View the Live Looker Dashboard](https://your-looker-dashboard-link.com)
3. Interact with visualizations to uncover key insights.

---

## Data Last Updated
**January 28, 2025, 3:36:36 PM**

---

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Happy Analyzing! 🚀
```
