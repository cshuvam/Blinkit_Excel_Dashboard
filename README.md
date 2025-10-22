# Blinkit Sales Dashboard in Excel

This project is an Excel dashboard I put together to look at how [Blinkit](https://blinkit.com/) is doing with sales, how happy customers are, and where they're selling stuff. It uses some key numbers (KPIs) and cool charts to help us understand what's working well and where things could be better.

---

## Table of Contents
* [Overview](#overview)
* [Key Performance Indicators (KPIs)](#key-performance-indicators-kpis)
* [Charts and Visuals](#charts-and-visuals)
* [Data Source & Preparation](#data-source--preparation)
* [Dashboard Features](#dashboard-features)
* [Usage](#usage)
* [Dashboard Insights](#dashboard-insights)
* [Conclusion](#conclusion)
* [Acknowledgement](#acknowledgement)

---

## Overview

My main goal with this project was to dig into Blinkit's sales data. I wanted to find out important trends, new chances for growth, and areas that need a little tweak. This meant checking out sales numbers, customer ratings, and how different stores and product types are performing.

---

## Key Performance Indicators (KPIs)

To get a quick overview of the business, I tracked these important numbers:

1.  **Total Sales**: This is simply all the money made from everything sold.
2.  **Average Sales**: This tells us the average money made per sale.
3.  **Number of Items**: The total count of all the different things sold.
4.  **Average Rating**: This shows how customers generally rate the items they buy.

---

## Charts and Visuals

I included several interactive charts in the dashboard so we can dive deeper into the data:

1.  **Total Sales by Fat Content**:
    *   **Goal**: To see if the fat content of an item affects how much it sells.
    *   **What else it shows**: It also helps us see how Average Sales, Number of Items, and Average Rating change with different fat content.
    *   **Chart Type**: A donut chart.

2.  **Total Sales by Item Type**:
    *   **Goal**: To find out which types of items (like snacks or fruits) are selling best.
    *   **What else it shows**: It also helps us see how Average Sales, Number of Items, and Average Rating change for different item types.
    *   **Chart Type**: A bar chart.

3.  **Fat Content by Outlet for Total Sales**:
    *   **Goal**: To compare sales across different Blinkit stores, broken down by the fat content of the items.
    *   **What else it shows**: It also helps us see how Average Sales, Number of Items, and Average Rating vary by fat content at each store.
    *   **Chart Type**: A stacked column chart.

4.  **Total Sales by Outlet Establishment Year**:
    *   **Goal**: To see if older or newer stores sell more over time.
    *   **Chart Type**: A line chart.

5.  **Sales by Outlet Size**:
    *   **Goal**: To check if the size of a store (Small, Medium, or Big) has anything to do with its total sales.
    *   **Chart Type**: A donut or pie chart.

6.  **Sales by Outlet Location**:
    *   **Goal**: To understand where sales are happening most, like in big cities (Tier 1) or smaller towns (Tier 3).
    *   **Chart Type**: A funnel map (shown as a bar chart here).

7.  **All Metrics by Outlet Type**:
    *   **Goal**: To get a full picture of all the key numbers (Total Sales, Average Sales, Number of Items, Average Rating) for different kinds of stores (like Supermarkets or Grocery Stores).
    *   **Chart Type**: A matrix card.

---

## Data Source & Preparation

I used a [**Blinkit_Grocery_Source_Data.xlsx**](https://github.com/cshuvam/Blinkit_Excel_Dashboard/blob/main/data/Blinkit_Grocery_Source_Data.xlsx) dataset with about 8,500 rows and 12 columns, where each row is a single item sale. The data included things like:

*   `Item_Fat_Content`: If the product was "Low Fat" or "Regular."
*   `Item_Identifier`: A unique code for each item.
*   `Item_Type`: What kind of item it was (e.g., "Snack Foods," "Soft Drinks").
*   `Outlet_Establishment_Year`: The year the store was set up.
*   `Outlet_Identifier`: A unique code for each store.
*   `Outlet_Location_Type`: If the store was in a Tier 1, Tier 2, or Tier 3 city.
*   `Outlet_Size`: How big the store was (Small, Medium, High).
*   `Outlet_Type`: What kind of store it was (e.g., "Supermarket," "Grocery Store").
*   `Item_Visibility`: How easy it was to find the item online.
*   `Item_Weight`: The weight of the item.
*   `Sales`: How much money was made from that item.
*   `Rating`: The customer's rating for the item.

---

### Data Cleaning

Before I could analyze anything, I had to clean up the data a bit:

*   **Making Fat Content Consistent**: Some entries for fat content were shortened (like "LF" or "R"), so I changed them all to "Low Fat" and "Regular" to make sure everything was uniform.
*   **Adding a Serial Number**: I added a simple "Serial Number" column to easily count how many items were sold.
*   **Dealing with Empty Spaces**: I checked for any blank spots in the data. For example, it's okay if `Item_Weight` is sometimes blank, but `Sales` should always have a number if an item was sold!

---

## Dashboard Features

*   **Interactive Filters**: You can play around with the dashboard by using filters for `Outlet Size`, `Outlet Location`, and `Item Type` to see different views of the data.
*   **Easy Navigation**: There are buttons to jump between the main dashboard, detailed tables (pivot tables), and the raw data sheet.
*   **Look and Feel**: I designed the dashboard to be easy to use and visually appealing, using yellow and green colors that match Blinkit's brand.

---

## Usage

1.  **Get the Excel file**: You'll find the [**Blinkit_Analysis_Dashboard.xlsx**](https://github.com/cshuvam/Blinkit_Excel_Dashboard/blob/main/Blinkit_Analysis_Dashboard.xlsx) file right here in this project.
2.  **Open it up**: Make sure you're using Excel 2019 or a newer version so everything works perfectly.
3.  **Start exploring!**: Click around on the filters and buttons to discover interesting things about Blinkit's sales.

---

## Dashboard Insights

### Overall Dashboard View (Unfiltered)

The dashboard looks clean and is easy to use, with a yellow and green color scheme that matches Blinkit's brand. At the top, you'll see the main numbers: Total Sales ($1.20M), Average Sales ($141), Number of Items (8523), and Average Rating (4.0).

![Overall Dashboard View](https://github.com/cshuvam/Blinkit_Excel_Dashboard/blob/main/assets/dashboard_images/dashboard.jpg)

Here's what the main charts show:
*   **Fat Content**: A donut chart shows that items with "Regular" fat content sell a lot more ($776.32K) than "Low Fat" items ($425.36K).
*   **Item Type**: A bar chart tells us that "Fruits and Vegetables" ($178.12K) and "Snack Foods" ($175.43K) are the best-selling item types.
*   **Fat by Outlet**: This chart helps compare sales of different fat content items across various stores.
*   **Outlet Establishment**: A line chart shows how sales have changed each year from 2011 to 2022, with a peak in 2018 ($204.52K).
*   **Outlet Size**: A donut chart reveals that "Medium" sized stores bring in the most sales ($507.90K, 42%).
*   **Outlet Location**: A bar chart (like a funnel map) indicates that stores in Tier 3 cities have the highest sales ($472.13K).
*   **Outlet Type**: A table (matrix card) shows sales, average sales, and number of items for different store types. "Supermarket Type1" has the highest total sales ($707.55K).

---

### Filtered View: Outlet Size - High

*   **Filters Applied**: I've selected `High` for `Outlet Size`.
*   **Key Insights**:
    *   Total Sales: $0.25M, Number of Items: 1753, Average Rating: 3.9.
    *   Even in high-sized outlets, "Regular" fat content items still sell more ($122.86K) than "Low Fat" items ($126.13K).
    *   "Snack Foods" ($42.34K) and "Fruits and Vegetables" ($34.83K) are still the top sellers.
    *   Sales from stores established in 2014 had a peak ($131.81K) but then declined in later years.
    *   Stores in Tier 3 locations have the highest sales ($164.38K) for high-sized outlets.
    *   "Supermarket Type1" is the main type of high-sized outlet, bringing in $216.42K in total sales.

![Outlet Size - High Filtered View](https://github.com/cshuvam/Blinkit_Excel_Dashboard/blob/main/assets/dashboard_images/outlet_high.jpg)

---

### Filtered View: Outlet Size - Medium

*   **Filters Applied**: I've selected `Medium` for `Outlet Size`.
*   **Key Insights**:
    *   Total Sales: $0.51M, Number of Items: 3631, Average Rating: 4.0.
    *   "Regular" fat content items sell much more ($338.23K) than "Low Fat" items ($169.67K) in medium-sized outlets.
    *   "Fruits and Vegetables" ($83.57K) and "Snack Foods" ($72.19K) are the leading item types here.
    *   Sales from stores established in 2014 ($130.48K) and 2018 ($130.71K) show consistent good performance.
    *   Tier 3 cities ($299.37K) are where medium-sized outlets perform best.
    *   "Supermarket Type1" ($208.53K) is the most common and highest-selling type of medium outlet.

![Outlet Size - Medium Filtered View](https://github.com/cshuvam/Blinkit_Excel_Dashboard/blob/main/assets/dashboard_images/outlet_medium.jpg)

---

### Filtered View: Outlet Size - Small

*   **Filters Applied**: I've selected `Small` for `Outlet Size`.
*   **Key Insights**:
    *   Total Sales: $0.44M, Number of Items: 3139, Average Rating: 4.0.
    *   "Regular" fat content items still lead sales ($315.23K) over "Low Fat" items ($129.57K) in small outlets.
    *   "Snack Foods" ($60.90K) and "Fruits and Vegetables" ($59.72K) are the top item types.
    *   Sales from stores established in 2016 had a peak ($132.11K).
    *   Tier 2 ($230.49K) and Tier 1 ($205.92K) cities are the main locations for small-sized outlets.
    *   "Supermarket Type1" ($361.60K) is the primary outlet type for small stores.

![Outlet Size - Small Filtered View](https://github.com/cshuvam/Blinkit_Excel_Dashboard/blob/main/assets/dashboard_images/outlet_small.jpg)

---

### Filtered View: Outlet Location - Tier 1

*   **Filters Applied**: I've selected `Tier 1` for `Outlet Location`.
*   **Key Insights**:
    *   Total Sales: $0.47M, Number of Items: 3350, Average Rating: 4.0.
    *   "Regular" fat content items contribute more to sales ($306.81K) than "Low Fat" items ($165.33K) in Tier 1 cities.
    *   "Fruits and Vegetables" ($70.73K) and "Snack Foods" ($66.69K) are the top item types.
    *   Sales from stores established in 2018 had a peak ($130.71K).
    *   "Medium" sized outlets are the biggest contributors (63%) to sales in Tier 1 locations.
    *   "Supermarket Type1" ($181.18K) is the leading outlet type in Tier 1 cities.

![Outlet Location - Tier 1 Filtered View](https://github.com/cshuvam/Blinkit_Excel_Dashboard/blob/main/assets/dashboard_images/tier1.jpg)

---

### Filtered View: Outlet Location - Tier 2

*   **Filters Applied**: I've selected `Tier 2` for `Outlet Location`.
*   **Key Insights**:
    *   Total Sales: $0.39M, Number of Items: 2785, Average Rating: 4.0.
    *   "Regular" fat content items lead sales ($254.46K) over "Low Fat" items ($138.69K) in Tier 2 cities.
    *   "Snack Foods" ($57.93K) and "Fruits and Vegetables" ($57.27K) are the top item types.
    *   Sales from stores established in 2017 had a peak ($133.40K).
    *   "High" sized outlets are the biggest contributors (59%) to sales in Tier 2 locations.
    *   "Supermarket Type1" ($393.15K) is the dominant outlet type in Tier 2 cities.

![Outlet Location - Tier 2 Filtered View](https://github.com/cshuvam/Blinkit_Excel_Dashboard/blob/main/assets/dashboard_images/tier2.jpg)

---

### Filtered View: Outlet Location - Tier 3

*   **Filters Applied**: I've selected `Tier 3` for `Outlet Location`.
*   **Key Insights**:
    *   Total Sales: $0.34M, Number of Items: 2388, Average Rating: 4.0.
    *   "Regular" fat content items contribute more to sales ($215.05K) than "Low Fat" items ($121.35K) in Tier 3 cities.
    *   "Fruits and Vegetables" ($50.13K) and "Snack Foods" ($48.81K) are the top item types.
    *   Sales from stores established in 2016 had a peak ($132.11K).
    *   "Medium" sized outlets are the biggest contributors (61%) to sales in Tier 3 locations.
    *   "Supermarket Type1" ($202.59K) is the leading outlet type in Tier 3 cities.

![Outlet Location - Tier 3 Filtered View](https://github.com/cshuvam/Blinkit_Excel_Dashboard/blob/main/assets/dashboard_images/tier3.jpg)

---

## Conclusion

After looking closely at Blinkit's sales data, here are some key things I found and what I think Blinkit could do:

### **Key Findings**

*   **Fat Content Matters**: Items with "Regular" fat content consistently sell more, no matter the store size or location. This probably means customers prefer these items, or maybe they're just more available and promoted.
*   **Top Sellers**: "Fruits and Vegetables" and "Snack Foods" are always the best-selling items.
*   **Store Performance**:
    *   **Store Size**: "Medium" sized stores bring in the most sales, then "Small," and then "High." This suggests that having a good mix of store sizes, or placing medium stores in just the right spots, works best.
    *   **Store Location**: Stores in Tier 3 cities (often smaller towns) have the highest sales, followed by Tier 2 and then Tier 1 (big cities). This could mean more customers, less competition, or really good operations in those Tier 3 areas.
    *   **Store Type**: "Supermarket Type1" stores are the clear winners in sales compared to "Grocery Stores."
*   **Sales Ups and Downs**: The chart showing sales over the years has some highs and lows. It would be good to understand *why* sales went up or down in certain years (e.g., new promotions, changes in the market).
*   **Happy Customers**: The average customer rating is pretty good, usually around 4.0, which means customers are generally satisfied.

---

### **Recommendations (for Blinkit)**

1.  **Boost "Regular" Fat Content Items**: Since "Regular" fat content items sell so well, Blinkit should make sure they always have enough stock and maybe even promote them more. This way, they can really make the most of what customers already like.
2.  **Keep an Eye on Top Items**: Keep giving "Fruits and Vegetables" and "Snack Foods" priority in terms of stock, promotions, and how easy they are to find on the app, because they're consistently the best sellers. Also, think about ways to make other item types sell better, maybe with special deals or new product options.
3.  **Smart Store Growth**:
    *   **Focus on Medium Stores**: It makes sense to invest more in or improve medium-sized stores, as they're currently bringing in the most money. They seem to be really good at reaching a lot of customers.
    *   **Learn from Tier 3 Success**: Since Tier 3 cities have the highest sales, Blinkit should look into what makes them so successful. Then, they could try those same strategies in other city tiers or open more stores in similar markets to grow even more.
4.  **Understand Sales Changes**: Take a closer look at the years where sales changed a lot (like the big sales in 2018 or drops in other years). By figuring out *why* these changes happened (e.g., new marketing campaigns, economic shifts), Blinkit can make better decisions for the future.
5.  **Keep Customers Happy**: Even though ratings are good, it's always a good idea to keep checking in with customers and finding ways to make their experience even better. This helps keep ratings high and customers coming back.
6.  **Learn from "Supermarket Type1"**: Study what makes "Supermarket Type1" stores so successful, as they're the top performers. Blinkit could then use those successful methods in other types of stores or even open more "Supermarket Type1" locations where it makes sense.

---

## Acknowledgement

A special thanks to [Swapnjeet S](https://www.linkedin.com/in/swapnjeet-s-58a673273/) for providing the data required for analysis and guiding throughout this project, as outlined in this [video tutorial](https://www.youtube.com/watch?v=klZj_282ApY).

---
