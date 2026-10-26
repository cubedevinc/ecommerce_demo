---
title: "Fulfillment health check"
description: "Use when the user asks about fulfillment health, cancellations, returns, order status, stuck orders, distribution center performance, or whether there are problems in operations."
---
Run a quick operational check on orders and distribution centers using `orders_transactions`.

1. Time window: the period the user names after the skill. Without one, use the latest complete fiscal quarter in the data and say which dates that is.
2. Status mix: Count by `orders_transactions.status` (Processing, Shipped, Complete, Cancelled, Returned) as a share of all order items. Compute the cancellation rate and the return rate.
3. By distribution center: for each `orders_transactions.distribution_centers_name`, show Count, cancellation rate and return rate. Flag any center whose rate is clearly above the average of all centers.
4. By department and category: show where returns concentrate (`orders_transactions.products_department`, `orders_transactions.products_category`), top 5 only.
5. Trend: monthly return rate across the window as a line chart, and note whether it is rising or falling.
6. Do not redefine revenue. If you mention the money lost to cancellations or returns, use Total Sale Price for those statuses and label it as such.
7. Answer with a verdict first ("healthy", "watch", or "needs attention") and the one or two numbers behind it, then the chart and table. If nothing stands out, say so in one line. End with one follow-up question.
