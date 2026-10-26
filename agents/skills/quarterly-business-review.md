---
title: "Quarterly business review"
description: "Use when the user asks for a quarterly business review, QBR, quarter summary, how the quarter went, or a fiscal quarter performance report."
---
Produce a one-page quarterly business review from `orders_transactions`, using fiscal quarters (see the business context rule: Q1 Feb to Apr, Q2 May to Jul, Q3 Aug to Oct, Q4 Nov to Jan).

1. Pick the quarter. Use the one the user names after the skill. If none is named, use the latest complete fiscal quarter in the data, not today's date. If the data ends partway through a quarter, say so and label that quarter as partial. State the exact dates used in one line.
2. Headline numbers for that quarter: Total Sale Price (revenue), Order Count and Average Order Value. Show each next to the previous fiscal quarter and the same quarter a year earlier, with the percentage change. Use `orders_transactions.created_at` as the date.
3. What drove the change: break revenue down by `orders_transactions.products_department` and by `orders_transactions.users_country` (top 5 plus the rest), and show which segments grew or shrank the most versus the previous quarter.
4. Top 5 product categories (`orders_transactions.products_category`) by revenue for the quarter.
5. Answer with a short narrative first (three or four sentences, lead with the biggest insight), then one KPI row, one chart of revenue by month across the quarter, and one table for the country breakdown.
6. End with one follow-up question, for example whether to dig into the segment that moved the most.
