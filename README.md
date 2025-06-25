# Cost-and-Profitability-Analysis-of-Food-Orders-in-New-Delhi
To analyze the cost structure and profitability of a food delivery service in New Delhi using real order data. The goal is to identify unprofitable patterns and simulate strategic changes to improve margins.

# Dataset Overview
- Total Orders: 1,000
- Key Columns:
- Order ID,
- Order Value,
- Delivery Fee,
- Discounts and Offers,
- Commission Fee,
- Payment Processing Fee,
- Refunds/Chargebacks.

# Step-by-Step Process
1. Data Loading & Preparation
Imported libraries: pandas, numpy, matplotlib, seaborn, re.
Loaded dataset using pd.read_csv()

2. Data Cleaning
Converted monetary columns (e.g. Order Value, Delivery Fee) to float
Handled missing values and standardized discount formats.

3. Discount Calculation
Extracted discount types:
Percentage: e.g., "10%" → calculated as 10% of order value
Flat amount: e.g., "50 off" → extracted ₹50
Added new columns:
Discount Amount
Discount Percentage.

4. Cost and Profit Metrics
Computed:
Total Cost = Delivery Fee + Payment Fee + Discount
Profit = Commission Fee − Total Cost.

# Cost and Profitability Analysis
To understand the cost, we’ll look at three main expenses for each order:
- Delivery Fee – cost of delivering the food
- Payment Processing Fee – charge for handling the payment
- Discount Amount – any discount given to the customer

We’ll add these up to get the total cost per order, and then sum everything to see the overall cost for the platform.
On the revenue side, the platform mainly earns money from the Commission Fee.
Finally, we’ll calculate profit by subtracting the total cost from the commission earned on each order.
Let’s move ahead with this analysis.



![Screenshot 2025-06-25 084025](https://github.com/user-attachments/assets/400e7894-599f-4c84-899c-66f868de9a66)

# Overall Summary of Food Delivery Operations
- Total Orders: 1,000
- Total Revenue (Commission Fees): ₹126,990
- Total Costs: ₹232,709.85
- Total Profit: ₹-105,719.85

This analysis shows that the platform is operating at a loss. The total costs including delivery, payment processing, and discounts are much higher than the revenue from commission fees. This suggests that the current pricing, discount, and commission strategies are not sustainable and need to be adjusted to achieve profitability.


![Screenshot 2025-06-23 050407](https://github.com/user-attachments/assets/7bd811bf-26fa-411b-ad76-dd7fdd2b5c33)

The histogram shows that profit per order varies a lot, with many orders making a loss (profit below zero). The blue dashed line marks the average profit, which is also negativeclearly showing that the business is losing money overall.


![Screenshot 2025-06-25 084848](https://github.com/user-attachments/assets/fd62b796-783c-41e0-80fa-82421d9f46c1)

![Screenshot 2025-06-23 050810](https://github.com/user-attachments/assets/af2dcc0c-0928-4fda-96f4-fd77578cc5e6)

The pie chart breaks down the total costs into delivery fees, payment processing fees, and discounts. Discounts take up a large share, showing that promotions are a major contributor to the high costs and may be hurting overall profitability.

Now, let’s look at the overall numbers by comparing total revenue, total costs, and total profit (which is actually a net loss in this case). This comparison will clearly show whether the business is earning enough to cover its expenses.

![Screenshot 2025-06-25 085200](https://github.com/user-attachments/assets/9f1b624f-a890-4beb-ba38-37e374e6088f)


![Screenshot 2025-06-23 051034](https://github.com/user-attachments/assets/00fe5da0-356e-4927-84f8-365583761585)

The bar chart shows total revenue, total costs, and total profit side by side. It clearly highlights that costs are higher than revenue, resulting in an overall loss for the business.

# A New Strategy for Profitability
Our analysis shows that high discounts are a major reason for the platform’s losses. To turn this around, we need a better balance between discounts and commission rates a “sweet spot” that keeps customers happy while ensuring the business stays profitable.

What I am Looking For:
- To define this sweet spot, i will focus on orders that were actually profitable and calculate:
- The average commission percentage from these profitable orders
- The average discount percentage from the same group

These new averages will guide us in setting more sustainable discount and commission policies helping the business improve profitability not just on a few orders, but across the board.
Let’s go ahead and calculate them.

![Screenshot 2025-06-25 085648](https://github.com/user-attachments/assets/354fdfef-2e89-40ea-a984-b1bf4d1e79ac)

Analysis of profitable orders reveals a potential “sweet spot”:
Average Commission Percentage: 27.70%
Average Discount Percentage: 5.62%

These figures show that profitable orders tend to have higher commissions and lower discounts than the overall average. This suggests that increasing the commission rate and reducing discount levels could be key to boosting profitability. Aiming for a commission rate near 30% and a discount rate around 6% may help the business move toward overall profitability.

# Visualizing Profitability: Actual vs. Recommended Strategy
To understand how changes in discounts and commissions could affect profitability, we’ll compare two scenarios:

1. Actual Scenario
Use the existing discounts and commission rates from the dataset.
Calculate profit per order using:
Profit = Commission Fee - (Delivery Fee + Payment Processing Fee + Discount Amount)

2. Simulated (Recommended) Scenario
Apply a 6% discount and 27% commission across all orders.
Recalculate profit using:
Simulated Profit = (27% of Order Value) - (Delivery Fee + Payment Fee + 6% Discount)

Purpose of the Comparison:
This side-by-side view will show how many more orders could become profitable with the new strategy — helping us visualize the potential improvement in overall business performance.

Visualization Ideas:
Histogram comparing profit distributions in both scenarios

Bar chart showing total revenue, total cost, and total profit under both setups
Overlayed density plots to show the shift in profit per order
This comparison will help make a strong case for adopting the recommended discount and commission strategy.

![Screenshot 2025-06-25 090508](https://github.com/user-attachments/assets/d77fd269-b534-4f1a-a258-30935997ba06)

![Screenshot 2025-06-23 052948](https://github.com/user-attachments/assets/02b958f2-cb6d-4d0c-a32e-6bf61a749080)


The chart compares profit per order under two conditions: actual discounts and commissions, and a simulated scenario using the recommended 6% discount and 28% commission.
In the current setup, many orders show losses (profit < 0), with a wide range of profit levels. In contrast, the simulated results show a clear shift toward positive profits, suggesting that the recommended changes could lead to more consistently profitable orders.


# Summary
This is how you can analyze the cost and profitability of a food delivery business. The analysis involves looking at all expenses tied to each order including direct costs like delivery fees and packaging, and indirect costs such as customer discounts and restaurant commissions. By comparing these costs with the revenue earned (mainly from order values and commission fees), we can assess how profitable each order is and uncover ways to improve overall business performance.
