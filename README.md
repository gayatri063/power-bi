# Power BI Analytics Projects

This repository contains two end-to-end **Microsoft Power BI Business Intelligence projects** demonstrating data modeling, interactive dashboard design, KPI tracking, and operational analytics. Each project includes a cleaned 15,000-record dataset and a rich, interactive `.pbix` report.

---

## Repository Structure

| File Name | File Type | Records / Size | Project Description |
| :--- | :---: | :---: | :--- |
| **`Uber_Eats_Performance_Dashboard.pbix`** | Power BI Report (`.pbix`) | 1.04 MB | Interactive sales, revenue, and restaurant partner analytics dashboard for Uber Eats. |
| **`Uber_Eats_15K_Dataset.xlsx`** | Excel Dataset (`.xlsx`) | 15,000 Rows (21 Cols) | Source sales and order dataset for the Uber Eats dashboard. |
| **`Wynn_Resort_Performance_Dashboard.pbix`** | Power BI Report (`.pbix`) | 1.04 MB | Resort operations, occupancy, ADR, and revenue analytics dashboard for Wynn Al Marjan Island. |
| **`Hotel_Dataset_15000.xlsx`** | Excel Dataset (`.xlsx`) | 15,000 Rows (22 Cols) | Source hospitality and bookings dataset for the Wynn Resort dashboard. |

---

## 1. Uber Eats Sales & Performance Dashboard

### Project Definition & Business Objective
The **Uber Eats Sales & Performance Dashboard** evaluates food delivery marketplace dynamics across 15,000 orders. The project provides deep visibility into restaurant partner performance, cuisine profitability, delivery efficiency, customer demographics, and order economics.

```
+-----------------------------------------------------------------------------------+
|                  UBER EATS SALES AND PERFORMANCE DASHBOARD                        |
+-----------------------------------------------------------------------------------+
|  [ Total Revenue ]   [ Total Orders ]   [ Average Ratings ]   [ Avg Order Value ] |
+----------------------------------------+------------------------------------------+
|  Revenue by Cuisine                    |  Revenue by Restaurant Type              |
|  (Italian, Asian, American, Mexican)   |  (Chain, Independent, Cloud Kitchen)     |
+----------------------------------------+------------------------------------------+
|  Revenue by Food Category              |  Revenue by Join Year (Cohort Analysis)  |
+----------------------------------------+------------------------------------------+
|  Restaurant Performance Summary (Interactive Matrix & Delivery Analytics)         |
+-----------------------------------------------------------------------------------+
```

### Core Key Performance Indicators (KPIs)
- **Total Revenue**: Cumulative net sales generated across all orders and restaurant partners.
- **Total Orders**: Overall order volume across cities and timeframes.
- **Average Customer Rating**: Mean customer satisfaction score on a 5.0 scale.
- **Average Order Value (AOV)**: Average dollar spend per transaction.

### Dashboard Visualizations & Analytics
1. **Revenue by Cuisine**: Categorical comparison of sales across cuisines (e.g., Italian, Asian, American, Mexican, etc.).
2. **Revenue by Restaurant Type & Size**: Segmented performance comparing restaurant formats (chain vs. independent, small vs. large enterprise).
3. **Revenue by Food Category**: Sales breakdown across meal courses and food categories.
4. **Revenue by Join Year**: Cohort analysis showing long-term value and revenue contribution by partner onboarding year.
5. **Restaurant Performance Summary**: Granular matrix detailing individual restaurant ratings, order counts, delivery times, and net revenue.

### Source Data Dictionary (`Uber_Eats_15K_Dataset.xlsx`)
| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `Order_ID` | Identifier | Unique transaction reference for each order. |
| `Order_Date` / `Order_Hour` | Temporal | Timestamp showing date and hour of order placement. |
| `City` / `Restaurant` | Categorical | Geographic location and name of the restaurant partner. |
| `Cuisine` / `Food_Category` | Categorical | Primary cuisine type and specific food menu category. |
| `Restaurant_Type` / `Restaurant_Size` | Categorical | Operating model (Chain/Independent) and scale of the restaurant. |
| `Join_Year` | Temporal | Onboarding year of the restaurant partner on Uber Eats. |
| `Order_Value` / `Delivery_Fee` / `Discount` | Numeric (Currency) | Financial components comprising total order gross and net pricing. |
| `Net_Revenue` | Numeric (Currency) | Final recognized revenue after discounts and adjustments. |
| `Delivery_Time_Min` | Numeric | Total order fulfillment and delivery duration in minutes. |
| `Customer_Rating` | Numeric (1.0–5.0) | Customer rating submitted after delivery completion. |
| `Payment_Method` / `Order_Status` | Categorical | Transaction method and final order completion status. |
| `Customer_Gender` / `Age_Group` | Demographics | Demographics of the ordering customer. |
| `Weekend` | Boolean (0/1) | Flag indicating weekday vs. weekend transaction. |

---

