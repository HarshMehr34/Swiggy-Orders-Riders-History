# 📌 Project Overview
. This project analyzes the relationship between First-Mile Distance (driver-to-restaurant) and Order Assignment Latency to identify bottlenecks in the delivery dispatch lifecycle. By analyzing thousands of data points for both delivered and cancelled orders, the study aims to optimize driver dispatching logic and reduce order churn.

# 📊 Key Insights

. The "Golden Window": 85% of successful deliveries are assigned within the first 100 seconds. Latency beyond 200 seconds shows a sharp decline in delivery probability.

. Cancellation Correlation: High-latency cancellations occur regardless of distance, suggesting that "Time-to-Assign" is a higher predictor of churn than "Driver Proximity."

# 🛠 Tech Stack
. Language: Python

. Libraries: Pandas (Data Wrangling), Matplotlib/Seaborn (Visualization), NumPy

. Analysis Techniques: Scatter Plot Density Analysis, Latency Distribution, Geospatial Constraint Identification.

# 📈 Visualizations

💡 Business Recommendations
Dynamic Radius: Implement a dynamic first-mile radius that expands from 4 to 5 units during low-supply periods to capture more orders.

Predictive Re-assignment: Orders not assigned within 120 seconds should be flagged for "Priority Dispatch" to prevent them from entering the high-latency churn zone.


# Data Cleaning:
. Add a small section in your README or Notebook about how you handled outliers or null values. In real-world data jobs, cleaning is 80% of the work.
