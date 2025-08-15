Ola Ride Analytics - README
===========================

Project Overview
----------------
The Ola Ride Analytics project is a Power BI dashboard built to analyze Ola ride booking data. 
It helps identify ride trends, cancellations, vehicle performance, and customer/driver behavior.
This enables stakeholders to make data-driven decisions for business improvements.

Objectives
----------
- Track ride volume and trends over time.
- Analyze booking status and cancellation reasons.
- Compare customer vs. driver ratings.
- Assess vehicle type performance.
- Evaluate payment method preferences.

Business Questions Addressed
----------------------------
1. Ride Volume Over Time – How many rides are booked per month?
2. Booking Status Breakdown – What proportion of rides are completed, cancelled, or ongoing?
3. Average Customer Ratings by Vehicle Type – How do customers rate each vehicle category?
4. Revenue by Payment Method – Which payment methods generate the most revenue?
5. Ride Distance Distribution Per Day – What is the spread of ride distances on a daily basis?

Key Metrics & Measures
----------------------
- Total Rides = COUNTROWS(Rides)
- Completed Rides = CALCULATE([Total Rides], Rides[Ride_Status] = "Completed")
- Cancelled Rides = CALCULATE([Total Rides], Rides[Ride_Status] = "Cancelled")
- Cancellation % = DIVIDE([Cancelled Rides], [Total Rides], 0)
- Avg Customer Rating = AVERAGE(Rides[Customer_Rating])
- Avg Driver Rating = AVERAGE(Rides[Driver_Rating])
- Revenue by Payment Method = SUM(Fare_Amount) grouped by Payment_Method
- Average Ride Distance