## 2. Wynn Al Marjan Island Resort Performance Dashboard

### Project Definition & Business Objective
The **Wynn Al Marjan Island Resort Performance Dashboard** is an executive hospitality intelligence tool designed for luxury resort operations. Analyzing 15,000 hotel bookings, the dashboard tracks revenue generation, room occupancy, guest satisfaction, department profitability, and booking channels to optimize revenue per available room (RevPAR) and guest experience.

```
+-----------------------------------------------------------------------------------+
|             WYNN AL MARJAN ISLAND - RESORT PERFORMANCE DASHBOARD                  |
+-----------------------------------------------------------------------------------+
|  [ Total Revenue ]   [ Total Bookings ]  [ Occupancy Rate ]   [ ADR & RevPAR ]    |
+----------------------------------------+------------------------------------------+
|  Revenue Trend (Monthly / Seasonal)    |  Occupancy Rate by Month                 |
+----------------------------------------+------------------------------------------+
|  Revenue by Room Type (Suites/Deluxe)  |  Booking Source (Direct/OTA/Corporate)   |
+----------------------------------------+------------------------------------------+
|  Revenue by Department (Rooms/F&B/Spa) |  Guests by Nationality & Satisfaction    |
+-----------------------------------------------------------------------------------+
```

### Core Key Performance Indicators (KPIs)
- **Total Revenue**: Aggregate resort earnings from room bookings and ancillary services.
- **Total Bookings**: Count of confirmed guest reservations.
- **Occupancy Rate**: Percentage of available rooms occupied across reporting periods.
- **Average Daily Rate (ADR)**: Average rental revenue earned per occupied room day.
- **Average Revenue (RevPAR)**: Revenue generated per booking / per available room.
- **Customer Ratings**: Overall guest satisfaction rating on a 5.0 scale.

### Dashboard Visualizations & Analytics
1. **Revenue Trend**: Month-over-month trajectory of earnings highlighting seasonality and peak resort demand.
2. **Occupancy Rate by Month**: Seasonal occupancy fluctuations across winter and summer periods.
3. **Revenue by Room Type**: Revenue performance comparing Deluxe Rooms, Executive Suites, Penthouses, and Villas.
4. **Booking Source Analysis**: Attribution of reservations across Direct Bookings, Online Travel Agencies (OTAs), Corporate agreements, and Walk-ins.
5. **Revenue by Department**: Multi-department revenue breakdown across Room Reservations, F&B (Food & Beverage), Spa & Wellness, and Events.
6. **Guests by Nationality & Satisfaction**: Demographic mix of international and domestic guests correlated with cancellation rate trends and ratings.
7. **Room Performance Summary**: Interactive summary table providing filtering across room types, dates, and channels.

### Source Data Dictionary (`Hotel_Dataset_15000.xlsx`)
| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `BookingID` | Identifier | Unique reservation reference code. |
| `BookingDate` / `CheckInDate` / `CheckOutDate` | Temporal | Key lifecycle dates for reservation placement and guest stay. |
| `Year` / `Month` | Temporal | Date hierarchy attributes for seasonal aggregation. |
| `RoomType` | Categorical | Reserved accommodation class (e.g., Deluxe, Suite, Villa). |
| `BookingSource` | Categorical | Acquisition channel (e.g., Direct, OTA, Corporate, Agent). |
| `Department` | Categorical | Revenue-generating resort department (Rooms, F&B, Spa, etc.). |
| `GuestNationality` | Categorical | Primary nationality/country of origin of the booked guest. |
| `Adults` / `Children` / `TotalGuests` | Numeric | Party size breakdown per reservation. |
| `Nights` | Numeric | Length of stay in number of nights. |
| `ADR` | Numeric (Currency) | Average Daily Rate charged per night. |
| `Revenue` / `RevPAR` | Numeric (Currency) | Total recognized revenue and Revenue per Available Room metric. |
| `OccupancyRate` | Numeric (Percentage) | Daily/monthly occupancy utilization figure. |
| `GuestRating` | Numeric (1.0–5.0) | Post-stay evaluation rating provided by the guest. |
| `CancellationFlag` / `CancellationReason` | Categorical | Status indicator for cancelled reservations and underlying cause. |
| `BookingStatus` / `PaymentMethod` | Categorical | Current reservation state and transaction instrument used. |

---

## Getting Started

1. **Prerequisites**: Ensure you have [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed on Windows.
2. **Opening a Report**:
   - Launch `Uber_Eats_Performance_Dashboard.pbix` or `Wynn_Resort_Performance_Dashboard.pbix` directly in Power BI Desktop.
   - Use the built-in slicers, cross-filtering, and drill-through capabilities to explore the underlying datasets interactively.
3. **Data Source Updates**:
   - If refreshing the model, point Power BI's Data Source Settings to the corresponding `.xlsx` file located in this repository (`Uber_Eats_15K_Dataset.xlsx` or `Hotel_Dataset_15000.xlsx`).