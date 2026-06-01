# 🚖 OLA Ride Analytics Dashboard

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black">
  <img src="https://img.shields.io/badge/SQL-Data%20Analysis-blue">
  <img src="https://img.shields.io/badge/Excel-Data%20Preparation-green">
  <img src="https://img.shields.io/badge/Project-Interactive%20Dashboard-orange">
</p>

---

# 📌 Project Overview

This project focuses on analyzing OLA ride booking data using **Power BI, SQL, and Excel** to provide actionable business insights related to ride bookings, revenue generation, cancellations, vehicle performance, and customer satisfaction.

The dashboard enables stakeholders to monitor operational KPIs and make data-driven decisions for improving ride completion rates and overall business performance.

---

# 📂 Dataset Used

📊 **Dataset Link**

<a href="https://github.com/kartikgawali-00/OLA-Ride-Analytics-Dashboard/blob/main/Dataset.csv">Dataset.csv</a>

---

# 🎯 Project Objective

The objective of this project is to build an interactive dashboard that helps answer critical business questions such as:

- How many rides are booked daily?
- What is the overall revenue generated?
- Which vehicle types perform best?
- What are the major reasons for ride cancellations?
- Which payment methods contribute most to revenue?
- How satisfied are customers and drivers?

---

# 🛠️ Tools & Technologies Used

| Tool | Purpose |
|--------|----------|
| 📊 Power BI | Dashboard Development |
| 🗄️ SQL | Data Analysis |
| 📑 Excel | Data Cleaning & Preparation |
| ⚡ DAX | KPI Creation |
| 🔄 Power Query | Data Transformation |

---

# 📊 Dashboard Pages

## 1️⃣ Overall Dashboard

### KPI Metrics

| KPI | Value |
|------|------|
| 🚕 Total Bookings | 103,024 |
| 💰 Total Revenue | ₹35 Million |
| ✅ Successful Bookings | 63,967 |
| 📈 Booking Success Rate | 62.09% |

### Dashboard Preview

<img src="https://github.com/kartikgawali-00/OLA-Ride-Analytics-Dashboard/blob/main/Dashboard%20Images/Screenshot%202026-06-01%20182805.png?raw=true">

### Key Insights

✅ Total bookings exceeded 103K rides.

✅ Revenue generated reached ₹35 Million.

✅ Successful rides account for 62% of all bookings.

✅ Driver cancellations contribute significantly to ride failures.

---

## 2️⃣ Vehicle Type Analysis

### Business Questions

- Which vehicle type generates the highest booking value?
- Which vehicle category contributes the highest successful bookings?
- What is the average distance travelled?

### Vehicle Categories

- Prime Sedan
- Prime SUV
- Prime Plus
- Mini
- Auto
- Bike
- E-Bike

### Dashboard Preview

<img src="https://github.com/kartikgawali-00/OLA-Ride-Analytics-Dashboard/blob/main/Dashboard%20Images/Screenshot%202026-06-01%20182832.png?raw=true">

### Key Insights

✅ Prime Sedan generated the highest booking value.

✅ Premium vehicle categories contribute strongly to revenue.

✅ Auto rides have the lowest average travel distance.

---

## 3️⃣ Revenue Analysis

### Business Questions

- Which payment method generates maximum revenue?
- What are the daily revenue trends?
- Who are the top customers?

### Dashboard Preview

<img src="https://github.com/kartikgawali-00/OLA-Ride-Analytics-Dashboard/blob/main/Dashboard%20Images/Screenshot%202026-06-01%20182855.png?raw=true">

### Key Insights

✅ Cash contributes the highest share of revenue.

✅ UPI is the second most preferred payment method.

✅ Debit and Credit Card usage remains comparatively low.

---

## 4️⃣ Cancellation Analysis

### KPI Metrics

| KPI | Value |
|------|------|
| 🚕 Total Bookings | 103,024 |
| ✅ Successful Bookings | 63,967 |
| ❌ Cancelled Bookings | 28,933 |
| 📉 Cancellation Rate | 28.08% |

### Dashboard Preview

<img src="https://github.com/kartikgawali-00/OLA-Ride-Analytics-Dashboard/blob/main/Dashboard%20Images/Screenshot%202026-06-01%20182911.png?raw=true">

### Key Insights

✅ Driver-related issues account for the highest cancellation percentage.

✅ Customer cancellations significantly impact ride completion.

✅ Reducing driver cancellations can improve revenue and customer satisfaction.

---

## 5️⃣ Ratings Analysis

### Dashboard Preview

<img src="https://github.com/kartikgawali-00/OLA-Ride-Analytics-Dashboard/blob/main/Dashboard%20Images/Screenshot%202026-06-01%20183018.png?raw=true">

### Key Insights

✅ Customer ratings remain consistently around 4.0.

✅ Driver ratings are maintained above 3.9.

✅ Service quality is relatively stable across vehicle categories.

---

# 🔍 SQL Analysis

### Total Bookings

```sql
SELECT COUNT(*) AS Total_Bookings
FROM Ola_Bookings;
```

### Revenue Analysis

```sql
SELECT SUM(Booking_Value) AS Total_Revenue
FROM Ola_Bookings;
```

### Booking Status Analysis

```sql
SELECT Booking_Status,
       COUNT(*) AS Total_Bookings
FROM Ola_Bookings
GROUP BY Booking_Status;
```

### Revenue by Payment Method

```sql
SELECT Payment_Method,
       SUM(Booking_Value) Revenue
FROM Ola_Bookings
GROUP BY Payment_Method;
```

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

# 💡 Overall Project Insights

### 🚕 Ride Performance

- 103K+ rides analyzed
- 62% booking success rate
- 28% cancellation rate observed

### 💰 Revenue Insights

- ₹35 Million total booking value generated
- Cash and UPI dominate payment methods

### 🚗 Vehicle Insights

- Prime Sedan performs best in revenue generation
- Auto contributes lowest average trip distance

### ⭐ Customer Experience

- Average ratings remain around 4.0
- Customer satisfaction is stable across categories

---

# 🚀 Business Recommendations

### 🚗 Improve Driver Availability

Reduce cancellations by improving driver allocation efficiency.

### 💳 Promote Digital Payments

Encourage UPI and Card transactions through rewards and cashback programs.

### 🚕 Focus on Premium Categories

Expand Prime Sedan and Prime Plus offerings.

### 📉 Reduce Ride Cancellations

Improve ETA accuracy and customer-driver communication.

### ⭐ Enhance Customer Experience

Continue monitoring ratings and customer feedback.

---

# 🏆 Skills Demonstrated

## 📊 Power BI

- Data Modeling
- DAX Measures
- Power Query
- Interactive Dashboards
- KPI Design
- Navigation & Bookmarks

## 🗄️ SQL

- Aggregations
- Group By
- Filtering
- KPI Queries
- Business Analysis

## 📑 Excel

- Data Cleaning
- Data Validation
- Data Preparation

---
---

# 📌 Final Conclusion

The OLA Ride Analytics Dashboard provides a complete overview of booking performance, revenue generation, ride cancellations, and customer satisfaction.

The analysis highlights that while the platform generates strong revenue and maintains positive customer ratings, reducing cancellation rates and improving driver availability present the biggest opportunities for business growth.

---

# 👨‍💻 Author

## Kartik Gawali

📊 Data Analyst | Power BI | SQL | Excel

⭐ If you found this project useful, don't forget to star the repository.
