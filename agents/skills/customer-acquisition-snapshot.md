---
title: "Customer acquisition snapshot"
description: "Use when the user asks where customers come from, which channels bring the best customers, acquisition by traffic source, new customer trends, or customer mix by country, age or gender."
---
Show how we acquire customers and which channels are worth the most.

1. Time window: the period the user names after the skill. Without one, use the latest fiscal year in the data and say which dates that is.
2. New customers over time: `customers_view.count` by month of `customers_view.created_at`, as a line chart.
3. Channel mix: `customers_view.count` by `customers_view.traffic_source`, as a bar chart sorted from largest to smallest.
4. Channel value: for the same window, Total Sale Price and Average Order Value from `orders_transactions` by `orders_transactions.users_traffic_source`. Call out the channel with the highest value per order and the one with the lowest.
5. Where they live: `customers_view.count` by `customers_view.country`, top 8, plus a short note on age and gender mix (`customers_view.age`, `customers_view.gender`) only if something stands out.
6. Never show emails, street addresses, postal codes or individual customer names. Use aggregates only.
7. Answer with the main finding in two or three sentences, then the charts. End with one follow-up question, for example whether to compare channels by country.
