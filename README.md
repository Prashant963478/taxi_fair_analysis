# 🚖 Ride Booking Analytics Dashboard (Power BI)

An end-to-end analysis of **150,000 ride-hailing bookings** from 2024, built in Power BI to uncover trends in revenue, cancellations, vehicle performance, and customer/driver ratings.

---

## 📌 Project Overview

Ride-hailing platforms generate huge volumes of trip data every day, but raw logs rarely tell a clear story on their own. This project transforms a full year of booking records into a multi-page, interactive Power BI dashboard that a business or operations team could use to monitor performance, spot cancellation patterns, and track revenue.

**Dataset:** `rideBookings.csv` — 150,000 records, Jan 1 – Dec 30, 2024
**Dashboard:** `yt.pbix` — 7-page interactive Power BI report

---

## 🗂️ Dataset Description

Each row represents a single ride booking, with fields covering:

| Category | Columns |
|---|---|
| Trip identifiers | `Booking ID`, `Customer ID`, `Date`, `Time` |
| Trip details | `Vehicle Type`, `Pickup Location`, `Drop Location`, `Ride Distance` |
| Status | `Booking Status`, cancellation flags, cancellation/incomplete reasons |
| Service timing | `Avg VTAT` (vehicle turnaround time), `Avg CTAT` (customer turnaround time) |
| Financials | `Booking Value`, `Payment Method` |
| Feedback | `Driver Ratings`, `Customer Rating` |

**Key stats:**
- **150,000** total bookings across **148,788** unique customers
- **7** vehicle types: Auto, Go Mini, Go Sedan, Bike, Premier Sedan, eBike, Uber XL
- **176** unique pickup zones
- **6** payment methods (UPI, Cash, Uber Wallet, Credit Card, Debit Card, plus unpaid/cancelled trips)

**Booking status breakdown:**

| Status | Count | % of Total |
|---|---|---|
| Completed | 93,000 | 62% |
| Cancelled by Driver | 27,000 | 18% |
| No Driver Found | 10,500 | 7% |
| Cancelled by Customer | 10,500 | 7% |
| Incomplete | 9,000 | 6% |

---

## 📊 Dashboard Pages

The `.pbix` report is organized into 7 pages:

1. **Homepage** – Landing/cover page with report navigation
2. **Overall** – High-level KPIs, booking trend over time, and status split
3. **Vehicle Type** – Performance breakdown (bookings, revenue, ratings, distance) by vehicle category
4. **Revenue** – Revenue by vehicle type and payment method, with a detailed transaction table
5. **Cancellation** – Cancellation-reason breakdown for both customers and drivers
6. **Ratings** – Driver and customer rating distributions and trends
7. **Summary** – Executive summary combining KPI cards, gauges, and combo charts, with slicers for date, vehicle type, and status

Each page uses slicers (date, vehicle type, payment method) so the report is fully interactive and filterable.

---

## 🔍 Key Insights

- Only **62%** of bookings were completed — a substantial **31%** were lost to cancellations (by driver or customer) or "No Driver Found," highlighting a significant supply/matching problem.
- **Driver-side cancellations (18%)** outnumber customer-side cancellations (7%) by a wide margin, with the top driver reasons being customer-related issues and personal/vehicle problems.
- The top customer cancellation reasons are **wrong address**, **change of plans**, and the **driver not moving toward pickup** — pointing to both address-data quality and driver-app tracking issues.
- **Auto** and **Go Mini** are the most-booked vehicle types, together accounting for roughly 45% of all rides.
- Average booking value across completed/valued trips is **≈ ₹508**, with **UPI** as the dominant payment method.
- **9,000 rides (6%)** were marked incomplete, split fairly evenly between customer demand, vehicle breakdown, and other issues — a useful signal for fleet maintenance planning.

---

## 🛠️ Tools & Techniques

- **Power BI Desktop** – data modeling, DAX measures, and report design
- **Power Query** – data cleaning (handling `null` values, deduplicating quoted IDs, type conversions)
- **DAX** – calculated measures for completion rate, cancellation rate, average ratings, and revenue KPIs
- Interactive **slicers**, **KPI cards**, **gauge**, **combo charts**, and **detail tables** for drill-down analysis

---

## 📁 Repository Contents

```
├── rideBookings.csv   # Raw dataset (150,000 ride bookings, 2024)
├── yt.pbix             # Power BI dashboard file
└── README.md           # Project documentation
```

---

## 🚀 How to Use

1. Clone or download this repository.
2. Open `yt.pbix` in **Power BI Desktop** (free download from Microsoft).
3. Use the slicers on each page to filter by date, vehicle type, or booking status.
4. Explore the **Summary** page for a quick executive overview, or dive into individual pages for deeper analysis.

---

## 👤 Author

**Prashant Solanki**
B.Tech Computer Science, GLA University
[GitHub](https://github.com/Prashant963478)
