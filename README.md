# 🚖 OLA Ride Analytics Dashboard

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow)
![SQL](https://img.shields.io/badge/SQL-Analysis-blue)
![Excel](https://img.shields.io/badge/Excel-Data%20Preparation-green)

## 📌 Project Overview

This project focuses on analyzing OLA ride booking data using **Power BI, SQL, and Excel** to provide actionable business insights related to ride bookings, revenue generation, cancellations, vehicle performance, and customer satisfaction.

The dashboard enables stakeholders to monitor operational KPIs and make data-driven decisions for improving ride completion rates and overall business performance.

---
## 📌 Dataset Used 

-<a href="https://github.com/kartikgawali-00/OLA-Ride-Analytics-Dashboard/blob/main/Dataset.csv">Dataset</a>


## 🎯 Project Objective

The objective of this project is to build an interactive dashboard that helps answer critical business questions such as:

* How many rides are booked daily?
* What is the overall revenue generated?
* Which vehicle types perform best?
* What are the major reasons for ride cancellations?
* Which payment methods contribute most to revenue?
* How satisfied are customers and drivers?

---

## 🛠️ Tools & Technologies Used

| Tool        | Purpose                     |
| ----------- | --------------------------- |
| Power BI    | Dashboard Development       |
| SQL         | Data Analysis               |
| Excel       | Data Cleaning & Preparation |
| DAX         | KPI Creation                |
| Power Query | Data Transformation         |

---

## 📂 Dataset Information

The dataset includes:

* Booking ID
* Customer ID
* Vehicle Type
* Ride Distance
* Booking Value
* Booking Status
* Payment Method
* Driver Rating
* Customer Rating
* Cancellation Reasons
* Booking Date

---

# 📊 Dashboard Pages

## 1️⃣ Overall Dashboard

### KPIs

✔ Total Bookings

✔ Total Revenue

✔ Booking Status Breakdown

✔ Ride Volume Trend

### Key Metrics

* Total Bookings: **103,024**
* Total Revenue: **₹35 Million**
* Successful Bookings: **63,967**
* Booking Success Rate: **62.09%**

### Dashboard Preview

> Add Screenshot Here

```markdown
![Overall Dashboard]([screenshots/overall_dashboard.png](https://github.com/kartikgawali-00/OLA-Ride-Analytics-Dashboard/blob/main/Dashboard%20Images/Screenshot%202026-06-01%20182805.png))
```

---

## 2️⃣ Vehicle Type Analysis

### Business Questions

* Which vehicle type generates the highest booking value?
* Which category contributes the highest successful bookings?
* What is the average distance travelled?

### Vehicle Categories

* Prime Sedan
* Prime SUV
* Prime Plus
* Mini
* Auto
* Bike
* E-Bike

### Dashboard Preview

```markdown
![Vehicle Dashboard](screenshots/vehicle_dashboard.png)
```

---

## 3️⃣ Revenue Analysis

### Business Questions

* Which payment method generates maximum revenue?
* What are the daily revenue trends?
* Who are the top customers?

### Insights

* Cash contributes highest revenue.
* UPI is the second preferred payment mode.
* Card payments contribute relatively lower revenue.

### Dashboard Preview

```markdown
![Revenue Dashboard](screenshots/revenue_dashboard.png)
```

---

## 4️⃣ Cancellation Analysis

### Business Questions

* What is the cancellation rate?
* Why are customers cancelling rides?
* Why are drivers cancelling rides?

### Key Metrics

* Total Cancelled Bookings: **28,933**
* Cancellation Rate: **28.08%**

### Dashboard Preview

```markdown
![Cancellation Dashboard](screenshots/cancellation_dashboard.png)
```

---

## 5️⃣ Ratings Analysis

### Business Questions

* How do customer ratings vary by vehicle type?
* How do driver ratings compare?

### Insights

* Average ratings remain close to 4.0.
* Customer satisfaction is consistent across categories.

### Dashboard Preview

```markdown
![Ratings Dashboard](screenshots/ratings_dashboard.png)
```

---

# 🔍 SQL Analysis

### Total Bookings

```sql
SELECT COUNT(*) AS Total_Bookings
FROM Ola_Bookings;
```

### Revenue Analysis

```sql
SELECT SUM(Booking_Value) AS Revenue
FROM Ola_Bookings;
```

### Booking Status Analysis

```sql
SELECT Booking_Status,
       COUNT(*) AS Total_Bookings
FROM Ola_Bookings
GROUP BY Booking_Status;
```

---

# 📈 DAX Measures

### Total Bookings

```DAX
Total Bookings =
COUNT('OLA'[Booking_ID])
```

### Revenue

```DAX
Revenue =
SUM('OLA'[Booking_Value])
```

### Cancellation Rate

```DAX
Cancellation Rate =
DIVIDE(
    [Cancelled Bookings],
    [Total Bookings]
) * 100
```

---

# 💡 Key Insights

### Overall Performance

* 103K+ bookings analyzed.
* ₹35M total booking value generated.
* 62% ride success rate achieved.
* 28% bookings were cancelled.

### Vehicle Analysis

* Prime Sedan generated the highest booking value.
* Premium vehicles contributed significantly to revenue.
* Auto rides recorded the shortest travel distance.

### Revenue Analysis

* Cash is the most preferred payment method.
* UPI adoption is strong and growing.
* Card payments have the lowest contribution.

### Cancellation Analysis

* Driver-related issues account for the largest share of cancellations.
* Customer cancellations impact overall ride completion.

### Ratings Analysis

* Average ratings remain around 4.0.
* Customer satisfaction remains stable across vehicle categories.

---

# 🚀 Business Recommendations

### Improve Driver Availability

Reduce ride cancellations by improving driver allocation and availability.

### Promote Digital Payments

Encourage UPI and card transactions through rewards and cashback programs.

### Focus on High Performing Categories

Expand and optimize Prime Sedan and Prime Plus services.

### Reduce Cancellation Rates

Improve ETA accuracy and customer communication.

### Maintain Service Quality

Continue monitoring ratings and customer feedback.

---

# 🏆 Skills Demonstrated

### Power BI

* Data Modeling
* DAX
* Power Query
* Interactive Dashboards
* KPI Design

### SQL

* Aggregations
* Group By
* Filtering
* KPI Queries

### Excel

* Data Cleaning
* Data Validation
* Data Preparation

---

# 📌 Final Conclusion

The OLA Ride Analytics Dashboard provides a complete overview of booking performance, revenue generation, ride cancellations, and customer satisfaction.

The analysis highlights that while the platform generates strong revenue and maintains good customer ratings, reducing cancellation rates and improving driver availability present the biggest opportunities for business growth.

---

## 👨‍💻 Author

**Kartik Gawali**

Data Analyst | Power BI | SQL | Excel

Connect with me on LinkedIn and GitHub.

