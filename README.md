# ✈️ Airline Revenue & Occupancy Optimization Analysis

## 📌 Project Overview

This project analyzes airline operational data to evaluate aircraft occupancy rates, revenue performance, and profitability per seat. The objective is to identify strategic opportunities to increase aircraft utilization and maximize turnover under current market constraints.

The analysis was performed using **Python (Pandas, NumPy, Matplotlib, Seaborn)** and **SQLite (SQL queries)** within a Jupyter Notebook environment.

---

## 🎯 Problem Statement

The airline company aims to enhance aircraft occupancy rates and improve profitability per seat while addressing the following operational challenges:

### Key Challenges

1. **Stricter Environmental Regulations**
   - Increased operational costs
   - Limited expansion capacity

2. **Higher Flight Taxes**
   - Increased ticket prices
   - Reduced passenger demand

3. **Tight Labor Market**
   - Higher labor costs
   - Increased employee turnover

Given these constraints, optimizing seat utilization and revenue generation becomes critical.

---

## 🛠 Tools & Technologies

| Tool | Purpose |
|------|----------|
| SQLite | Database storage and querying |
| Python | Data analysis |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Jupyter Notebook | Interactive analysis |

---

## 📂 Data Source

The dataset was downloaded directly from Kaggle:

```python
import kagglehub

# Download dataset
path = kagglehub.dataset_download("datalearn/airlines-db")
```

The dataset includes relational tables such as:

- flights  
- aircrafts  
- seats  
- bookings  
- tickets  
- ticket_flights  
- boarding_passes  

All data is stored in an SQLite database.

---

## 🔌 Database Connection

```python
import sqlite3

connection = sqlite3.connect("airlines.sqlite")
cursor = connection.cursor()
```

---

## 📊 Analysis Performed

### 1️⃣ Aircraft Capacity Analysis
- Compared seat capacity across aircraft types.
- Identified high-capacity aircraft (e.g., 773, 763).
- Determined that seat capacity alone does not guarantee highest revenue.

<p align="center">
  <img src="images/Planes with More than 100 Seats.png" alt="Planes with More than 100 Seats" width="1000"/>
</p>

---

### 2️⃣ Ticket Volume & Revenue Trend Analysis
- Analyzed number of tickets booked over time.
- Compared revenue growth patterns.
- Found strong correlation between ticket volume and total revenue.
- Revenue growth is primarily volume-driven rather than price-driven.

<p align="center">
  <img src="images/Number of Tickets Booked Over Time.png" alt="Number of Tickets Booked Over Time" width="1000"/>
</p>


<p align="center">
  <img src="images/Sum of Amount EarnerdOver Time.png" alt="Sum of Amount EarnerdOver Time" width="1000"/>
</p>

---

### 3️⃣ Fare Class Pricing Analysis
- Compared average fares across Business, Economy, and Comfort classes.
- Business fares are approximately 3× Economy fares.
- Wide-body aircraft generate higher premium revenue.

<p align="center">
  <img src="images/Average Charges by Aircraft and Fare Condition.png" alt="Average Charges by Aircraft and Fare Condition" width="1000"/>
</p>

---

### 4️⃣ Total Revenue by Aircraft
- SU9 generated the highest revenue.
- 763 and 773 followed.
- CN1 contributed minimal revenue.

<p align="center">
  <img src="images/Total Revenue by Aircraft Over Years.png" alt="Total Revenue by Aircraft Over Years" width="1000"/>
</p>

Key Insight:  
Operational frequency and route allocation impact revenue more than aircraft size alone.

---

### 5️⃣ Average Occupancy Rate Analysis
- 773 showed the highest occupancy (~33%).
- CN1 showed the lowest occupancy (~7%).
- Significant unused seat capacity exists across multiple aircraft.

<p align="center">
  <img src="images/Average Occupancy Rate by Aircraft.png" alt="Average Occupancy Rate by Aircraft" width="1000"/>
</p>

---

### 6️⃣ Scenario Modeling – 10% Occupancy Increase

A hypothetical scenario was modeled assuming:

- 10% increase in occupancy
- Constant ticket prices
- Constant seat capacity

Mathematical assumption:

Revenue_new = Revenue_current × 1.10

Incremental Revenue = 0.10 × Current Revenue


<p align="center">
  <img src="images/Turnover Increase.png" alt="Turnover Increase" width="1000"/>
</p>


Findings:

- SU9 shows the highest absolute revenue increase.
- 763 and 773 provide strong upside potential.
- CN1 yields minimal financial impact even with improved occupancy.

---

## 📈 Key Insights

- Revenue is primarily driven by ticket volume.
- High-capacity aircraft are not automatically the most profitable.
- Significant opportunity exists to improve load factors.
- Improving occupancy of high-revenue aircraft produces the greatest financial impact.

---

## 💡 Strategic Recommendations

1. Focus on improving occupancy for high-revenue aircraft (SU9, 763, 773).
2. Optimize route allocation for underperforming aircraft.
3. Strengthen premium seat marketing on high-yield routes.
4. Improve demand forecasting to reduce unused capacity.

---

## 📌 Final Conclusion

The analysis demonstrates that increasing aircraft occupancy is a highly effective strategy to improve airline profitability under rising cost pressures.

A 10% increase in occupancy results in a proportional 10% increase in turnover, assuming pricing and capacity remain constant. Aircraft with higher base revenue generate the largest absolute gains.

The most effective growth strategy is to prioritize high-performing aircraft and optimize route utilization rather than focusing solely on fleet expansion.

---

## 🚀 Future Improvements

- Revenue per Available Seat Mile (RASM)
- Route-level profitability modeling
- Cost integration for net profit analysis
- Time-series demand forecasting
- Multi-scenario sensitivity analysis (5%, 10%, 15%)

---

## 📎 Project Type

Airline Data Analysis  
Python | SQL | Data Visualization | Scenario Modeling
